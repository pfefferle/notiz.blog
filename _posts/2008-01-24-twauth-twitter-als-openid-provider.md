---
ID: 720
post_title: 'twauth: Twitter als OpenID Provider'
author: Matthias Pfefferle
post_date: 2008-01-24 09:10:25
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/01/24/twauth-twitter-als-openid-provider/
published: true
aktt_tweeted:
  - "1"
---
<a href="http://twauth.ianloic.com/">twauth</a> steht für twitter+authentication und ist ein, für mobile Geräte gedachter, <a href="http://www.openid.net">OpenID Provider</a> basierend auf <a href="http://twitter.com">Twitter</a>. Ausschlaggebend für den von <a href="http://ianloic.com/2008/01/13/a-simpler-mobile-openid-workflow/">Ian McKellar</a> entwickelten Dienst, war der von Chris Messina verfasste Blog-Post "<a href="http://factoryjoe.com/blog/2008/01/13/the-openid-mobile-experience/">The OpenID mobile experience</a>" in dem er seine eher negativen Erfahrungen mit bisherigen OpenID Providern auf mobilen Endgeräten beschreibt. 
Um den Dienst nutzen zu können sind folgende Schritte notwendig:
<ol><li>Man muss <em><a href="http://twitter.com/twauth">twauth</a></em> in seine <em>Follow</em>-Liste bei twitter hinzufügen.</li>
<li>Danach kann man <code>http://twauth.ianloic.com/&lt;twittername&gt;</code> als OpenID Identity einsetzen.</li></ol>

Ich habe das ganze mal mit der mobilen Version von Ma.gnolia (<a href="http://m.gnolia.com">m.gnolia.com</a>) und <a href="http://www.marketcircle.com/iphoney/">iPhoney</a>, einem iPhone Emulator für den Mac, durchgespielt.

<a href="http://www.flickr.com/photos/pfefferle/2215311980/" title="twauth login von Pfefferle bei Flickr"><img class="aligncenter" src="http://farm3.static.flickr.com/2274/2215311980_1283744b30_o.jpg" width="480" height="256" alt="twauth login" /></a>

Nach dem Eingeben der OpenID <abbr title="Uniform Resource Locator">URL</abbr> wird man automatisch auf die Loginseite von twauth geleitet. Die Authentifizierung findet nicht wie im klassischen Sinn, über Benutzername und Passwort, statt sondern über eine 5 Stellige Zahl die man als "Private Message" via Twitter bekommt.

<a href="http://www.flickr.com/photos/pfefferle/2215311826/" title="twauth auth von Pfefferle bei Flickr"><img class="aligncenter" src="http://farm3.static.flickr.com/2123/2215311826_042d534c27_o.jpg" width="480" height="256" alt="twauth auth" /></a>

Danach noch die entsprechende <abbr title="Uniform Resource Locator">URL</abbr> (in diesem Fall Ma.gnolia) bestätigen und fertig. 

<a href="http://www.flickr.com/photos/pfefferle/2214518657/" title="twauth confirm von Pfefferle bei Flickr"><img class="aligncenter" src="http://farm3.static.flickr.com/2120/2214518657_594e31028c_o.jpg" width="480" height="256" alt="twauth confirm" /></a>

Leider muss man nach der Anmeldung über twauth seine kompletten Daten per Hand ausfüllen, da twauth bisher weder <abbr title="Simple Registration Extension">SREG</abbr> noch <abbr title="Attribute Exchange">AX</abbr> unterstützt. Außerdem muss man den oben beschriebenen Vorgang bei jeder Anmeldung wiederholen, da twauth noch kein Session-Management unterstützt.

Genau genommen bietet twauth also noch keine wirkliche Vereinfachung des Registrier- und Anmelde-Prozessen (es dauert im Gegenteil wahrscheinlich sogar länger), ich mag jedoch die Idee mit Twitter und der <abbr title="Private Message">PM</abbr> sehr und hoffe dass sich bei twauth in Zukunft noch einiges tun wird.
Mit SREG und einem simplen Session Management würde twauth schon einen sehr guten mobilen OpenID Provider abgeben.

<!--more-->
Hier nochmal ein kleiner Screen-Cast wie es funktioniert:

<object type="application/x-shockwave-flash" style="width:425px; height:350px" data="http://www.youtube.com/v/KJACymflbxk"><param name="movie" value="http://www.youtube.com/v/KJACymflbxk"></param></object>