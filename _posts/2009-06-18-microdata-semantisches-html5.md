---
ID: 1700
post_title: 'Microdata &#8211; Semantisches HTML5'
author: Matthias Pfefferle
post_date: 2009-06-18 23:23:08
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/06/18/microdata-semantisches-html5/
published: true
---
<div class="alert alert-info">Der Inhalt wure an die <a href="http://notiz.blog/2009/10/10/microdata-update-und-usability-studie/">neusten Änderungen der Microdata-Spezifikation</a> angepasst. Letztes Update 30.01.2010.</div>

In dem Punkt, dass HTML semantischer werden muss, ist sich die Web-Welt einig, nur das "Wie" ist noch nicht ganz klar. Aus <a href="http://lists.whatwg.org/htdig.cgi/whatwg-whatwg.org/2009-May/019602.html">verschiedenen Gründen</a> (die alle sehr, sehr technisch sind) ist die <abbr title="Web Hypertext Application Technology Working Group"><a href="http://www.whatwg.org/">WHATWG</a></abbr>-Community bzw. <a href="http://ln.hixie.ch/">Ian Hickson</a> im speziellen, nicht sehr begeistert von dem bisherigen De-facto-Standard <a href="http://en.wikipedia.org/wiki/RDFa"><abbr title="Resource Description Framework - in - attributes">RDFa</abbr></a> und hat deshalb vor ein paar Wochen <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/microdata.html">Microdata</a> als eine mögliche Alternative vorgestellt.

Microdata-Objekte bestehen eigentlich <em>nur</em> aus einer Vielzahl von Key/Value-Paaren. Ein <em>Object</em> wird durch einen umschließenden HTML-Tag mit einem <code>itemscope</code>-Attribut gekennzeichnet und hat mehrere <em>Properties</em> ausgezeichnet durch <code>itemprop</code>-Attribute.

<pre>&lt;div <strong>itemscope</strong>&gt;
 &lt;p&gt;Mein Name ist &lt;span <strong>itemprop</strong>="name"&gt;Matthias&lt;/span&gt;.&lt;/p&gt;
&lt;/div&gt;</pre>

Microdata ist für mich die gelungene Weiterentwicklung der <a href="http://microformats.org/">Microformats-Idee</a> unter Berücksichtigung von RDFa und prinzipiell lassen sich auch beide Standards mit Microdata umsetzen. Wie generell von HTML5 gewohnt, kann man auch Microdata auf viele verschiedene Weisen benutzen ohne den Standard zu verletzen.

<h4 id="microdata-microformats">Microdata im Microformats-Stil</h4>

Um z.B. eine <a href="http://microformats.org/wiki/hcard">hCard</a> mit Microdata abzubilden muss man eigentlich nur die bisher verwendeten <code>class</code> durch <code>itemprop</code>-Attribute zu ersetzen und mit <code>itemtype</code> das Format festlegen.

<pre>&lt;div <strong>itemscope itemtype="http://microformats.org/profile/hcard"</strong>&gt;
 &lt;span <strong>itemprop="fn"</strong>&gt;Matthias Pfefferle&lt;/span&gt;
 &lt;img <strong>itemprop="photo"</strong> src="avatar.png" alt="Avatar" /&gt;
&lt;/div&gt;</pre>

HTML5 und Microdata bieten außerdem eine ganze Reihe weiterer Tags und Attribute die alle bisherigen Microformats-Probleme beheben sollten. Aber darauf werde ich in einem extra Artikel noch detaillierter darauf eingehen.

<h4 id="microdata-rdfa">Microdata im RDFa-Stil</h4>

<code>item</code> und <code>itemprop</code> können aber auch durch URIs  (ähnlich wie RDFa) ausgezeichnet werden und würden sich dadurch relativ leicht (durch z.B. <abbr title="Gleaning Resource Descriptions from Dialects of Languages"><a href="http://en.wikipedia.org/wiki/GRDDL">GRDDL</a></abbr>) in klassisches <abbr title="Resource Description Framework"><a href="http://en.wikipedia.org/wiki/Resource_Description_Framework">RDF</a></abbr> konvertieren lassen.

<pre>&lt;div <strong>itemscope itemtype="http://www.w3.org/2001/vcard-rdf/3.0#"</strong>&gt;
  &lt;span <strong>itemprop="http://www.w3.org/2001/vcard-rdf/3.0#fn"</strong>&gt;
    Matthias Pfefferle
  &lt;/span&gt;
  &lt;img <strong>itemprop="http://www.w3.org/2001/vcard-rdf/3.0#photo"</strong>
       src="avatar.png" alt="Avatar" /&gt;
&lt;/div&gt;</pre>

<h4>Fazit</h4>

Trotz <a href="http://notiz.blog/2009/05/16/html5-wird-kein-rdfa-unterstuetzen/">anfänglicher Skepsis</a> bin ich immer begeisterter von dem neuen HTML5 Draft! Microdata fühlt sich einfach viel mehr nacht HTML an... 

<pre>&lt;div <strong>itemscope itemtype="http://microformats.org/profile/hcard"</strong>&gt;
  &lt;a <strong>itemprop="url"</strong> href="http://notiz.blog"&gt;
    &lt;span <strong>itemprop="fn"</strong>&gt;Matthias Pfefferle&lt;/span&gt;
  &lt;/a&gt;
&lt;/div&gt;</pre>

...als RDFa.

<pre>&lt;div <strong>xmlns:foaf="http://xmlns.com/foaf/0.1/"</strong>&gt;
  &lt;span <strong>typeof="foaf:Person"</strong>&gt;
    &lt;a <strong>property="foaf:name"</strong> <strong>rel="foaf:homepage"</strong> href="http://notiz.blog"&gt;
      Matthias
    &lt;/a&gt;
  &lt;/span&gt;
&lt;/div&gt;</pre>

Trotzdem hoffe ich, dass man sich doch noch irgendwie einigen kann und sich vielleicht in der Mitte trifft. Zwei neue HTML-Spezifikationen (XHTML2 & (X)HTML5) sind schon verwirrend genug, da brauchen wir nicht auch noch zwei unterschiedliche <em>Semantik-HTML</em>-Standards