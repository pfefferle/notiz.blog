---
ID: 812
post_title: SingleUser NoseRub
author: Matthias Pfefferle
post_date: 2008-04-14 19:22:10
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/04/14/singleuser-noserub/
published: true
aktt_notify_twitter:
  - 'no'
---
Eigentlich wollte ich <a href="http://noserub.com/">NoseRub</a> schon vor ner ganze Weile mal testen, jetzt habe ich die seit vorgestern erhältliche <a href="http://noserub.com/blog/archives/52-NoseRub-0.6-released.html">Version 0.6</a> zum Anlass genommen, NoseRub mal auf meinem Server zu installieren: <a href="http://pfefferle.org">pfefferle.org</a>

Wer NoseRub, wie ich als SingleUser-System auf seinem Server/Webspace hosten will (anstatt als Service wie <a href="http://identoo.com/">Identoo.com</a>) muss nur zwei Dinge beachten:

<h4>NoseRub Registration Type</h4>

Zuerst sollte man sicherstellen dass sich keiner bei NoseRub registrieren kann, dazu einfach die Datei "<code>app/config/noserub.php</code>" öffnen und den <code>NOSERUB_REGISTRATION_TYPE</code> auf <code>none</code> setzen.

<p class="code">define('NOSERUB_REGISTRATION_TYPE', 'none');</p>

<h4>SocialStream durch "My Profile" ersetzen</h4>

Im zweiten Schritt kann man die Startseite (SocialStream) durch sein eigenes Profil ersetzen. Hierzu muss man in der "<code>app/config/routes.php</code>" einfach nur die Zeile

<p class="code">Router::connect('/', array('controller' => 'identities', 'action' => 'social_stream'));</p>

...mit...

<p class="code">Router::connect('/', array('controller' => 'identities', 'action' => 'index', 'username' => '<strong>USERNAME</strong>'));</p>

...ersetzen und statt <strong>USERNAME</strong> den eigenen Benutzernamen eintragen. Das wars eigentlich schon.

Viel Spaß beim ausprobieren :)