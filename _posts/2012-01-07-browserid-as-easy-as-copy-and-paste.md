---
ID: 4102
post_title: 'BrowserID &#8211; as easy as copy &#038; paste'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2012/01/07/browserid-as-easy-as-copy-and-paste/
published: true
post_date: 2012-01-07 17:35:27
---
<!-- wp:image {"id":4104,"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2012/01/BrowserID.jpg" alt="BrowserID" class="wp-image-4104" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Ich schreibe gerade einen Artikel für das <a href="http://t3n.de/">t3n Magazin</a> über aktuelle Sign-In-Mechanismen und hab mir in dem Zuge BrowserID mal etwas genauer angeschaut. Ich bin wirklich extrem überrascht mit wie wenig Arbeit es sich in z.B. WordPress einbauen lässt.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="https://browserid.org/">BrowserID</a> besteht eigentlich nur aus einem <abbr title="JavaScript">JS</abbr>-File,ein paar Zeilen <abbr title="JavaScript">JS</abbr>-Code:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;script src="https://browserid.org/include.js" type="text/javascript">&lt;/script>
&lt;script type="text/javascript">
navigator.id.get(function(assertion) {
    if (assertion) {
        // This code will be invoked once the user has successfully
        // selected an email address they control to sign in with.
    } else {
        // something went wrong!  the user isn't logged in.
    }
});
&lt;/script></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>und dem anschließenden Verifizieren der <code>assertion</code>:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>$ curl -d "assertion=&amp;audience=https://mysite.com" "https://browserid.org/verify"
{
    "status": "okay",
    "email": "lloyd@example.com",
    "audience": "https://mysite.com",
    "expires": 1308859352261,
    "issuer": "browserid.org"
}</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Den ausführlichen Ablauf der Authentifizierung findet ihr auf <a href="https://github.com/mozilla/browserid/wiki/How-to-Use-BrowserID-on-Your-Site">Github</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Um BrowserID in WordPress zu integrieren lädt man also zuerst den <abbr title="JavaScript">JS</abbr>-Code in den Login Header:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>// add the BrowserID javascript-code to the header
add_action('login_head', 'bi_add_js_header');
function bi_add_js_header() {
  echo '&lt;script src="https://browserid.org/include.js" type="text/javascript">&lt;/script>';
  echo '&lt;script type="text/javascript">'."\n";
  echo 'function browser_id_login() {
    navigator.id.get(function(assertion) {
      if (assertion) {
        window.location="' . get_site_url(null, '/') .'?browser_id_assertion=" + assertion;
      } else {
        // do nothing!
      }
    })
  };'."\n";
  echo '&lt;/script>';
}</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>und platziert den BrowserID-Button auf der Login-Seite:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>// add the login button
add_action('login_form', 'bi_add_button');
function bi_add_button() {
  echo '&lt;p>&lt;a href="#" onclick="return browser_id_login();">&lt;img src="https://browserid.org/i/sign_in_blue.png" style="border: 0;" />&lt;/a>&lt;/p>';
}</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Nach dem klick auf den Button öffnet sich das Autorisierungs-Fenster von BrowserID und nach dem erfolgreichen Sign-In wird die gerade implementierte Methode <code>navigator.id.get(function(assertion) {}</code> aufgerufen.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":4111,"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2012/01/BrowserID-login-window.jpg" alt="BrowserID login window" class="wp-image-4111" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Im nächsten Schritt muß man die erhaltene <code>assertion</code> über BrowserID.org verifizieren. Da ich den notwendigen <code>POST</code> nicht über JavaScript absetzen will, leite ich einfach auf eine Seite weiter und übergebe die erhaltene <code>assertion</code> als GET-Paramater.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>if (assertion) {
  window.location="' . get_site_url(null, '/') .'?browser_id_assertion=" + assertion;
}</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Jetzt kann der POST bequem über WordPress abgesetzt werden.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>// the verification code
add_action('parse_request', 'bi_verify_id');
function bi_verify_id() {
  global $wp_query, $wp, $user;

  if( array_key_exists('browser_id_assertion', $wp->query_vars) ) {
    // some settings for the post request
    $args = array(
      'method' => 'POST',
      'timeout' => 30,
      'redirection' => 0,
      'httpversion' => '1.0',
      'blocking' => true,
      'headers' => array(),
      'body' => array(
        'assertion' => $wp->query_vars['browser_id_assertion'], // the assertion number we get from the js
        'audience' => "http://".$_SERVER['HTTP_HOST'] // the server host
      ),
      'cookies' => array(),
      'sslverify' => 0
    );

    // check the response
    $response = wp_remote_post("https://browserid.org/verify", $args);

    if (!is_wp_error($response)) {
      $bi_response = json_decode($response['body'], true);

      // if everything is ok, check if there is a user with this email address
      if ($bi_response['status'] == 'okay') {
        $userdata = get_user_by('email', $bi_response['email']);
        if ($userdata) {
          $user = new WP_User($userdata->ID);
          wp_set_current_user($userdata->ID, $userdata->user_login);
          wp_set_auth_cookie($userdata->ID, $rememberme);
          do_action('wp_login', $userdata->user_login);

          wp_redirect(home_url());
          exit;
        } else {
          // show error when there is no matching user
          echo "no user with email address '" . $bi_response['email'] . "'"; 
          exit;
        }
      }
    }
    
    // show error if something didn't work well
    echo "error logging in"; 
    exit;
  }
}</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Gibt es einen User mit der entsprechenden E-Mail - Adresse wird er eingeloggt, falls nicht, wird ein Fehler ausgegeben.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Bei der Demo hab ich mir aus Zeitgründen ein wenig Code bei Marcel Bokhorst geliehen, dessen <a href="http://wordpress.org/extend/plugins/browserid/">BrowserID-Plugin</a> wesentlich ausgereifter und vollständiger ist als der kleine Demo-Code den ich hier zusammengestückelt habe.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Wenn euch das zu schnell ging und ich auf einige Details nicht genügend eingegangen bin, könnt ihr gerne fragen :)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ich habe den kompletten Code übrigens auch auf <a href="https://gist.github.com/1574995">Github</a> hochgeladen... das ist einfacher als sich alles zusammen zu kopieren.</p>
<!-- /wp:paragraph -->