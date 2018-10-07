---
ID: 2059
post_title: 'Microdata: Update und Usability-Studie'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/10/10/microdata-update-und-usability-studie/
published: true
post_date: 2009-10-10 17:20:50
---
<!-- wp:paragraph -->
<p><em>Endlich denkt beim Thema "Usability" auch mal jemand an die Entwickler :)</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Google hat über die letzten Wochen eine <a href="http://blog.whatwg.org/usability-testing-html5">Usability-Studie zu Microdata</a> durchgeführt und die <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/microdata.html">Spezifikation</a> wurde auch gleich entsprechend der Ergebnisse angepasst.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;address itemscope itemtype="http://microformats.org/profile/hcard">
 &lt;strong itemprop="fn">Alfred Person&lt;/strong>
 &lt;span itemprop="adr" itemscope>
  &lt;span itemprop="street-address">1600 Amphitheatre Parkway&lt;/span> &lt;br>
  &lt;span itemprop="street-address">Building 43, Second Floor&lt;/span> &lt;br>
  &lt;span itemprop="locality">Mountain View&lt;/span>,
  &lt;span itemprop="region">CA&lt;/span> &lt;span itemprop="postal-code">94043&lt;/span>
 &lt;/span>
&lt;/address></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Die Änderungen:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li>Aus <strong><code>item</code></strong> wird <strong><code>itemscope</code></strong>.</li>
	<li>Der Typ wird über <strong><code>itemtype</code></strong> und nicht mehr über <strong><code>item</code></strong> bzw. <strong><code>itemscope</code></strong> angegeben.</li>
	<li>Das Attribut <strong><code>itemid</code></strong> wurde eingeführt, um z.B. auf ISBN-Nummer zu verweisen <strong><code>itemid="urn:isbn:0-330-34032-8"</code></strong>.</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Über den neuen <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/semantics.html#itemfor">HTML-Tag</a> <strong><code>&lt;itemref /></code></strong> (alternativ: <strong><code>&lt;itemfor /></code></strong>) werde ich im zweiten Teil von "<em>Microdata – wie Microformats bloß besser…</em>" eingehen (<a href="https://notiz.blog/2009/08/10/microdata-wie-microformats-bloss-besser-teil-1/">zum ersten Teil</a>).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Jetzt muss ich nur noch meine alten Artikel zu Microdata anpassen... das hat man nun davon, wenn man über Drafts berichtet ;)</p>
<!-- /wp:paragraph -->