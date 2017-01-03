---
ID: 519
post_title: Mit wevent Freundeslisten importieren
author: Matthias Pfefferle
post_date: 2007-07-15 23:35:22
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/07/15/mit-wevent-freundeslisten-importieren/
published: true
---
Die Jungs von <a href="http://wevent.org">wevent</a> haben ein neues Feature zum <a href="http://blog.wevent.org/2007/07/importiere-dein-freundesnetzwerk/">Importieren von Freundeslisten</a> implementiert. Der Import funktioniert wie auch bei <a href="http://pixelsebi.com/2007-06-25/dopplr-importiert-social-network-auf-basis-von-microformats/">dopplr</a> über das <a href="http://microformats.org/wiki/hCard">hCard</a> Microformat. Das heißt, es ist möglich bestehende sozialen Netze (Twitter, Last.fm, ...) über einen Klick an wevent zu übertragen.

Und um das ganze noch mehr zu vereinfachen habe ich ein kleines <a href="http://www.kaply.com/weblog/category/operator/">Operator</a> Script geschrieben welches die hCard URL an das Import Script übergibt.

Installationsanleitung:
<ol><li>Zuerst müsst ihr das Script (<a href='http://notiz.blog/wp-content/uploads/2007/07/wevent.js' title='Operator Script'>wevent.js</a>) lokal speichern.</li>
<li>Dann öffnet ihr die JavaScript Datei über Options-&gt;User Scripts-&gt;New</li>
<li>Mit "OK" bestätigen</li>
<li>Firefox neu starten</li>
<li>Fertig :)</li></ol>

<img class="aligncenter" src='http://notiz.blog/wp-content/uploads/2007/07/wevent-operator.jpg' alt='wevent operator user script' />

Wenn <a href="http://blog.dopefreshtight.de/">Dennis</a> und <a href="http://soeren-web.de/">Sören</a> das ganze auch noch für hCalendar umgesetzt haben gibt's natürlich auch ein Update für das Script.

Links:
<ul><li><a href="http://wevent.org/friends/import">wevent Freundeslisten-Import</a></li>
<li><a href="http://www.kaply.com/weblog/2007/07/03/operator-08b-is-available/">Operator 0.8b für Firefox</a></li></ul>