---
ID: 679
post_title: >
  Unobtrusively Mapping Microformats with
  jQuery
author: Matthias Pfefferle
post_date: 2007-12-17 21:19:09
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/12/17/unobtrusively-mapping-microformats-with-jquery/
published: true
---
Auf <a href="http://24ways.org">24 ways</a> habe ich einen schönen Artikel über <em><a href="http://24ways.org/2007/unobtrusively-mapping-microformats-with-jquery">Unobtrusively Mapping Microformats with jQuery</a></em> gefunden.

<a href="http://en.wikipedia.org/wiki/Unobtrusive_JavaScript">Unobtrusive JavaScript</a> verfolgt den Ansatz, den JavaScript Code komplett von der HTML Seite zu trennen. Dise Methode ermöglicht das schnelle und einfache Ändern des JavaScript-Codes an zentraler Stelle, ähnlich wie bei der Trennung von Design und <abbr title="Hypertext Markup Language">HTML</abbr> bei <abbr title="Cascading Style Sheets">CSS</abbr>.

Der Artikel beschreibt, wie man mit <a href="http://microformats.org/wiki/hCard">hCard</a> ausgezeichnete Kontakt-Daten auf <a href="http://maps.google.de">Google-Maps</a> anzeigt (<a href="http://24ways.org/examples/unobtrusively-mapping-microformats-with-jquery/restaurants.html">Demo</a>).

Eine wesentlich simplete Demo lässt sich mit den <a href="http://microformats.org/wiki/rel">rel-Attribute</a> realisieren. Als Beispiel HTML Code nehmen wir das <a href="http://microformats.org/wiki/rel-nofollow">rel-nofollow</a> Microformat:

<pre class="code">&lt;a href="http://google.de" rel="nofollow"&gt;Google.de&lt;/a&gt;</pre>

Mit dem folgenden Code ist es Möglich, das <code>a</code> HTML-Tag mit dem CSS-Code <code>text-decoration: line-through;</code> zu erweitern.

<pre class="code">jQuery("a[@rel=nofollow]").css("text-decoration", "line-through");</pre>

Das ganze funktioniert natürlich auch wesentlich eleganter mit CSS, aber es geht hier ja nur ums Prinzip ;) 

Den wesentlich besseren und ausführlicheren Bericht gibt es auf <a href="http://24ways.org/2007/unobtrusively-mapping-microformats-with-jquery">24ways.org</a>.