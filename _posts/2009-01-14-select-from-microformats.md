---
ID: 1389
post_title: 'SELECT * FROM microformats'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/01/14/select-from-microformats/
published: true
post_date: 2009-01-14 09:21:31
---
<!-- wp:paragraph -->
<p><abbr title="Yahoo! Query Language">YQL</abbr> (<a href="http://developer.yahoo.com/yql/">Yahoo! Query Language</a>) ist eine Art <abbr title="Structured Query Language"><a href="http://de.wikipedia.org/wiki/SQL">SQL</a></abbr>-Sprache um HTML- oder XML-Inhalte abzufragen. Oder wie es <a href="http://netzwertig.com/2008/12/11/yahoo-yql-das-web-als-datenbank/">Markus Spath</a> so schön formuliert hat:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Yahoo verwandelt das Web mit der Yahoo Query Language in eine gigantische Datenbank.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Wer bisher schon etwas Erfahrung mit z.B. MySQL gemacht hat, sollte auch mit YQL keine weiteren Probleme haben. Ein Beispiel:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>SELECT * FROM feed WHERE url='https://notiz.blog/feed/'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Übersetzt: Gib mir (<code>SELECT</code>) alle Inhalte (<code>*</code>) des RSS-Feeds (<code>FROM feed</code>) die unter der URL: <code>https://notiz.blog</code> zu finden sind (<code>url='https://notiz.blog/feed/'</code>).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Das Spannende (weshalb ich es überhaupt erst erwähne) an YQL ist aber der gerade <a href="http://developer.yahoo.net/blog/archives/2009/01/yql_with_microformats.html">angekündigte <em>Microformats Support</em></a>, der die <em>Query Language</em> zu einem vollwertigen <em>Microformats Parser</em> macht.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Über den Befehl:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>SELECT * FROM microformats WHERE url='https://notiz.blog/kontakt/'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>werden Beispielsweise alle <em>Microformats</em> meiner Kontaktseite geparst und mir in einem standardisierten <abbr title="Extensible Markup Language">XML</abbr> oder <abbr title="JavaScript Object Notation">JSON</abbr> Format bereit gestellt.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Großartig! Was Yahoo! im Zuge der <a href="http://developer.yahoo.com/yos/intro/">Open Strategy</a> mit Systemen wie dem <a href="http://developer.yahoo.com/searchmonkey/">SearchMonkey</a> oder YQL geschaffen hat, ist ein echter Traum für jeden Webentwickler und <em>Open Standards Evangelist</em>! Ich hoffe einer der nächste Schritte wird sein, die YQL (als Alternative zu XSLT) auch in den <a href="http://developer.yahoo.com/searchmonkey/">SearchMonkey</a> zu integrieren.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ach ja... die <a href="http://developer.yahoo.com/yql/console/">YQL-Console</a> bietet übrigens eine schöne Alternative zur <a href="http://developer.yahoo.com/yql/guide/">YQL-Dokumentation</a>... einfach mal einige bekannte SQL-Befehle eingeben und schauen was passiert (so ähnlich habe ich mir damals auch HTML beigebracht) ;)</p>
<!-- /wp:paragraph -->