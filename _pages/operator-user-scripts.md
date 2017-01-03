---
ID: 522
post_title: Operator User Scripts
author: Matthias Pfefferle
post_date: 2007-07-15 23:59:08
post_excerpt: ""
layout: page
permalink: >
  https://notiz.blog/projects/operator-user-scripts/
published: true
---
<a href="https://addons.mozilla.org/de/firefox/addon/4106">Operator</a> ist ein von <a href="http://www.kaply.com/weblog/">Michael Kaply</a> entwickeltes Addon für den Firefox zum Anzeigen und Bearbeiten von <a href="http://microformats.org">Microformats</a>.

<blockquote>Operator leverages microformats that are already available on many web pages to provide new ways to interact with web services.</blockquote>
Das Addon ist so konzipiert dass man kleine Plugins (User-Scripts) in JavaScript schreiben kann um neue Microformats hinzuzufügen oder bestimmte Handler für bestehende zu realisieren.  

Installationsanleitung:
<ol><li>Zuerst müsst ihr das entsprechende Script lokal speichern.</li>
<li>Dann öffnet ihr die JavaScript Datei über Options->User Scripts->New</li>
<li>Mit "OK" bestätigen</li>
<li>Firefox neu starten</li>
<li>Fertig :)</li></ol>

Links:
<ul><li><a href="http://www.kaply.com/weblog/category/operator/">Aktuelle News von Michael Kaply</a></li>
<li><a href="http://www.kaply.com/weblog/operator-user-scripts/">Weitere User-Scripts</a></li>
<li><a href="http://www.kaply.com/weblog/operator-user-scripts/creating-a-microformat-action-user-script-basic/">User-Scripts HowTo</a></li></ul>

<h3 id="optimus">Optimus</h3>
<img src='http://notiz.blog/wp-content/uploads/2007/10/htransformer.jpg' alt='optimus transformer' style='border: none;' />

A small User Script to transform detected microformats using the <a href="http://microformatique.com/optimus/">Optimus transformer</a>. Optimus supports two kinds of transformations (microformats to jSON or to XML) and a basic microformats validation.

The User Script supports the transformations and the validation for the following Microformats: <a href="http://microformats.org/wiki/hcard" rel="tag">hCard</a>, <a href="http://microformats.org/wiki/hcal" rel="tag">hCalendar</a>, <a href="http://microformats.org/wiki/adr" rel="tag">adr</a>, <a href="http://microformats.org/wiki/hreview" rel="tag">hReview</a>, <a href="http://microformats.org/wiki/hresume" rel="tag">hResume</a>, <a href="http://microformats.org/wiki/rel-tag" rel="tag">tag</a>, <a href="http://microformats.org/wiki/geo" rel="tag">geo</a>, <a href="http://gmpg.org/xfn/" rel="tag">XFN</a>, <a href="http://microformats.org/wiki/xfolk" rel="tag">xFolk</a>, <a href="http://microformats.org/wiki/rel-license" rel="tag">license</a>, <a href="http://microformats.org/wiki/hAudio" rel="tag">hAudio</a>, <a href="http://microformats.org/wiki/hListing" rel="tag">hListing</a> and <a href="http://microformats.org/wiki/hatom" rel="tag">hAtom-hFeed</a>.

<p class="download">Download: <a href='http://notiz.blog/wp-content/uploads/2008/04/optimus02.js' title='Optimus User Script for Operator'>Optimus User Script for Operator</a> V .2</p>

Changelog since version 0.1:

<ul><li>fixed problem with url</li>
<li>added hListing and hAudio support</li></ul>

<p class="download">Download: <a href='http://notiz.blog/wp-content/uploads/2007/10/optimus.js' title='Optimus User Script for Operator'>Optimus User Script for Operator</a> V .1</p>

<h3 id="wevent">wevent</h3>
<img src='http://notiz.blog/wp-content/uploads/2007/07/wevent.png' alt='wevent logo' style='border: none;' />

Ein Script um Inhalte, die mit <a href="http://microformats.org/wiki/hCard">hCard</a> und <a href="http://microformats.org/wiki/hCal">hCalendar</a> ausgezeichnet wurden, in <a href="http://wevent.org">wevent</a> zu importieren außerdem können Tags die mit <a href="http://microformats.org/wiki/rel-tag">rel-tag</a> ausgezeichnet wirden, bei wevent gesucht werden.

<p class="download">Download <a href='http://notiz.blog/wp-content/uploads/2007/08/wevent.js' title='download wevent.js'>wevent.js</a> V .2</p>
changelog since last version:
<ul><li>Added: Events import</li>
<li>Changed: Einige URLs die sich bei wevent geändert haben</li></ul>

<p class="download">Download <a href='http://notiz.blog/wp-content/uploads/2007/07/wevent.js' title='download wevent.js'>wevent.js</a> V .1</p>

<h3 id="wong">Mister Wong</h3>

Ein kleines User-Script um <a href="http://microformats.org/wiki/rel-tag">Tags</a> bei Mister Wong zu suchen und <a href="http://microformats.org/wiki/xFolk">xFolk</a> Links bei Mister Wong zu speichern.

<img src='http://notiz.blog/wp-content/uploads/2007/07/operator-tag.jpg' alt='Mister Wong Tag' />

Links:
<ul><li><a href="http://www.mister-wong.de/">Mister Wong</a></li></ul>

<p class="download">Download <a href='http://notiz.blog/wp-content/uploads/2007/07/mister-wong.js' title='Operator Script'>mister-wong.js</a></p>