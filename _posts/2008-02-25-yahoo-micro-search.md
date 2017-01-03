---
ID: 758
post_title: Yahoo! Micro Search
author: Matthias Pfefferle
post_date: 2008-02-25 21:46:33
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/02/25/yahoo-micro-search/
published: true
aktt_tweeted:
  - "1"
---
<img class="aligncenter" src="http://notiz.blog/wp-content/uploads/2008/02/microsearch-logo.jpg" alt="microsearch-logo.jpg" border="0" width="284" height="46" />

So, endlich komm ich neben den ganzen <a href="http://notiz.blog/tag/dataportability/">DataPortability</a> und <a href="http://notiz.blog/tag/openid/">OpenID</a> News auch mal wieder zu meinen sehr geschätzten Microformats ;)

<a href="http://research.yahoo.com/Yahoo_Research_Barcelona">Yahoo! Research Barcelona</a> bastelt mit "<a href="http://www.yr-bcn.es/demos/microsearch/">Yahoo! Micro Search</a>" an einer <em>Social/Semantic Search</em> Engine. Yahoo! Micro Search ist aber keine reine Microformats Suche wie z.B. die Technorati "<a href="http://kitchen.technorati.com/search/">Microformats Search</a>" sondern unterstützt (wie die <a href="http://code.google.com/apis/socialgraph/">Social Graph API</a>) auch <abbr title="Resource Description Framework using Attributes">RDFa</abbr>, über <code>&lt;link rel="me" /&gt;</code> verlinkte <abbr title="Resource Description Framework">RDF</abbr> Dateien wie z.B. <a href="http://xmlns.com/foaf/spec/"><abbr title="Friend of a Friend">FoaF</abbr></a> und demnächst soll auch noch <a href="http://www.w3.org/TR/grddl/"><abbr title="Gleaning Resource Descriptions from Dialects of Languages">GRDDL</abbr></a> dazu kommen (bin mal gespannt wie das aussehen soll).

Der Aufbau der Suchergebnisse ist (zumindest im Hauptteil) eher klassisch wie bei <a href="http://www.google.de">Google</a> oder <a href="http://www.yahoo.de">Yahoo!</a> aufgebaut.

<img class="aligncenter" src="http://notiz.blog/wp-content/uploads/2008/02/yahoo-search-results.jpg" alt="yahoo-search-results.jpg" border="0" width="480" height="237" />

Im oberen Teil der Sidebar werden gefundene <a href="http://microformats.org/wiki/geo">GEO-Daten</a> direkt auf einer Yahoo Map dargestellt. Die unten abgebildeten Orte wurden z.B. in meinem <a href="http://plazes.com/users/pfefferle">Plazes Account</a> gefunden.

<img class="aligncenter" src="http://notiz.blog/wp-content/uploads/2008/02/yahoo-search-results-map.jpg" alt="yahoo-search-results-map.jpg" border="0" width="480" height="286" />

Darunter sollen wohl gefundene <a href="http://microformats.org/wiki/hCal">hCalendar</a>-Events mit Hilfe der <a href="http://simile.mit.edu/timeline/">Smile Timeline</a> angezeigt werden, das habe ich aber leider nicht ausprobieren können... meine war immer leer, ich hoffe das liegt nicht an mir ;)


Wo bei Google "nur" die Anzahl der Suchtreffer zu einem Suchbegriff angezeigt werden, listet die Micro Search genau auf wie viele davon Profile (z.B. vCards/hCards) oder Events (z.B. hCalendar) sind.

<img class="aligncenter" src="http://notiz.blog/wp-content/uploads/2008/02/micro-search-details.jpg" alt="micro-search-details.jpg" border="0" width="480" height="30" />

Fazit: "Yahoo! Micro Search" dient wohl in erster Linie dazu Google einen Schritt voraus zu sein und ein Pendant zu der "Social Graph API" zu schaffen... und wenn schon, ich mag die Idee. Man sollte sich in Zukunft nur im klaren sein, dass arglos veröffentlichte Microformats demnächst auch alle gefunden (und meist auch dessen Autor zugeordnet) werden können...

Weiterführende Links:
<ul><li>Yahoo! Research Barcelona <a href="http://www.yr-bcn.es/dokuwiki/doku.php?id=microsearch">DokuWiki</a></li>
<li><a href="http://www.sitepoint.com/blogs/2008/02/22/structured-data-set-to-take-on-google/">Structured data - set to take on Google</a></li></ul>