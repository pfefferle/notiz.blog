---
ID: 387
post_title: rel und rev
author: Matthias Pfefferle
post_date: 2007-05-14 22:50:27
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/05/14/rel-und-rev/
published: true
---
Seit ich mich mehr mit Microformats beschäftige, lese ich auch immer öfter von den HTML Attributen <code>rel</code> und <code>rev</code> unter die Augen, eines der Bekanntesten ist wohl <code>&lt;a href="..." <strong>rel="licence"</strong>&gt;...&lt;/a&gt;</code> für z.B. die <a href="http://creativecommons.org/">Creative Commons</a>. 

Aber für was genau stehen die HTML Attribute <code>rel</code> und <code>rev</code> genau?

<a href="http://de.selfhtml.org/html/verweise/typisierte.htm#beziehung">SelfHTML</a> meint dazu:
<blockquote>Mit dem Attribut <code>rel</code> bestimmen Sie eine logische Vorwärtsbeziehung zum Verweisziel, mit <code>rev</code> eine logische Rückwärtsbeziehung (<code>rel</code> = relation = Bezug, <code>rev</code> = reverse = Umkehr). Beide Angaben sind nur in Verbindung mit dem Attribut <code>href</code> sinnvoll - dort geben Sie wie üblich das eigentliche Verweisziel an.</blockquote>

Betrachtet man es am Beispiel der <abbr title="XHTML Friends Network"><a href="http://gmpg.org/xfn/">XFN</a></abbr> Microformats wird definiert, in welcher Beziehung man zu der verlinkten Person steht, man hätte das ganze auch als <code>rev="friend met"</code> definieren, da der andere auch die gleiche Beziehung zu mir hat.

Im <a href="http://microformats.org/wiki/">Microformats Wiki</a> sind einige dieser Attribute definiert.

<code>rel</code>:
<ul><li><a href="http://gmpg.org/xfn/">XFN</a>: Zeigt die Beziehung zur verlinkten Person, Bsp.: <code>&lt;a href="..." rel="friend met"&gt;...</code></li>
<li><a href="http://microformats.org/wiki/rel-tag">rel-tag</a>: Gibt an, dass es sich um einen Tag handelt, Bsp.: <code>&lt;a href="http://technorati.com/tag/notizblog" rel="tag"&gt;...</code></li>
<li><a href="http://microformats.org/wiki/rel-license">rel-licence</a>: Attribut für Lizenzen, Bsp.: <code>&lt;a href="http://creativecommons.org/licenses/by/2.0/" rel="license"&gt;...</code></li>
<li><a href="http://microformats.org/wiki/vote-links">vote-links</a>: Zeigt an ob man für oder gegen den Verlinkten stimmen  soll, Bsp.: <code>&lt;a rev="vote-for" href="http://notiz.blog"  
   title="vote for"&gt;...</code></li>
<li><a href="http://microformats.org/wiki/rel-payment">rel-paymant</a>, <a href="http://microformats.org/wiki/rel-nofollow">rel-nofollow</a> und <a href="http://microformats.org/wiki/rel-directory">rel-directory</a></li></ul>

Mehr zu den <code>rel</code> Attributen im <a href="http://microformats.org/wiki/rel">Microformats Wiki</a>.