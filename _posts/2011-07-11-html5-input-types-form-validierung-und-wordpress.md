---
ID: 3840
post_title: >
  HTML5, Input-Types, Form-Validierung und
  WordPress
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2011/07/11/html5-input-types-form-validierung-und-wordpress/
published: true
post_date: 2011-07-11 20:46:37
---
<!-- wp:image {"align":"right"} -->
<figure class="wp-block-image alignright" style="max-width:50%"><img src="https://notiz.blog/wp-content/uploads/2011/07/HTML5_Logo_256.png" alt="HTML5 Logo" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Dass HTML5 ein paar neue input-types definiert, habe ich durch die <a href="http://microformats.org/wiki/hcard-input-brainstorming#HTML5_input_types">hcard-input-brainstorming</a> so am Rande auf geschnappt, mir aber nichts weiter dabei gedacht... Durch Zufall bin ich heute aber über folgenden <a href="http://twitter.com/sprungmarkers/status/90305500108947457">Tweet</a> von Sylvia Egger gestoßen:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
    <p>Just implemented native #HTML5 form validation on #wp comments form - it&#x27; quite simple &amp; should be in #wp default theme</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>und habe bissle recherchiert... Mit den neuen Input-Types ist es doch tatsächlich möglich Input-Felder über den Browser validieren zu lassen... Ich bin begeistert! :)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Trägt man beispielsweise eine Nicht-Email-Adresse in folgendes Feld...</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;input type=&quot;email&quot; /&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>bekommt man...</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2011/07/firefox-email-validation.jpg" alt="Email Validation im Firefox" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Schön wenn man sich noch über solche Kleinigkeiten freuen kann oder ;)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Lange rede kurzer Sinn: Da WordPress alle Formulare an zentraler Stelle definiert, ist es ziemlich einfach sie mit ein paar neuen Input-Types zu versehen. Mit dem folgenden Code wird das Kommentar-Formular mit den Typen &quot;email&quot; und &quot;url&quot; und das Suchformular mit dem Typ &quot;search&quot; (funktioniert nur in den WebKit-Browsern) erweitert:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><ins><strong>Code-Update</strong>: <a href="http://yatil.de/">Eric Eggert</a> hat mich in den <a href="https://notiz.blog/2011/07/11/html5-input-types-form-validierung-und-wordpress/#comment-173210">Kommentaren</a> darauf hingewiesen, dass man mit <code>&lt;input required /&gt;</code> auch noch die Pflichtfelder validieren kann. Danke!</ins></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><ins><strong>Code-Update 2</strong>: Dank <a href="http://www.im-tal.net">maxe</a> werden jetzt auch die WordPress Settings berücksichtigt (Comment author must fill out name and e-mail) und das &quot;Comment&quot;-Feld ist natürlich auch <code>required</code></ins></p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;?php
/*
Plugin Name: html5 input-types
Plugin URI: https://notiz.blog/
Description: Adds the new HTML5 input-types to WordPress&#x27; default forms
Version: 0.1
Author: pfefferle
Author URI: https://notiz.blog/
*/

add_filter(&quot;comment_form_default_fields&quot;, &quot;change_comment_input_types&quot;);

function change_comment_input_types($fields) {
  if (get_option(&quot;require_name_email&quot;, false)) {
    $fields[&#x27;author&#x27;] = preg_replace(&#x27;/&lt;input/&#x27;, &#x27;&lt;input required&#x27;, $fields[&#x27;author&#x27;]);
    $fields[&#x27;email&#x27;] = preg_replace(&#x27;/&quot;text&quot;/&#x27;, &#x27;&quot;email&quot; required&#x27;, $fields[&#x27;email&#x27;]);
  } else {
    $fields[&#x27;email&#x27;] = preg_replace(&#x27;/&quot;text&quot;/&#x27;, &#x27;&quot;email&quot;&#x27;, $fields[&#x27;email&#x27;]);
  }

  $fields[&#x27;url&#x27;] = preg_replace(&#x27;/&quot;text&quot;/&#x27;, &#x27;&quot;url&quot;&#x27;, $fields[&#x27;url&#x27;]);

  return $fields;
}

add_filter(&quot;get_search_form&quot;, &quot;change_search_form_input_types&quot;);

function change_search_form_input_types($form) {
  return preg_replace(&#x27;/&quot;text&quot;/&#x27;, &#x27;&quot;search&quot;&#x27;, $form);
}

add_filter(&quot;comment_form_field_comment&quot;, &quot;change_comment_field_input_types&quot;);

function change_comment_field_input_types($field) {
  return preg_replace(&#x27;/&lt;textarea/&#x27;, &#x27;&lt;textarea required&#x27;, $field);
}
?&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Funktioniert als Plugin und in Child-Themes (einfach in die <code>functions.php</code> kopieren).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Danke auch an <a href="http://marcgoertz.de/">Marc Görtz</a> der mich über <a href="http://twitter.com/dreamseer">Twitter</a> reichlich mit Links zu dem Thema versorgt hat:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li><a href="http://diveintohtml5.info/forms.html">A Form of Madness (den hab ich selber gefunden)</a></li>
    <li><a href="http://html5pattern.com/">HTML5 Pattern</a></li>
    <li><a href="http://flowplayer.org/tools/demos/validator/index.html">Fallback jQuery Validator</a></li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Testen könnt ihr das übrigens hier auf notiz.blog.</p>
<!-- /wp:paragraph -->