---
ID: 720
post_title: 'twauth: Twitter als OpenID Provider'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/01/24/twauth-twitter-als-openid-provider/
published: true
post_date: 2008-01-24 09:10:25
---
<!-- wp:paragraph -->
<p><a href="http://twauth.ianloic.com/">twauth</a> steht für twitter+authentication und ist ein, für mobile Geräte gedachter, <a href="http://www.openid.net">OpenID Provider</a> basierend auf <a href="http://twitter.com">Twitter</a>. Ausschlaggebend für den von <a href="http://ianloic.com/2008/01/13/a-simpler-mobile-openid-workflow/">Ian McKellar</a> entwickelten Dienst, war der von Chris Messina verfasste Blog-Post "<a href="http://factoryjoe.com/blog/2008/01/13/the-openid-mobile-experience/">The OpenID mobile experience</a>" in dem er seine eher negativen Erfahrungen mit bisherigen OpenID Providern auf mobilen Endgeräten beschreibt.<br/>Um den Dienst nutzen zu können sind folgende Schritte notwendig:</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol>
	<li>Man muss <em><a href="http://twitter.com/twauth">twauth</a></em> in seine <em>Follow</em>-Liste bei twitter hinzufügen.</li>
	<li>Danach kann man <code>http://twauth.ianloic.com/&lt;twittername></code> als OpenID Identity einsetzen.</li>
</ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Ich habe das ganze mal mit der mobilen Version von Ma.gnolia (<a href="http://m.gnolia.com">m.gnolia.com</a>) und <a href="http://www.marketcircle.com/iphoney/">iPhoney</a>, einem iPhone Emulator für den Mac, durchgespielt.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","linkDestination":"custom"} -->
<figure class="wp-block-image aligncenter"><a href="http://www.flickr.com/photos/pfefferle/2215311980/"><img src="http://farm3.static.flickr.com/2274/2215311980_1283744b30_o.jpg" alt="twauth login"/></a></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Nach dem Eingeben der OpenID <abbr title="Uniform Resource Locator">URL</abbr> wird man automatisch auf die Loginseite von twauth geleitet. Die Authentifizierung findet nicht wie im klassischen Sinn, über Benutzername und Passwort, statt sondern über eine 5 Stellige Zahl die man als "Private Message" via Twitter bekommt.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","linkDestination":"custom"} -->
<figure class="wp-block-image aligncenter"><a href="http://www.flickr.com/photos/pfefferle/2215311826/"><img src="http://farm3.static.flickr.com/2123/2215311826_042d534c27_o.jpg" alt="twauth auth"/></a></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Danach noch die entsprechende <abbr title="Uniform Resource Locator">URL</abbr> (in diesem Fall Ma.gnolia) bestätigen und fertig.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","linkDestination":"custom"} -->
<figure class="wp-block-image aligncenter"><a href="http://www.flickr.com/photos/pfefferle/2214518657/"><img src="http://farm3.static.flickr.com/2120/2214518657_594e31028c_o.jpg" alt="twauth confirm"/></a></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Leider muss man nach der Anmeldung über twauth seine kompletten Daten per Hand ausfüllen, da twauth bisher weder <abbr title="Simple Registration Extension">SREG</abbr> noch <abbr title="Attribute Exchange">AX</abbr> unterstützt. Außerdem muss man den oben beschriebenen Vorgang bei jeder Anmeldung wiederholen, da twauth noch kein Session-Management unterstützt.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Genau genommen bietet twauth also noch keine wirkliche Vereinfachung des Registrier- und Anmelde-Prozessen (es dauert im Gegenteil wahrscheinlich sogar länger), ich mag jedoch die Idee mit Twitter und der <abbr title="Private Message">PM</abbr> sehr und hoffe dass sich bei twauth in Zukunft noch einiges tun wird.<br/>Mit SREG und einem simplen Session Management würde twauth schon einen sehr guten mobilen OpenID Provider abgeben.</p>
<!-- /wp:paragraph -->