---
ID: 715
post_title: AOL will XMPP/Jabber einsetzen?
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/01/18/aol-will-xmppjabber-einsetzen/
published: true
post_date: 2008-01-18 20:57:45
---
<!-- wp:paragraph -->
<p>Nach einem <a href="http://florianjensen.com/2008/01/17/aol-adopting-xmpp-aka-jabber/">Blog-Eintrag</a> von Florian Jensen will <a href="http://www.aol.com">AOL</a> für seinen Instant Messenger (kurz IM) <a href="http://www.aol.de/AIM/"><abbr title="AOL Instant Messenger">AIM</abbr></a>, zukünftig auf <abbr title="Extensible Messaging and Presence Protocol">XMPP</abbr> (oder auch <a href="http://www.jabber.org/">Jabber</a>) setzen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Eine Anleitung im <a href="http://wiki.jabber.org/index.php/AOL_Alpha">Jabber Wiki</a> erklärt die Schritte:</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol>
	<li>JIDs like uin@aol.com or username@aol.com</li>
	<li>Host: xmpp.oscar.aol.com : 5222</li>
	<li>Allow SASL PLAIN</li>
	<li>Turn on StartTLS</li>
	<li>Make sure there is no '@' in the resource (bug in the service). Some clients by default add a resource with an @ in it. So you have to overwrite this</li>
</ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Ich hab das ganze mal mit <a href="http://www.adiumx.com/">Adium</a> ausprobiert und mit folgende Einstellungen sollte es funktionieren:</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/01/aol-jabber-adium.jpg" alt="aol-jabber-adium.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Das ganze läuft noch etwas holprig, aber nach ein paar Versuchen hab ich's dann doch geschafft zu verbinden.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/01/aol-jabber-online.jpg" alt="aol-jabber-online.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Vorerst kann man nur anderen AIM-Usern Nachrichten schreiben, aber das wird wohl daran liegen dass der Server noch Beta ist.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Wäre schön wenn AOL XMPP weiter ausbauen würde, um nach dem Einsatz von <a href="http://www.notsorelevant.com/2007-02-15/openid-now-with-aol-support/">OpenID</a> einen weiteren großen Schritt in Richtung <a href="http://dataportability.org">DataPortability</a> zu gehen.<br/> Wenn jetzt auch noch Yahoo! und Microsoft auf den <em>Offenen Standard</em> umsteigen würden, könnte man in Zukunft vielleicht über einen Account mit ICQ, AIM, Y! Messenger und MSN Nutzern in Kontakt zu treten.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Weiterführende Links:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><a href="http://digg.com/software/AOL_ICQ_are_adopting_the_open_source_technology_Jabber">Die original Story bei DIGG</a></li>
</ul>
<!-- /wp:list -->