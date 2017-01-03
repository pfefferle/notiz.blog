---
ID: 2059
post_title: 'Microdata: Update und Usability-Studie'
author: Matthias Pfefferle
post_date: 2009-10-10 17:20:50
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/10/10/microdata-update-und-usability-studie/
published: true
---
<em>Endlich denkt beim Thema "Usability" auch mal jemand an die Entwickler :)</em>

Google hat über die letzten Wochen eine <a href="http://blog.whatwg.org/usability-testing-html5">Usability-Studie zu Microdata</a> durchgeführt und die <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/microdata.html">Spezifikation</a> wurde auch gleich entsprechend der Ergebnisse angepasst.

<pre>&lt;address <strong>itemscope</strong> <strong>itemtype</strong>="http://microformats.org/profile/hcard"&gt;
 &lt;strong <strong>itemprop</strong>="fn"&gt;Alfred Person&lt;/strong&gt;
 &lt;span <strong>itemprop</strong>="adr" <strong>itemscope</strong>&gt;
  &lt;span <strong>itemprop</strong>="street-address"&gt;1600 Amphitheatre Parkway&lt;/span&gt; &lt;br&gt;
  &lt;span <strong>itemprop</strong>="street-address"&gt;Building 43, Second Floor&lt;/span&gt; &lt;br&gt;
  &lt;span <strong>itemprop</strong>="locality"&gt;Mountain View&lt;/span&gt;,
  &lt;span <strong>itemprop</strong>="region"&gt;CA&lt;/span&gt; &lt;span itemprop="postal-code"&gt;94043&lt;/span&gt;
 &lt;/span&gt;
&lt;/address&gt;</pre>

Die Änderungen:

<ul><li>Aus <strong><code>item</code></strong> wird <strong><code>itemscope</code></strong>.</li>
<li>Der Typ wird über <strong><code>itemtype</code></strong> und nicht mehr über <strong><code>item</code></strong> bzw. <strong><code>itemscope</code></strong> angegeben.</li>
<li>Das Attribut <strong><code>itemid</code></strong> wurde eingeführt, um z.B. auf ISBN-Nummer zu verweisen <strong><code>itemid="urn:isbn:0-330-34032-8"</code></strong>.</li></ul>

Über den neuen <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/semantics.html#itemfor">HTML-Tag</a> <strong><code>&lt;itemref /&gt;</code></strong> (alternativ: <strong><code>&lt;itemfor /&gt;</code></strong>) werde ich im zweiten Teil von "<em>Microdata – wie Microformats bloß besser…</em>" eingehen (<a href="http://notiz.blog/2009/08/10/microdata-wie-microformats-bloss-besser-teil-1/">zum ersten Teil</a>).

Jetzt muss ich nur noch meine alten Artikel zu Microdata anpassen... das hat man nun davon, wenn man über Drafts berichtet ;)