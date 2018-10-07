---
ID: 2383
post_title: Microdata aus HTML5 verbannt
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2010/03/24/microdata-aus-html5-verbannt/
published: true
post_date: 2010-03-24 21:39:17
---
<!-- wp:paragraph -->
<p>Die <abbr title="Resource Description Framework - in - attributes">RDFa</abbr> Community hat es <a href="http://www.w3.org/html/wg/tracker/issues/76">geschafft</a>: <a href="http://dev.w3.org/html5/md/Overview.html">Microdata</a> ist seit einigen Monaten kein fester Bestandteil mehr von <abbr title="Hyper Text Markup Language">HTML</abbr>5! Man verpasst damit leider die einmalige Chance, <a href="http://www.w3.org/TR/xhtml-rdfa-primer/">RDFa</a> und <a href="http://microformats.org/">Microformats</a> als festen Bestandteil von HTML zu veröffentlichen und damit die größtmögliche Verbreitung zu erreichen... keine Erweiterungen... keine Hacks... reines <abbr title="Hypertext Markup Language">HTML</abbr>!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Warum ich so an der <em>Microdata</em> Idee festhalte? Frei nach der <a href="http://microformats.org/about">Microformats Ideologie</a>: "Paving the cow paths" sollte man sich bei der Entwicklung eines neuen Standards hauptsächlich am Nutzerverhalten orientieren: Wenn es für ein Problem noch keinen <em>Standard</em> gab, wie hat man sich bisher beholfen?</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Yahoo!s <a href="https://notiz.blog/2008/06/19/searchmonkey-fuer-anwender/">Search-Monkey</a> meint: mit <a href="http://microformats.org/">Microformats</a>!</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><strong>NUR</strong> <a href="http://search.yahoo.com/search?p=searchmonkey%3Acom.yahoo.page.uf.hcard">hCard</a>: 1,970,000,000</li>
	<li><a href="http://search.yahoo.com/search?p=searchmonkey%3Acom.yahoo.page.rdf.erdf">eRDF</a> + <a href="http://search.yahoo.com/search?p=searchmonkey%3Acom.yahoo.page.rdf.rdfa">RDFa</a>: 1,470,000,000</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>...und ich kann mich nur <a href="https://notiz.blog/2009/06/18/microdata-semantisches-html5/">wiederholen</a>:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Microdata ist für mich die gelungene Weiterentwicklung der Microformats-Idee unter Berücksichtigung von RDFa und prinzipiell lassen sich auch beide Standards mit Microdata umsetzen.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Naja... falls sich keine der oben genannten Semantiken durchsetzen sollte, freue ich mich schon auf folgendes:</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">&lt;div
  itemscope="" itemtype="http://microformats.org/profile/hcard"
  xmlns:vCard="http://www.w3.org/2006/vcard/ns#"
  about="http://www.example.com"
  class="vcard">
  &lt;span
    itemprop="fn"
    property="vCard:FN"
    class="fn">
    Max Mustermann
  &lt;/span>
&lt;/div></pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>(via <a href="http://bnode.org/blog/2010/01/26/microdata-semantic-markup-for-both-rdfers-and-non-rdfers">Benjamin Nowack</a>)</p>
<!-- /wp:paragraph -->