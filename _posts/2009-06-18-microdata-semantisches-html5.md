---
ID: 1700
post_title: 'Microdata &#8211; Semantisches HTML5'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/06/18/microdata-semantisches-html5/
published: true
post_date: 2009-06-18 23:23:08
---
<!-- wp:paragraph -->
<p>Der Inhalt wure an die <a href="https://notiz.blog/2009/10/10/microdata-update-und-usability-studie/">neusten Änderungen der Microdata-Spezifikation</a> angepasst. Letztes Update 30.01.2010.
</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In dem Punkt, dass HTML semantischer werden muss, ist sich die Web-Welt einig, nur das "Wie" ist noch nicht ganz klar. Aus <a href="http://lists.whatwg.org/htdig.cgi/whatwg-whatwg.org/2009-May/019602.html">verschiedenen Gründen</a> (die alle sehr, sehr technisch sind) ist die <abbr title="Web Hypertext Application Technology Working Group"><a href="http://www.whatwg.org/">WHATWG</a></abbr>-Community bzw. <a href="http://ln.hixie.ch/">Ian Hickson</a> im speziellen, nicht sehr begeistert von dem bisherigen De-facto-Standard <a href="http://en.wikipedia.org/wiki/RDFa"><abbr title="Resource Description Framework - in - attributes">RDFa</abbr></a> und hat deshalb vor ein paar Wochen <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/microdata.html">Microdata</a> als eine mögliche Alternative vorgestellt.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Microdata-Objekte bestehen eigentlich <em>nur</em> aus einer Vielzahl von Key/Value-Paaren. Ein <em>Object</em> wird durch einen umschließenden HTML-Tag mit einem <code>itemscope</code>-Attribut gekennzeichnet und hat mehrere <em>Properties</em> ausgezeichnet durch <code>itemprop</code>-Attribute.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div itemscope>
 &lt;p>Mein Name ist &lt;span itemprop="name">Matthias&lt;/span>.&lt;/p>
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Microdata ist für mich die gelungene Weiterentwicklung der <a href="http://microformats.org/">Microformats-Idee</a> unter Berücksichtigung von RDFa und prinzipiell lassen sich auch beide Standards mit Microdata umsetzen. Wie generell von HTML5 gewohnt, kann man auch Microdata auf viele verschiedene Weisen benutzen ohne den Standard zu verletzen.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>Microdata im Microformats-Stil</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Um z.B. eine <a href="http://microformats.org/wiki/hcard">hCard</a> mit Microdata abzubilden muss man eigentlich nur die bisher verwendeten <code>class</code> durch <code>itemprop</code>-Attribute zu ersetzen und mit <code>itemtype</code> das Format festlegen.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div itemscope itemtype="http://microformats.org/profile/hcard">
 &lt;span itemprop="fn">Matthias Pfefferle&lt;/span>
 &lt;img itemprop="photo" src="avatar.png" alt="Avatar" />
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>HTML5 und Microdata bieten außerdem eine ganze Reihe weiterer Tags und Attribute die alle bisherigen Microformats-Probleme beheben sollten. Aber darauf werde ich in einem extra Artikel noch detaillierter darauf eingehen.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>Microdata im RDFa-Stil</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><code>item</code> und <code>itemprop</code> können aber auch durch URIs (ähnlich wie RDFa) ausgezeichnet werden und würden sich dadurch relativ leicht (durch z.B. <abbr title="Gleaning Resource Descriptions from Dialects of Languages"><a href="http://en.wikipedia.org/wiki/GRDDL">GRDDL</a></abbr>) in klassisches <abbr title="Resource Description Framework"><a href="http://en.wikipedia.org/wiki/Resource_Description_Framework">RDF</a></abbr> konvertieren lassen.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div itemscope itemtype="http://www.w3.org/2001/vcard-rdf/3.0#">
  &lt;span itemprop="http://www.w3.org/2001/vcard-rdf/3.0#fn">
    Matthias Pfefferle
  &lt;/span>
  &lt;img itemprop="http://www.w3.org/2001/vcard-rdf/3.0#photo"
       src="avatar.png" alt="Avatar" />
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:heading {"level":4} -->
<h4>Fazit</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Trotz <a href="https://notiz.blog/2009/05/16/html5-wird-kein-rdfa-unterstuetzen/">anfänglicher Skepsis</a> bin ich immer begeisterter von dem neuen HTML5 Draft! Microdata fühlt sich einfach viel mehr nacht HTML an... </p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div itemscope itemtype="http://microformats.org/profile/hcard">
  &lt;a itemprop="url" href="https://notiz.blog">
    &lt;span itemprop="fn">Matthias Pfefferle&lt;/span>
  &lt;/a>
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...als RDFa.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div xmlns:foaf="http://xmlns.com/foaf/0.1/">
  &lt;span typeof="foaf:Person">
    &lt;a property="foaf:name" rel="foaf:homepage" href="https://notiz.blog">
      Matthias
    &lt;/a>
  &lt;/span>
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Trotzdem hoffe ich, dass man sich doch noch irgendwie einigen kann und sich vielleicht in der Mitte trifft. Zwei neue HTML-Spezifikationen (XHTML2 &amp; (X)HTML5) sind schon verwirrend genug, da brauchen wir nicht auch noch zwei unterschiedliche <em>Semantik-HTML</em>-Standards</p>
<!-- /wp:paragraph -->