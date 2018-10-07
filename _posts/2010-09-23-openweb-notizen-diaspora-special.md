---
ID: 3212
post_title: 'OpenWeb-Notizen: Diaspora Special'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2010/09/23/openweb-notizen-diaspora-special/
published: true
post_date: 2010-09-23 23:10:09
---
<!-- wp:paragraph -->
<p><strong>Das</strong> (OpenWeb-) Thema, welches die letzten Tage die meisten <a href="http://de.wikipedia.org/wiki/Netizen">Netizens</a> beschäftigt hat war wohl die Veröffentlichung des Diaspora-Codes. Irgendwie kam das Tool dabei nicht ganz so gut weg. Hier ein paar Meinungen aus deutschen Quellen:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Lange hat es nicht gedauert, bis die ersten sicherheitsrelevanten Lücken aufgedeckt wurden. Wie The Register meldet, haben Experten bereits Möglichkeiten entdeckt fremde Accounts zu übernehmen, ohne Erlaubnis neue Kontakte aufzubauen oder Fotos zu löschen.</p>
	<p>Entwickler haben sich den Code bereits genauer angesehen und sind enttäuscht: Diaspora ist eine einfache Rails App, mit der man Fotos hochladen kann“, zitiert Mashable den Entwickler J. Chris Anderson. Daraus könne man schließen, dass die Codebasis keinesfalls ausreicht, um daraus in den nächsten Monaten einen echten Konkurrenten für Facebook zu machen.</p><cite><strong>t3n</strong> - <a href="http://t3n.de/news/diaspora-welche-chancen-hat-dezentrale-279997/">Welche Chancen hat die dezentrale Facebook-Alternative?</a></cite></blockquote>
<!-- /wp:quote -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Nun wurde Diaspora mit Ruby on Rails geschrieben zusätzlich braucht es eine Mongo Database – zwei dinge die jetzt nicht jeder installiert hat – oder ums spezifizieren – so gut wie niemand installiert hat. Das sind schonmal zwei Hürden die so gleich vorneweg mal 80% aller Hostingoptionen ausschliessen. Man braucht dafür dann schon ein Hostingprovider der einen Kram installieren lässt was bei den meisten Shared Massen Hostern(tm) nicht funktioniert – oder man hat nen eigenen Server irgendwo stehen.</p><cite><strong>Blog Rebellen</strong> - <a href="http://blog.rebellen.info/2010/09/17/diaspora-ein-erster-eindruck/">Diaspora – Ein erster Eindruck</a></cite></blockquote>
<!-- /wp:quote -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Die eigenen Server stehen übrigens auch einer großen Verbreitung von Diaspora entgegen. Denn wie viele an Social Networking interessierte Nutzer gibt es, die einen eigenen Server betreiben? Selbst wenn es Hoster in der Art von Wordpress.com geben sollte, dürfte die Nutzerzahl begrenzt bleiben.</p>
	<p>Nur mal so: Jeder kann einen Mail Server betreiben, jeder kann OpenID Provider werden. Frage: Wie viele Leute betreiben einen eigenen Mail Server und wie viele Leute sind ihr eigener OpenID Provider? Genau.</p><cite> <strong>Neunetz</strong> - <a href="http://www.neunetz.com/2010/09/16/diaspora-automatisch-gut-dank-open-source/#comment-78099096">Carsten Pötter in den Kommentaren</a></cite></blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Neben den Sicherheitsmängeln und den anspruchsvollen "Server Requirements" gibt es aber vor allem ein Problem: Diaspora basiert auf den gleichen Ideen wie z.B. auch <a href="http://noserub.com">Noserub</a> oder <a href="http://status.net">StatusNET</a> und übernimmt auch all deren Probleme. Um einen Kontakt einer anderen <em>Diaspora-Node</em> hinzufügen zu können muss man seinen <em>Identifier</em> kennen (z.B. <code>pfefferle@diaspora.t3n-magazin.de</code>)... ein Problem mit dem beispielsweise die <em>OpenID-Community</em> schon seit Jahren kämpft. Des Weiteren spricht Diaspora eine eigene Sprache und kann nicht mit funktionierenden, etablierten und dezentralen Systemen (basierend auf offenen Standards) wie <em>StatusNET</em>, verbunden werden!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Technische Mittel ein dezentrales Netzwerk zu erstellen gibt es genug: <a href="http://ostatus.org"><em>OStatus</em></a>, <a href="http://www.salmon-protocol.org/"><em>Salmon Protocol</em></a>, <a href="http://code.google.com/p/pubsubhubbub/"><em>Pubsubhubbub</em></a>, <a href="http://openid.net"><em>OpenID</em></a> uvm. (von denen Diaspora übrigens keine einzige nutzt) und wir brauchen wirklich nicht noch eine neue offene Plattform... viel wichtiger wäre doch die bestehenden Netzwerke untereinander zu verbinden oder einen Weg zu finden, dem normalen <em>Surfer</em> das Thema <em>Identifier</em> näher zu bringen...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ich will keine Software installieren müssen um dann nur User der gleichen Software <em>folgen</em> zu können, ich will Google-User mit meinem Twitter-Account verbinden! Ich will meine Bilder bei Flickr hoch laden und bei MySpace referenzieren. Ein dezentrales "<a href="http://federatedsocialweb.net/">federated social web</a>" bedeutet für mich, das verbinden von verschiedenen Diensten, anstatt einer offenen <strong>Kopie</strong> von Facebook!</p>
<!-- /wp:paragraph -->