---
ID: 1790
post_title: 'Microdata &#8211; wie Microformats bloß besser&#8230; (Teil 1)'
author: Matthias Pfefferle
post_date: 2009-08-10 22:30:32
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/08/10/microdata-wie-microformats-bloss-besser-teil-1/
published: true
---
<div class="alert alert-info">Der Inhalt wurde an die <a href="http://notiz.blog/2009/10/10/microdata-update-und-usability-studie/">neusten Änderungen der Microdata-Spezifikation</a> angepasst. Letztes Update 30.01.2010.</div>

<div class="alert alert-info"><a href="http://notiz.blog/2011/06/26/microdata-wie-microformats-blos-besser-teil-2/">Microdata – wie Microformats bloß besser… (Teil 2)</a>: über "Namenskollisionen und Namespaces" und "Informationen Referenzieren"</div>

Wie schon <a href="http://notiz.blog/2009/06/18/microdata-semantisches-html5/">erwähnt</a>, vereint Microdata die Vorzüge von <a href="http://rdfa.info">RDFa</a> und <a href="http://microformats.org">Microformats</a> in einem Standard... aber nicht nur das, Microdata (in Verbindung mit HTML5) bietet auch einige schicke Lösungen für diverse <a href="http://microformats.org/wiki/issues">Microformats-Problemchen</a>.

<h4>Das <em>abbr-design-pattern</em> oder das <em>value-class-pattern</em></h4>

<strong>Microformats:</strong>

Das <em><a href="http://microformats.org/wiki/abbr-design-pattern">abbr-design-pattern</a></em> ist bisher wohl das <a href="http://www.google.de/search?q=microformats+accessibility+abbr">umstrittenste Pattern</a> im <a href="http://microformats.org/wiki/Main_Page">Microformats-Wiki</a>. Grund für die Kritik an dem Pattern ist die etwas <a href="http://notiz.blog/2008/06/24/bbc-und-das-alte-haccessibility-problemchen/">unorthodoxe Verwendung</a> des <code>&lt;abbr&gt;</code> Tags um maschinenlesbare Meta-Informationen bereit zu stellen.

<pre>&lt;div class="vevent"&gt;
  &lt;abbr class="dtstart" title="<strong>2007-10-05</strong>"&gt;October 5&lt;/abbr&gt;
  ...
&lt;/div&gt;</pre>

Eine erste Alternative aus der Microformats-Community ist das <em><a href="http://microformats.org/wiki/value-class-pattern">value-class-pattern</a></em>, das zwar das Accessibility-Problem "behebt" aber noch lange keine Perfekte Lösung bietet.

<pre>&lt;div class="vevent"&gt;
  &lt;span class='dtstart'&gt;
    &lt;span class='value-title' title='<strong>2007-10-05</strong>'&gt; &lt;/span&gt;
    October 5
  &lt;/span&gt;
  ...
&lt;/div&gt;</pre>

Der HTML-Code wird durch weitere Elemente unnötig aufgeblasen und das Pattern basiert auf teilweise leeren Elementen.

<strong>Microdata/HTML5:</strong>

In HTML5 gibt es dagegen ein spezielles Tag um Zeit und Datum sowohl user als auch maschinenlesbar zu machen.

<pre>&lt;div itemscope
  itemtype="http://microformats.org/profile/hcalendar"&gt;
  &lt;time itemprop="dtstart" datetime="2007-10-05"&gt;October 5&lt;/time&gt;
  ...
&lt;/div&gt;</pre>

<h4>Reine Meta-Informationen</h4>

<strong>Microformats:</strong>

Eigentlich spricht es gegen die Prinzipien der Microformats-Idee, reine Metadaten zu verwenden: 

<blockquote>Visible data = more accurate data. By designing for humans first and making the data presentable (thus viewed and <i>verified</i> by humans), the data is inevitably more accurate, not only to begin with (as errors are easily/quickly noticed by those viewing the pages/sites), but over time as well; in that changes are noticed, and if data becomes out-of-date or obsolete, that's more likely to be noticed as well.  This is in direct contrast to "side files" and invisible data like that contained in <code>&lt;meta&gt;</code> tags.
-- <a href="http://microformats.org/wiki/principles#effects_of_principles">Tantek Çelik</a></blockquote>

...aber <a href="http://microformats.org/wiki/geo">GEO-Daten</a> sind z.B. Informationen die der Benutzer nicht unbedingt sehen muss.

<pre>&lt;div class="geo"&gt;
 &lt;span class="latitude"&gt;37.386013&lt;/span&gt;
 &lt;span class="longitude"&gt;-122.082932&lt;/span&gt;
&lt;/div&gt;</pre>

<strong>Microdata/HTML5:</strong>

In HTML5 gibt es für dieses Problem eine recht schicke Lösung: Laut der <a href="http://dev.w3.org/html5/spec/Overview.html#flow-content">Spezifikation</a> sind &lt;meta /&gt;-Tags im kompletten Quellcode (auch im <code>body</code>) erlaubt.

<pre>&lt;div itemscope 
 itemtype="http://microformats.org/profile/hcard#geo"&gt;
 &lt;meta itemprop="latitude" content="37.386013" /&gt;
 &lt;meta itemprop="longitude" content="-122.082932" /&gt;
&lt;/div&gt;</pre>

<h4>Fazit</h4>

Selbst wenn sich <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/microdata.html">Microdata</a> (item und itemprop) nicht durchsetzen sollte, sind &lt;meta&gt; und <a href="http://notiz.blog/2008/07/30/html5-is-made-for-microformats/">&lt;time&gt;</a> schon ein echter "Segen" für die <a href="http://microformats.org">Microformats-Community</a> :)

Im zweiten Teil nehm' ich mir das <a href="http://microformats.org/wiki/include-pattern">include-pattern</a> und das Problem der möglichen <a href="http://meiert.com/en/blog/20070913/microformats-and-pseudo-namespaces/">Namens</a>-<a href="http://meiert.com/en/blog/20090716/microformats-key-flaws/">Kollisionen</a> vor.

<div class="info"><a href="http://notiz.blog/2011/06/26/microdata-wie-microformats-blos-besser-teil-2/">Microdata – wie Microformats bloß besser… (Teil 2)</a>: über "Namenskollisionen und Namespaces" und "Informationen Referenzieren"</div>