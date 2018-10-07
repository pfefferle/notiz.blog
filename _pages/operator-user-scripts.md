---
ID: 522
post_title: Operator User Scripts
author: Matthias Pfefferle
post_excerpt: ""
layout: page
permalink: >
  https://notiz.blog/projects/operator-user-scripts/
published: true
post_date: 2007-07-15 23:59:08
---
<!-- wp:paragraph -->
<p><a href="https://addons.mozilla.org/de/firefox/addon/4106">Operator</a> ist ein von <a href="http://www.kaply.com/weblog/">Michael Kaply</a> entwickeltes Addon für den Firefox zum Anzeigen und Bearbeiten von <a href="http://microformats.org">Microformats</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
    <p>Operator leverages microformats that are already available on many web pages to provide new ways to interact with web services.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Das Addon ist so konzipiert dass man kleine Plugins (User-Scripts) in JavaScript schreiben kann um neue Microformats hinzuzufügen oder bestimmte Handler für bestehende zu realisieren.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Installationsanleitung:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ol>
    <li>Zuerst müsst ihr das entsprechende Script lokal speichern.</li>
    <li>Dann öffnet ihr die JavaScript Datei über Options-&gt;User Scripts-&gt;New</li>
    <li>Mit &quot;OK&quot; bestätigen</li>
    <li>Firefox neu starten</li>
    <li>Fertig :)</li>
</ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Links:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li><a href="http://www.kaply.com/weblog/category/operator/">Aktuelle News von Michael Kaply</a></li>
    <li><a href="http://www.kaply.com/weblog/operator-user-scripts/">Weitere User-Scripts</a></li>
    <li><a href="http://www.kaply.com/weblog/operator-user-scripts/creating-a-microformat-action-user-script-basic/">User-Scripts HowTo</a></li>
</ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h3>Optimus</h3>
<!-- /wp:heading -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2007/10/htransformer.jpg" alt="optimus transformer" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>A small User Script to transform detected microformats using the <a href="http://microformatique.com/optimus/">Optimus transformer</a>. Optimus supports two kinds of transformations (microformats to jSON or to XML) and a basic microformats validation.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The User Script supports the transformations and the validation for the following Microformats: <a href="http://microformats.org/wiki/hcard">hCard</a>, <a href="http://microformats.org/wiki/hcal">hCalendar</a>, <a href="http://microformats.org/wiki/adr">adr</a>, <a href="http://microformats.org/wiki/hreview">hReview</a>, <a href="http://microformats.org/wiki/hresume">hResume</a>, <a href="http://microformats.org/wiki/rel-tag">tag</a>, <a href="http://microformats.org/wiki/geo">geo</a>, <a href="http://gmpg.org/xfn/">XFN</a>, <a href="http://microformats.org/wiki/xfolk">xFolk</a>, <a href="http://microformats.org/wiki/rel-license">license</a>, <a href="http://microformats.org/wiki/hAudio">hAudio</a>, <a href="http://microformats.org/wiki/hListing">hListing</a> and <a href="http://microformats.org/wiki/hatom">hAtom-hFeed</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Download: <a href="https://notiz.blog/wp-content/uploads/2008/04/optimus02.js">Optimus User Script for Operator</a> V .2</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Changelog since version 0.1:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li>fixed problem with url</li>
    <li>added hListing and hAudio support</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Download: <a href="https://notiz.blog/wp-content/uploads/2007/10/optimus.js">Optimus User Script for Operator</a> V .1</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h3>wevent</h3>
<!-- /wp:heading -->

<!-- wp:image {"align":"right"} -->
<figure class="wp-block-image alignright" style="max-width:50%"><img src="https://notiz.blog/wp-content/uploads/2007/07/wevent.png" alt="wevent logo" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Ein Script um Inhalte, die mit <a href="http://microformats.org/wiki/hCard">hCard</a> und <a href="http://microformats.org/wiki/hCal">hCalendar</a> ausgezeichnet wurden, in <a href="http://wevent.org">wevent</a> zu importieren außerdem können Tags die mit <a href="http://microformats.org/wiki/rel-tag">rel-tag</a> ausgezeichnet wirden, bei wevent gesucht werden.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Download <a href="https://notiz.blog/wp-content/uploads/2007/08/wevent.js">wevent.js</a> V .2</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>changelog since last version:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li>Added: Events import</li>
    <li>Changed: Einige URLs die sich bei wevent geändert haben</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Download <a href="https://notiz.blog/wp-content/uploads/2007/07/wevent.js">wevent.js</a> V .1</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h3>Mister Wong</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Ein kleines User-Script um <a href="http://microformats.org/wiki/rel-tag">Tags</a> bei Mister Wong zu suchen und <a href="http://microformats.org/wiki/xFolk">xFolk</a> Links bei Mister Wong zu speichern.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2007/07/operator-tag.jpg" alt="Mister Wong Tag" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Links:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li><a href="http://www.mister-wong.de/">Mister Wong</a></li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Download <a href="https://notiz.blog/wp-content/uploads/2007/07/mister-wong.js">mister-wong.js</a></p>
<!-- /wp:paragraph -->