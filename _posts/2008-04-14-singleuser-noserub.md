---
ID: 812
post_title: SingleUser NoseRub
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/04/14/singleuser-noserub/
published: true
post_date: 2008-04-14 19:22:10
---
<!-- wp:paragraph -->
<p>Eigentlich wollte ich <a href="http://noserub.com/">NoseRub</a> schon vor ner ganze Weile mal testen, jetzt habe ich die seit vorgestern erhältliche <a href="http://noserub.com/blog/archives/52-NoseRub-0.6-released.html">Version 0.6</a> zum Anlass genommen, NoseRub mal auf meinem Server zu installieren: <a href="http://pfefferle.org">pfefferle.org</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Wer NoseRub, wie ich als SingleUser-System auf seinem Server/Webspace hosten will (anstatt als Service wie <a href="http://identoo.com/">Identoo.com</a>) muss nur zwei Dinge beachten:</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>NoseRub Registration Type</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Zuerst sollte man sicherstellen dass sich keiner bei NoseRub registrieren kann, dazu einfach die Datei "<code>app/config/noserub.php</code>" öffnen und den <code>NOSERUB_REGISTRATION_TYPE</code> auf <code>none</code> setzen.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>define('NOSERUB_REGISTRATION_TYPE', 'none');</code></pre>
<!-- /wp:code -->

<!-- wp:heading {"level":4} -->
<h4>SocialStream durch "My Profile" ersetzen</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Im zweiten Schritt kann man die Startseite (SocialStream) durch sein eigenes Profil ersetzen. Hierzu muss man in der "<code>app/config/routes.php</code>" einfach nur die Zeile</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Router::connect('/', array('controller' => 'identities', 'action' => 'social_stream'));</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...mit...</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Router::connect('/', array('controller' => 'identities', 'action' => 'index', 'username' => 'USERNAME'));</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...ersetzen und statt <strong>USERNAME</strong> den eigenen Benutzernamen eintragen. Das wars eigentlich schon.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Viel Spaß beim ausprobieren :)</p>
<!-- /wp:paragraph -->