---
ID: 1003
post_title: HTML5 is made for Microformats
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/07/30/html5-is-made-for-microformats/
published: true
post_date: 2008-07-30 20:34:52
---
<!-- wp:paragraph -->
<p>Naja, nicht wirklich aber immerhin hat es <a href="http://www.w3.org/TR/xhtml-rdfa-primer/">RDFa</a> bis dato nicht in die <a href="http://www.w3.org/html/wg/html5/">HTML5 Spezifikation</a> geschafft. Es gibt zwar einen <a href="http://www.w3.org/2007/03/HTML-WG-charter.html#deliverables">Milestone</a>...</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote"><p>The HTML WG is encouraged to provide a mechanism to permit independently developed vocabularies such as Internationalization Tag Set (ITS), Ruby, and RDFa to be mixed into HTML documents.</p></blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>...aber wer weiß wie lange das noch dauert. Das heißt wohl, dass die Microformats noch eine gewisse Zeit lang als Übergangslösung her halten müssen. Aber das ist ne andere Geschichte...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Eigentlich wollte ich auf zwei HTML5 - Elemente eingehen, die eine schicke Alternative zu den bisherigen (in <a href="http://microformats.org/wiki/geo">vielen</a> <a href="http://microformats.org/wiki/hCal">Microformats</a> verwendeten) <a href="http://microformats.org/wiki/abbr-design-pattern">abbr-design-pattern</a> bietet.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>Der &lt;time />-Tag</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Das <code><a href="http://www.w3.org/html/wg/html5/#time">time</a></code> Element ermöglicht das kennzeichnen eines Datums in z.B. Blogposts o.Ä.</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote"><p>The primary use cases for these elements are for marking up publication dates e.g. in blog entries, and for marking event dates in hCalendar markup.</p></blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Also:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;time datetime="2006-09-23">a Saturday&lt;/time></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>statt:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;abbr title="2006-09-23">a Saturday&lt;/abbr></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Ein <a href="http://microformats.org/wiki/hCal">hCalendar</a> könnte dann so aussehen:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class="vevent">
  &lt;span class="summary">event title&lt;/span>
  &lt;time datetime="2006-09-23" class="dtstart dtend">a Saturday&lt;/time>
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:heading {"level":4} -->
<h4>Custom data attributes (data-)</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Ein <em>custom data attribute</em> ist ein frei benutzbares Attribut um Elemente mit <a href="http://de.wikipedia.org/wiki/Metadaten">Metadaten</a> anzureichern. Die einzige Vorgabe ist, dass es mit <code>data-</code> beginnen muss. Ein Beispiel:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class="monkey" data-arms="2"
     data-legs="2" data-race="chimp">
  Cheetah
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Ideal auch als <code>&lt;abbr /></code>-Ersatz bei z.B. dem <a href="http://microformats.org/wiki/geo">Geo-Microformat</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Also:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class="geo" data-latitude="49.5483" data-longitude="8.6661">Weinheim&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>statt:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;abbr class="geo" title="49.5483;8.6661">Weinheim&lt;/abbr></code></pre>
<!-- /wp:code -->

<!-- wp:heading {"level":4} -->
<h4>Fazit</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>(X)HTML (egal ob XHTML2 mit RDFa oder X/HTML5) wird also definitiv ein semantisches Feuerwerk, ganz im Sinne von Tim Berners Lee...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ich freu mich :)</p>
<!-- /wp:paragraph -->