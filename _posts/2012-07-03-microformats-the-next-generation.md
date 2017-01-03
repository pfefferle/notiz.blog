---
ID: 4343
post_title: 'Microformats: The next generation'
author: Matthias Pfefferle
post_date: 2012-07-03 08:43:02
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2012/07/03/microformats-the-next-generation/
published: true
---
<img src="http://notiz.blog/wp-content/uploads/2007/03/mf-white.png" alt="mf-white" width="150" height="150" class="alignright size-full wp-image-1750" /><a href="http://microformats.org/2012/06/25/microformats-org-at-7">microformats.org wird 7</a>... Alles Gute!

Zur Feier des Tages hat sich Frances Berriman die Mühe gemacht, die letzten 7 Jahre zusammen zu fassen und einen Ausblick auf die kommenden Änderungen zu geben.

Da ich, seit ich bloggen kann, schon <a href="http://notiz.blog/tag/microformats/">über Microformats berichte</a>, will ich den Rückblick nicht weiter kommentieren und nur auf die kommende Weiterentwicklung ein wenig eingehen.

<h2 id="uf-v2-html5">Microformats und HTML5</h2>

Seit dem ich das letzte mal <a href="http://notiz.blog/2008/07/30/html5-is-made-for-microformats/">über diese Kombination geschrieben habe</a>, hat sich leider nicht viel geändert... Die Microformats Community weigert sich weiterhin auf Microdata oder RDFa "upzugraden" und hält krampfhaft an den semantischen <code>classes</code> fest. Nichtsdestotrotz macht HTML5 mit <code>&lt;time /&gt;</code> und <code>&lt;data /&gt;</code> dem leidigen Thema <a href="http://notiz.blog/2009/05/12/microformats-value-class-pattern/"><code>abbr-design-pattern</code> bzw. <code>value-class-pattern</code></a> ein Ende. Statt Meta-Informationen umständlich in HTML-Attributen zu verwurschteln, können Termine und GEO Daten bald sauber dargestellt werden:

<pre><code>&lt;time class="dtstart" datetime="2006-09-23"&gt;a Saturday&lt;/time&gt;
...
&lt;data class="geo" value="37.386013;-122.082932" &gt;Mountain View&lt;/data&gt;</code></pre>

Immerhin! Mehr dazu im <a href="http://microformats.org/wiki/html5">microformats-wiki</a>.

<h2 id="uf-v2-namespaces">Namespaces</h2>

Die wohl größten Veränderungen sind aber die geplanten <a href="http://microformats.org/wiki/microformats-2#distinguishing_properties_from_other_classes">Pseudo-Namespaces</a> welche hauptsächlich das Parsen von Microformats vereinfachen sollen. Microformats waren bisher sehr fehleranfällig, da sie sich die <code>class</code>-Attribute mit CSS und JavaScript zu teilen hatten. Es besteht immer die Gefahr dass rein für CSS genutzte Attribute fälschlicherweise für Microformats genutzt wurden oder dass die semantischen Class-Names einem Re-Design zum Opfer fielen. Die Prefixes '<code>h-</code>', '<code>p-</code>', '<code>u-</code>', '<code>dt-</code>' und '<code>e-</code>' sollen das Zukünftig verhindern und ein generisches parsen ermöglichen.

<h3>'<code>h-</code>' kennzeichnet einen Microformats-Container</h3>

Bisher ist die Microformats Community etwas inkonsequent mit der Benennung ihrer Formate... Mal mit beginnendem "v", mal mit "h" und in seltenen Fällen auch ohne oder mit anderem Buchstaben:

<ul><li>hCard: <code>class="vcard"</code></li>
<li>hAtom: <code>class="hfeed"</code></li>
<li>adr: <code>class="adr"</code></li>
<li>xFolk: <code>class="xfolkentry"</code></li>
<li>XOXO: <code>class="xoxo"</code></li></ul>

Mit den Prefixes soll das jetzt alles vereinheitlicht werden:

<ul><li>hCard: <code>class="h-card"</code></li>
<li>hAtom: <code>class="h-feed"</code></li>
<li>adr: <code>class="h-adr"</code></li></ul>

<h3>'<code>p-</code>' zeichnet <em>Properties</em> aus</h3>

Die mit '<code>p-</code>' gekennzeichnet Properties sollten, wenn nicht expliziert definiert, als Plain-Text interpretiert werden (kein HTML). Ein klassisches Property ist beispielsweise der Name einer Person:

<pre><code>&lt;div class="h-card"&gt;
 &lt;span class="p-fn"&gt;Tantek Çelik&lt;/span&gt;
&lt;/div&gt;</code></pre>

<h3>'<code>e-</code>' zeichnet <em>Rich Text</em> aus</h3>

Das '<code>e-</code>' Prefix könnte als Abkürzung für "element tree", "embedded markup", oder "encapsulated markup" stehen und kann im Gegansatz zu den Properties auch HTML-Code beinhalten. In hAtom könnte der <code>entry-content</code> zu <code>e-entry-content</code> und bei der hReview die <code>description</code> zur <code>e-description</code> werden.

<h3>'<code>dt-</code>' für DateTime und  '<code>u-</code>' für URL</h3>

Aus <code>dtstart</code> wird <code>dt-start</code> und alle URL-Felder bekommen ein vorgestelltes '<code>u-</code>':

<pre><code>&lt;a class="u-url" href="..."&gt;...&lt;/a&gt;

&lt;img class="u-photo" src="..." /&gt;</code></pre>

Die URL kann in bestimmten Situtionen auch weg fallen, dazu aber im nächsten Beispiel mehr...

<h2 id="uf-v2-simple">Simpel und unabhängig vom Format</h2>

Zukünftig soll es auch nicht mehr so umständlich sein Informationen semantisch auszuzeichnen. Will man derzeit einen simplen Link mit einer <a href="http://microformats.org/wiki/hcard">hCard</a> versehen, muss man ihn wie folgt aufblähen:

<pre><code>&lt;div class="vcard"&gt;
 &lt;a class="url fn" href="http://tantek.com/"&gt;Tantek Çelik&lt;/a&gt;
&lt;/div&gt;</code></pre>

Nach der Überarbeitung soll folgendes reichen:

<pre><code>&lt;a class="h-card" href="http://tantek.com/"&gt;Tantek Çelik&lt;/a&gt;</code></pre>

Dabei gilt die Regel: Wenn es sich bei (z.B.) einer vCard um einen Link oder ein Bild handelt, kann man auf '<code>u-*</code>' und '<code>p-name</code>' verzichten... so ungefär zumindest ;)

Mehr dazu im Microformats-Wiki: <a href="http://microformats.org/wiki/microformats-2-implied-properties">implied properties</a>

Außerdem kommt mit v2 eine Anleitung wie Microformats auf andere Formate wie JSON gemappt werden sollen. Aus...

<pre><code>&lt;a class="h-card" href="http://benward.me"&gt;Ben Ward&lt;/a&gt;</code></pre>

wird...

<pre><code>[{
  "type": ["h-card"],
  "properties": {
    "name": ["Frances Berriman"] 
  }
}]</code></pre>

<h2>Fazit</h2>

Ich bin mir noch nicht ganz sicher was ich von den geplanten Änderungen halten soll... die Nutzung der neuen HTML5 Tags und die Vereinfachung und Vereinheitlichung der Formate finde ich gut und notwendig... Auch eine einheitliche Regel, wie Microformats in anderen Formaten abgebildet werden sollen (z.B. JSON) macht durchaus Sinn (warum das Sinn macht, <a href="http://microformats.org/wiki/JSON">hier</a>)... aber den Pseudo-Namespaces kann ich bisher nichts abgewinnen! Der "Namespace" sorgt zwar für mehr Qualität beim Parsen der Microformats, aber auf Kosten des semantischen HTMLs.

Microformats sollten weiterhin für schönes, semantisches HTML sorgen und mehr nicht. Geht es um maschinenlesbaren Code, sollte man mit der Zeit gehen und auf <a href="http://notiz.blog/2009/06/18/microdata-semantisches-html5/">Microdata</a> oder <a href="http://notiz.blog/2009/07/16/rdfa-wird-wohl-doch-in-html5-integriert/">RDFa</a> setzen. Ob man seinen Quelltext an Microformats v2 anpasst oder mit <a href="http://schema.org/">Schema.org</a> auszeichnet sollte kaum mehr Aufwand sein.

...Übrigens: Wer noch mehr über die Vorteile von Microdata gegenüber Microformats lesen will, sollte sich die <a href="http://notiz.blog/2011/06/21/pfefferles-openweb-microformats-v2/">Ausgabe 10 des Webstandards-Magazin</a> durchlesen oder die Reihe "<a href="http://notiz.blog/2009/08/10/microdata-wie-microformats-bloss-besser-teil-1/">Microdata – wie Microformats bloß besser…</a>" hier im Blog!