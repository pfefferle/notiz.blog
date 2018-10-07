---
ID: 1790
post_title: 'Microdata &#8211; wie Microformats bloß besser&#8230; (Teil 1)'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/08/10/microdata-wie-microformats-bloss-besser-teil-1/
published: true
post_date: 2009-08-10 22:30:32
---
<!-- wp:paragraph -->
<p>Der Inhalt wurde an die <a href="https://notiz.blog/2009/10/10/microdata-update-und-usability-studie/">neusten Änderungen der Microdata-Spezifikation</a> angepasst. Letztes Update 30.01.2010.
	<a href="https://notiz.blog/2011/06/26/microdata-wie-microformats-blos-besser-teil-2/">Microdata – wie Microformats bloß besser… (Teil 2)</a>: über "Namenskollisionen und Namespaces" und "Informationen Referenzieren"
</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Wie schon <a href="https://notiz.blog/2009/06/18/microdata-semantisches-html5/">erwähnt</a>, vereint Microdata die Vorzüge von <a href="http://rdfa.info">RDFa</a> und <a href="http://microformats.org">Microformats</a> in einem Standard... aber nicht nur das, Microdata (in Verbindung mit HTML5) bietet auch einige schicke Lösungen für diverse <a href="http://microformats.org/wiki/issues">Microformats-Problemchen</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>Das <em>abbr-design-pattern</em> oder das <em>value-class-pattern</em></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><strong>Microformats:</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Das <em><a href="http://microformats.org/wiki/abbr-design-pattern">abbr-design-pattern</a></em> ist bisher wohl das <a href="http://www.google.de/search?q=microformats+accessibility+abbr">umstrittenste Pattern</a> im <a href="http://microformats.org/wiki/Main_Page">Microformats-Wiki</a>. Grund für die Kritik an dem Pattern ist die etwas <a href="https://notiz.blog/2008/06/24/bbc-und-das-alte-haccessibility-problemchen/">unorthodoxe Verwendung</a> des <code>&lt;abbr></code> Tags um maschinenlesbare Meta-Informationen bereit zu stellen.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class="vevent">
  &lt;abbr class="dtstart" title="2007-10-05">October 5&lt;/abbr>
  ...
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Eine erste Alternative aus der Microformats-Community ist das <em><a href="http://microformats.org/wiki/value-class-pattern">value-class-pattern</a></em>, das zwar das Accessibility-Problem "behebt" aber noch lange keine Perfekte Lösung bietet.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class="vevent">
  &lt;span class='dtstart'>
    &lt;span class='value-title' title='2007-10-05'> &lt;/span>
    October 5
  &lt;/span>
  ...
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Der HTML-Code wird durch weitere Elemente unnötig aufgeblasen und das Pattern basiert auf teilweise leeren Elementen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Microdata/HTML5:</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In HTML5 gibt es dagegen ein spezielles Tag um Zeit und Datum sowohl user als auch maschinenlesbar zu machen.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div itemscope
  itemtype="http://microformats.org/profile/hcalendar">
  &lt;time itemprop="dtstart" datetime="2007-10-05">October 5&lt;/time>
  ...
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:heading {"level":4} -->
<h4>Reine Meta-Informationen</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><strong>Microformats:</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Eigentlich spricht es gegen die Prinzipien der Microformats-Idee, reine Metadaten zu verwenden: </p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote"><p>Visible data = more accurate data. By designing for humans first and making the data presentable (thus viewed and <em>verified</em> by humans), the data is inevitably more accurate, not only to begin with (as errors are easily/quickly noticed by those viewing the pages/sites), but over time as well; in that changes are noticed, and if data becomes out-of-date or obsolete, that's more likely to be noticed as well. This is in direct contrast to "side files" and invisible data like that contained in <code>&lt;meta></code> tags.<br/> -- <a href="http://microformats.org/wiki/principles#effects_of_principles">Tantek Çelik</a></p></blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>...aber <a href="http://microformats.org/wiki/geo">GEO-Daten</a> sind z.B. Informationen die der Benutzer nicht unbedingt sehen muss.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class="geo">
 &lt;span class="latitude">37.386013&lt;/span>
 &lt;span class="longitude">-122.082932&lt;/span>
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p><strong>Microdata/HTML5:</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In HTML5 gibt es für dieses Problem eine recht schicke Lösung: Laut der <a href="http://dev.w3.org/html5/spec/Overview.html#flow-content">Spezifikation</a> sind &lt;meta />-Tags im kompletten Quellcode (auch im <code>body</code>) erlaubt.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div itemscope 
 itemtype="http://microformats.org/profile/hcard#geo">
 &lt;meta itemprop="latitude" content="37.386013" />
 &lt;meta itemprop="longitude" content="-122.082932" />
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:heading {"level":4} -->
<h4>Fazit</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Selbst wenn sich <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/microdata.html">Microdata</a> (item und itemprop) nicht durchsetzen sollte, sind &lt;meta> und <a href="https://notiz.blog/2008/07/30/html5-is-made-for-microformats/">&lt;time></a> schon ein echter "Segen" für die <a href="http://microformats.org">Microformats-Community</a> :)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Im zweiten Teil nehm' ich mir das <a href="http://microformats.org/wiki/include-pattern">include-pattern</a> und das Problem der möglichen <a href="http://meiert.com/en/blog/20070913/microformats-and-pseudo-namespaces/">Namens</a>-<a href="http://meiert.com/en/blog/20090716/microformats-key-flaws/">Kollisionen</a> vor.<a href="https://notiz.blog/2011/06/26/microdata-wie-microformats-blos-besser-teil-2/">Microdata – wie Microformats bloß besser… (Teil 2)</a>: über "Namenskollisionen und Namespaces" und "Informationen Referenzieren"</p>
<!-- /wp:paragraph -->