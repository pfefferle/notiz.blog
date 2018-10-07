---
ID: 753
post_title: '&#8222;Zero Sign-On&#8220; mit OpenID und SSL'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/02/23/zero-sign-on-mit-openid-und-ssl/
published: true
post_date: 2008-02-23 20:19:42
---
<!-- wp:paragraph -->
<p>Bisher war für mich das klassische <a href="http://www.openid.net">OpenID</a> Prinzip (<a href="http://de.wikipedia.org/wiki/Single_Sign-On">Sigle Sign-On</a>) der einfachste und eleganteste Weg mich bei Seiten zu registrieren oder anzumelden... bisher! <a href="http://blog.cruisr.de/">Tobias</a> hat mich gestern auf einen <a href="http://drnicwilliams.com/2008/02/22/zero-sign-on-with-client-certificates/">Artikel</a> von Nic Williams aufmerksam gemacht in dem er beschreibt wie man mit <a href="http://myopenid.com">myOpenID</a> aus <a href="http://openid.net">OpenID</a> ein Zero Sign-On macht.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>myOpenID bietet neben dem klassischen Login auch SSL-Zertifikate:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Ihr Browser wird dieses Zertifikat nutzen, um Ihre Identität bei myOpenID, unter Verwendung von Transport Layer Security(TLS), zu bestätigen. Das Verwenden dieses Zertifikats vermeidet die Notwendigkeit empfindliche Daten, wie Ihr Passwort, eingeben zu müssen.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p><a href="http://www.mozilla.com/">Firefox</a> und <a href="http://www.microsoft.com/germany/windows/products/winfamily/ie/default.mspx">Internet Explorer</a> unterstützen diese Technik anscheinend auch schon seit den 90ern, es verwendet nur bisher keiner ;)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Die Einstellungen für myOpenID findet man unter "Kontoeinstellungen" -> "Authentication Settings".</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/02/zso-einstellungen.jpg" alt="zso-einstellungen.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Nach dem <em>Zertifikat erzeugen</em> wird das erstellte Zertifikat beim Firefox automatisch an die richtige Stelle kopiert (Bei Safari ist ein Schritt mehr notwendig).</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/02/zso-firefox-alert.jpg" alt="zso-firefox-alert.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Im Firefox "Zertifikat-Manager" sieht das ganze folgendermassen aus:</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/02/firefox-zertifikat-manager.jpg" alt="firefox-zertifikat-manager.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Eigentlich war es das jetzt auch schon... Beim nächsten anmelden mit OpenID wird man jetzt nur noch gefragt ob man für das nächste mal angemeldet bleiben will:</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/02/ssl-zertifikat-login.jpg" alt="ssl-zertifikat-login.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Gigantisch! Keine Ahnung warum sich diese Art der Authentifizierung noch nicht weiter herumgesprochen hat, ich jedenfalls hatte keine Ahnung dass myOpenID SSL-Zertifikate unterstützt... um ehrlich zu sein wusste ich bisher gar nichts über Client SSL-Zertifikate und dass nahezu alle Browser sie unterstützen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Also ab jetzt wirklich nie wieder Passwörter eintippen :)</p>
<!-- /wp:paragraph -->