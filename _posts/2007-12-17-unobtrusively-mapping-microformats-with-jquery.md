---
ID: 679
post_title: >
  Unobtrusively Mapping Microformats with
  jQuery
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/12/17/unobtrusively-mapping-microformats-with-jquery/
published: true
post_date: 2007-12-17 21:19:09
---
<!-- wp:paragraph -->
<p>Auf <a href="http://24ways.org">24 ways</a> habe ich einen schönen Artikel über <em><a href="http://24ways.org/2007/unobtrusively-mapping-microformats-with-jquery">Unobtrusively Mapping Microformats with jQuery</a></em> gefunden.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="http://en.wikipedia.org/wiki/Unobtrusive_JavaScript">Unobtrusive JavaScript</a> verfolgt den Ansatz, den JavaScript Code komplett von der HTML Seite zu trennen. Dise Methode ermöglicht das schnelle und einfache Ändern des JavaScript-Codes an zentraler Stelle, ähnlich wie bei der Trennung von Design und <abbr title="Hypertext Markup Language">HTML</abbr> bei <abbr title="Cascading Style Sheets">CSS</abbr>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Der Artikel beschreibt, wie man mit <a href="http://microformats.org/wiki/hCard">hCard</a> ausgezeichnete Kontakt-Daten auf <a href="http://maps.google.de">Google-Maps</a> anzeigt (<a href="http://24ways.org/examples/unobtrusively-mapping-microformats-with-jquery/restaurants.html">Demo</a>).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Eine wesentlich simplete Demo lässt sich mit den <a href="http://microformats.org/wiki/rel">rel-Attribute</a> realisieren. Als Beispiel HTML Code nehmen wir das <a href="http://microformats.org/wiki/rel-nofollow">rel-nofollow</a> Microformat:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;a href="http://google.de" rel="nofollow">Google.de&lt;/a></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Mit dem folgenden Code ist es Möglich, das <code>a</code> HTML-Tag mit dem CSS-Code <code>text-decoration: line-through;</code> zu erweitern.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>jQuery("a[@rel=nofollow]").css("text-decoration", "line-through");</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Das ganze funktioniert natürlich auch wesentlich eleganter mit CSS, aber es geht hier ja nur ums Prinzip ;) </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Den wesentlich besseren und ausführlicheren Bericht gibt es auf <a href="http://24ways.org/2007/unobtrusively-mapping-microformats-with-jquery">24ways.org</a>.</p>
<!-- /wp:paragraph -->