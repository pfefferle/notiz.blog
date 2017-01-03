---
ID: 753
post_title: '&#8222;Zero Sign-On&#8220; mit OpenID und SSL'
author: Matthias Pfefferle
post_date: 2008-02-23 20:19:42
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/02/23/zero-sign-on-mit-openid-und-ssl/
published: true
aktt_tweeted:
  - "1"
---
Bisher war für mich das klassische <a href="http://www.openid.net">OpenID</a> Prinzip (<a href="http://de.wikipedia.org/wiki/Single_Sign-On">Sigle Sign-On</a>) der einfachste und eleganteste Weg mich bei Seiten  zu registrieren oder anzumelden... bisher! <a href="http://blog.cruisr.de/">Tobias</a> hat mich gestern auf einen <a href="http://drnicwilliams.com/2008/02/22/zero-sign-on-with-client-certificates/">Artikel</a> von Nic Williams aufmerksam gemacht in dem er beschreibt wie man mit <a href="http://myopenid.com">myOpenID</a> aus <a href="http://openid.net">OpenID</a> ein Zero Sign-On macht.

myOpenID bietet neben dem klassischen Login auch SSL-Zertifikate:

<blockquote cite="https://www.myopenid.com/settings_authentication">Ihr Browser wird dieses Zertifikat nutzen, um Ihre Identität bei myOpenID, unter Verwendung von Transport Layer Security(TLS), zu bestätigen. Das Verwenden dieses Zertifikats vermeidet die Notwendigkeit empfindliche Daten, wie Ihr Passwort, eingeben zu müssen.</blockquote>

<a href="http://www.mozilla.com/">Firefox</a> und <a href="http://www.microsoft.com/germany/windows/products/winfamily/ie/default.mspx">Internet Explorer</a> unterstützen diese Technik anscheinend auch schon seit den 90ern, es verwendet nur bisher keiner ;)

Die Einstellungen für myOpenID findet man unter "Kontoeinstellungen" -&gt; "Authentication Settings".

<img class="aligncenter" src="http://notiz.blog/wp-content/uploads/2008/02/zso-einstellungen.jpg" alt="zso-einstellungen.jpg" border="0" width="480" height="266" />

Nach dem <em>Zertifikat erzeugen</em> wird das erstellte Zertifikat beim Firefox automatisch an die richtige Stelle kopiert (Bei Safari ist ein Schritt mehr notwendig).

<img class="aligncenter" src="http://notiz.blog/wp-content/uploads/2008/02/zso-firefox-alert.jpg" alt="zso-firefox-alert.jpg" border="0" width="480" height="165" />

Im Firefox "Zertifikat-Manager" sieht das ganze folgendermassen aus:

<img class="aligncenter" src="http://notiz.blog/wp-content/uploads/2008/02/firefox-zertifikat-manager.jpg" alt="firefox-zertifikat-manager.jpg" border="0" width="480" height="216" />

Eigentlich war es das jetzt auch schon... Beim nächsten anmelden mit OpenID wird man jetzt nur noch gefragt ob man für das nächste mal angemeldet bleiben will:

<img class="aligncenter" src="http://notiz.blog/wp-content/uploads/2008/02/ssl-zertifikat-login.jpg" alt="ssl-zertifikat-login.jpg" border="0" width="480" height="113" />

Gigantisch! Keine Ahnung warum sich diese Art der Authentifizierung noch nicht weiter herumgesprochen hat, ich jedenfalls hatte keine Ahnung dass myOpenID SSL-Zertifikate unterstützt... um ehrlich zu sein wusste ich bisher gar nichts über Client SSL-Zertifikate und dass nahezu alle Browser sie unterstützen.

Also ab jetzt wirklich nie wieder Passwörter eintippen :)