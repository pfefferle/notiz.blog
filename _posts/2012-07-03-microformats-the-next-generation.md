---
ID: 4343
post_title: 'Microformats: The next generation'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2012/07/03/microformats-the-next-generation/
published: true
post_date: 2012-07-03 08:43:02
---
<!-- wp:image {"align":"right"} -->
<figure class="wp-block-image alignright" style="max-width:50%"><img src="https://notiz.blog/wp-content/uploads/2007/03/mf-white.png" alt="mf-white" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><a href="http://microformats.org/2012/06/25/microformats-org-at-7">microformats.org wird 7</a>... Alles Gute!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Zur Feier des Tages hat sich Frances Berriman die Mühe gemacht, die letzten 7 Jahre zusammen zu fassen und einen Ausblick auf die kommenden Änderungen zu geben.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Da ich, seit ich bloggen kann, schon <a href="https://notiz.blog/tag/microformats/">über Microformats berichte</a>, will ich den Rückblick nicht weiter kommentieren und nur auf die kommende Weiterentwicklung ein wenig eingehen.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Microformats und HTML5</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Seit dem ich das letzte mal <a href="https://notiz.blog/2008/07/30/html5-is-made-for-microformats/">über diese Kombination geschrieben habe</a>, hat sich leider nicht viel geändert... Die Microformats Community weigert sich weiterhin auf Microdata oder RDFa &quot;upzugraden&quot; und hält krampfhaft an den semantischen <code>classes</code> fest. Nichtsdestotrotz macht HTML5 mit <code>&lt;time /&gt;</code> und <code>&lt;data /&gt;</code> dem leidigen Thema <a href="https://notiz.blog/2009/05/12/microformats-value-class-pattern/"><code>abbr-design-pattern</code> bzw. <code>value-class-pattern</code></a> ein Ende. Statt Meta-Informationen umständlich in HTML-Attributen zu verwurschteln, können Termine und GEO Daten bald sauber dargestellt werden:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;time class=&quot;dtstart&quot; datetime=&quot;2006-09-23&quot;&gt;a Saturday&lt;/time&gt;
...
&lt;data class=&quot;geo&quot; value=&quot;37.386013;-122.082932&quot; &gt;Mountain View&lt;/data&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Immerhin! Mehr dazu im <a href="http://microformats.org/wiki/html5">microformats-wiki</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Namespaces</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Die wohl größten Veränderungen sind aber die geplanten <a href="http://microformats.org/wiki/microformats-2#distinguishing_properties_from_other_classes">Pseudo-Namespaces</a> welche hauptsächlich das Parsen von Microformats vereinfachen sollen. Microformats waren bisher sehr fehleranfällig, da sie sich die <code>class</code>-Attribute mit CSS und JavaScript zu teilen hatten. Es besteht immer die Gefahr dass rein für CSS genutzte Attribute fälschlicherweise für Microformats genutzt wurden oder dass die semantischen Class-Names einem Re-Design zum Opfer fielen. Die Prefixes &#x27;<code>h-</code>&#x27;, &#x27;<code>p-</code>&#x27;, &#x27;<code>u-</code>&#x27;, &#x27;<code>dt-</code>&#x27; und &#x27;<code>e-</code>&#x27; sollen das Zukünftig verhindern und ein generisches parsen ermöglichen.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h3>&#x27;<code>h-</code>&#x27; kennzeichnet einen Microformats-Container</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Bisher ist die Microformats Community etwas inkonsequent mit der Benennung ihrer Formate... Mal mit beginnendem &quot;v&quot;, mal mit &quot;h&quot; und in seltenen Fällen auch ohne oder mit anderem Buchstaben:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li>hCard: <code>class=&quot;vcard&quot;</code></li>
    <li>hAtom: <code>class=&quot;hfeed&quot;</code></li>
    <li>adr: <code>class=&quot;adr&quot;</code></li>
    <li>xFolk: <code>class=&quot;xfolkentry&quot;</code></li>
    <li>XOXO: <code>class=&quot;xoxo&quot;</code></li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Mit den Prefixes soll das jetzt alles vereinheitlicht werden:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li>hCard: <code>class=&quot;h-card&quot;</code></li>
    <li>hAtom: <code>class=&quot;h-feed&quot;</code></li>
    <li>adr: <code>class=&quot;h-adr&quot;</code></li>
</ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h3>&#x27;<code>p-</code>&#x27; zeichnet <em>Properties</em> aus</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Die mit &#x27;<code>p-</code>&#x27; gekennzeichnet Properties sollten, wenn nicht expliziert definiert, als Plain-Text interpretiert werden (kein HTML). Ein klassisches Property ist beispielsweise der Name einer Person:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class=&quot;h-card&quot;&gt;
 &lt;span class=&quot;p-fn&quot;&gt;Tantek Çelik&lt;/span&gt;
&lt;/div&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h3>&#x27;<code>e-</code>&#x27; zeichnet <em>Rich Text</em> aus</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Das &#x27;<code>e-</code>&#x27; Prefix könnte als Abkürzung für &quot;element tree&quot;, &quot;embedded markup&quot;, oder &quot;encapsulated markup&quot; stehen und kann im Gegansatz zu den Properties auch HTML-Code beinhalten. In hAtom könnte der <code>entry-content</code> zu <code>e-entry-content</code> und bei der hReview die <code>description</code> zur <code>e-description</code> werden.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h3>&#x27;<code>dt-</code>&#x27; für DateTime und &#x27;<code>u-</code>&#x27; für URL</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Aus <code>dtstart</code> wird <code>dt-start</code> und alle URL-Felder bekommen ein vorgestelltes &#x27;<code>u-</code>&#x27;:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;a class=&quot;u-url&quot; href=&quot;...&quot;&gt;...&lt;/a&gt;

&lt;img class=&quot;u-photo&quot; src=&quot;...&quot; /&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Die URL kann in bestimmten Situtionen auch weg fallen, dazu aber im nächsten Beispiel mehr...</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Simpel und unabhängig vom Format</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Zukünftig soll es auch nicht mehr so umständlich sein Informationen semantisch auszuzeichnen. Will man derzeit einen simplen Link mit einer <a href="http://microformats.org/wiki/hcard">hCard</a> versehen, muss man ihn wie folgt aufblähen:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class=&quot;vcard&quot;&gt;
 &lt;a class=&quot;url fn&quot; href=&quot;http://tantek.com/&quot;&gt;Tantek Çelik&lt;/a&gt;
&lt;/div&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Nach der Überarbeitung soll folgendes reichen:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;a class=&quot;h-card&quot; href=&quot;http://tantek.com/&quot;&gt;Tantek Çelik&lt;/a&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Dabei gilt die Regel: Wenn es sich bei (z.B.) einer vCard um einen Link oder ein Bild handelt, kann man auf &#x27;<code>u-*</code>&#x27; und &#x27;<code>p-name</code>&#x27; verzichten... so ungefär zumindest ;)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Mehr dazu im Microformats-Wiki: <a href="http://microformats.org/wiki/microformats-2-implied-properties">implied properties</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Außerdem kommt mit v2 eine Anleitung wie Microformats auf andere Formate wie JSON gemappt werden sollen. Aus...</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;a class=&quot;h-card&quot; href=&quot;http://benward.me&quot;&gt;Ben Ward&lt;/a&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>wird...</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>[{
  &quot;type&quot;: [&quot;h-card&quot;],
  &quot;properties&quot;: {
    &quot;name&quot;: [&quot;Frances Berriman&quot;] 
  }
}]</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h2>Fazit</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Ich bin mir noch nicht ganz sicher was ich von den geplanten Änderungen halten soll... die Nutzung der neuen HTML5 Tags und die Vereinfachung und Vereinheitlichung der Formate finde ich gut und notwendig... Auch eine einheitliche Regel, wie Microformats in anderen Formaten abgebildet werden sollen (z.B. JSON) macht durchaus Sinn (warum das Sinn macht, <a href="http://microformats.org/wiki/JSON">hier</a>)... aber den Pseudo-Namespaces kann ich bisher nichts abgewinnen! Der &quot;Namespace&quot; sorgt zwar für mehr Qualität beim Parsen der Microformats, aber auf Kosten des semantischen HTMLs.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Microformats sollten weiterhin für schönes, semantisches HTML sorgen und mehr nicht. Geht es um maschinenlesbaren Code, sollte man mit der Zeit gehen und auf <a href="https://notiz.blog/2009/06/18/microdata-semantisches-html5/">Microdata</a> oder <a href="https://notiz.blog/2009/07/16/rdfa-wird-wohl-doch-in-html5-integriert/">RDFa</a> setzen. Ob man seinen Quelltext an Microformats v2 anpasst oder mit <a href="http://schema.org/">Schema.org</a> auszeichnet sollte kaum mehr Aufwand sein.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>...Übrigens: Wer noch mehr über die Vorteile von Microdata gegenüber Microformats lesen will, sollte sich die <a href="https://notiz.blog/2011/06/21/pfefferles-openweb-microformats-v2/">Ausgabe 10 des Webstandards-Magazin</a> durchlesen oder die Reihe &quot;<a href="https://notiz.blog/2009/08/10/microdata-wie-microformats-bloss-besser-teil-1/">Microdata – wie Microformats bloß besser…</a>&quot; hier im Blog!</p>
<!-- /wp:paragraph -->