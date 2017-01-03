---
ID: 1409
post_title: >
  BOSS mit vollständiger
  SearchMonkey-Integration
author: Matthias Pfefferle
post_date: 2009-02-12 08:40:21
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/02/12/boss-mit-vollstaendiger-searchmonkey-integration/
published: true
aktt_notify_twitter:
  - 'yes'
aktt_tweeted:
  - "1"
---
Die strukturierte Suche über diverse <a href="http://notiz.blog/2008/12/09/searchmonkey-bekommt-neue-formate/">Microformats-Kürzel</a> im <a href="http://notiz.blog/2008/12/10/boss-build-your-own-semantic-search/">Query</a> funktioniert ja schon eine ganze Weile auch mit BOSS (<a href="http://netzwertig.com/2008/11/27/yahoo-boss-trifft-techcrunch-suchmaschinen-innovation-geht-auch-ohne-google/">Build your Own Search Service</a>), aber, <a href="http://developer.yahoo.net/blog/archives/2009/02/new_boss_features.html">wie gestern von Yahoo! Ankündigt</a>, wurde der <a href="http://developer.yahoo.com/search/boss/structureddata.html">SearchMonkey jetzt komplett in die Such-API <em>BOSS</em> integriert</a>.  

Wer seiner BOSS-Applikation semantischen Charakter spendieren will, muss seiner Query-URL einfach folgende Key-Value Paare anhängen:
<ul><li><code>&view=searchmonkey_rdf</code> - für diverse RDF-Formate wie z.B. <a href="http://dublincore.org/2008/01/14/dcterms.rdf#">Dublin Core</a>, <abbr title="friend of a friend"><a href="http://developer.yahoo.com/searchmonkey/smguide/Friend-Of-A-Friend.html">FOAF</a></abbr> oder <abbr title="Semantically-Interlinked Online Communities"><a href="http://en.wikipedia.org/wiki/SIOC">SIOC</a></abbr></li>
<li><code>&view=searchmonkey_feed</code> - für diverse Microformats wie z.B. <a href="http://microformats.org/wiki/hCard">hCard</a> oder <a href="http://microformats.org/wiki/hCalendar">hCalendar</a></li></ul>

...und so wird aus einem <a href="http://boss.yahooapis.com/ysearch/web/v1/searchmonkeyid:com.yahoo.page.uf.hcard+Matthias+Pfefferle?appid=cHw_mwbV34EfW.Tq2vzNGZfhy62p.Frsvcagh2V0vWSmjeLxcSk1oNvXtvurpMTQVA--&format=xml">normalen Ergebnis</a> ein <a href="http://boss.yahooapis.com/ysearch/web/v1/searchmonkeyid:com.yahoo.page.uf.hcard+Matthias+Pfefferle?appid=cHw_mwbV34EfW.Tq2vzNGZfhy62p.Frsvcagh2V0vWSmjeLxcSk1oNvXtvurpMTQVA--&format=xml&view=searchmonkey_feed">semantisches Feuerwerk</a> :(|)