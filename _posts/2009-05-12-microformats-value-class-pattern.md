---
ID: 1539
post_title: 'Microformats: Value Class Pattern'
author: Matthias Pfefferle
post_date: 2009-05-12 19:33:05
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/05/12/microformats-value-class-pattern/
published: true
aktt_notify_twitter:
  - 'yes'
aktt_tweeted:
  - "1"
---
Das bisher wohl größte Problem bei der Verwendung von <strong>Microformats</strong> ist (oder besser wahr) die <a href="http://notiz.blog/?s=haccessibility">Accessibility</a> durch die etwas zweckentfremdete Verwendung des <a href="http://microformats.org/wiki/abbr-design-pattern"><code>&lt;abbr /&gt;</code>-Tags</a>.

Das so genanntes <a href="http://microformats.org/wiki/abbr-design-pattern">abbr-design-pattern</a> diente hauptsächlich dazu (es gibt noch einige andere Anwendungsfälle), ein für den Menschen lesbares Datum auch für die Maschine lesbar zu machen und ist Bestandteil von <strong>Mikroformaten</strong> wie z.B. <a href="http://microformats.org/wiki/hCalendar">hCalendar</a>, <a href="http://microformats.org/wiki/hAtom">hAtom</a> oder <a href="http://microformats.org/wiki/hReview">hReview</a>.

Ein Beispiel: <code>&lt;abbr class="dtstart" title="2009-05-12"&gt;heute&lt;/abbr&gt;</code>

<a href="http://de.selfhtml.org/html/text/logisch.htm#elemente">SelfHTML über das abbr-Element</a>:

<blockquote>zeichnet einen Text aus mit der Bedeutung "dies ist eine Abkürzung"</blockquote>

Selbst wenn man davon ausgeht, dass das Wort <em>heute</em> eine Abkürzung für das volle Datum <em>2009-05-12</em> ist, gibt es ein großes Problem mit Screen-Readern. Die meisten Screen-Reader sind so konfiguriert, dass sie statt der Abkürzung, das im title-Attribut angegebene, vollständige Wort lesen.
Im Falle der <a href="http://microformats.org/wiki/abbr-design-pattern">abbr-design-pattern</a> im oben genannten Beispiel wäre das <em>2009-05-12</em> (gelesen "Zweitausendneun minus Fünf minus Zwölf"), also viel missverständlicher als <em>heute</em>.

Das <a href="http://microformats.org/blog/2009/05/12/value-class-pattern/">gerade angekündigte</a> <strong><a href="http://microformats.org/wiki/value-class-pattern">value-class-pattern</a></strong> soll dieses (und einige andere) Problem jetzt beheben.

Ein Datum, wie im Beispiel oben, würde mit dem <strong>value-class-pattern</strong> folgendermaßen aussehen:

<pre>&lt;span class='dtstart'&gt;
  &lt;span class='value-title' title='2009-05-12'&gt; &lt;/span&gt;
  heute
&lt;/span&gt;</pre>

Erklärung:

<ul><li><em>dtstart</em> gibt immer noch an, dass es sich bei dem folgenden um ein Datum handelt</li>
<li>Die folgende Klasse: <em>value-title</em> gibt an, dass sich <em>dtstart</em> auf das <em>title</em>-Attribut des <em>spans</em> bezieht</li>
<li>Im <em>title</em> steht der maschinen-lesbare text</li></ul>

Das neue Pattern beschreibt aber noch eine ganze Reihe an anderen Anwendungsfällen, am besten ihr überfliegt die Seite einfach mal selbst: <a href="http://microformats.org/wiki/value-class-pattern">http://microformats.org/wiki/value-class-pattern</a>

...es sind übrigens alle Microformats-Nutzer aufgerufen, ihre Seiten und Parser auf das neue Pattern umzustellen, also viel Spaß dabei :)