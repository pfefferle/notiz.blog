---
ID: 646
post_title: hTimetable
author: Matthias Pfefferle
post_date: 2007-11-14 09:19:34
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/11/14/htimetable/
published: true
---
<strong>...oder "Warum nutzt Bahn.de keine Microformats"?</strong>

Ich war am Wochenende ein wenig unterwegs und wegen nicht vorhandenem Auto auf öffentliche Verkehrsmittel angewiesen. Das ist ja an sich nichts schlimmes, nur wenn dann noch eine gewisse Ortsunkundigkeit hinzu kommt, wird es problematisch. Dank einem Busfahrer, der die Haltestelle an der ich aussteigen musste (um einen Anschlusszug zu bekommen) einfach ignorierte, durfte ich dann etwas mehr von der Weinheimer Umgebung kennen lernen als mir lieb war.
Jetzt bin ich einer von der Sorte, der aus Zeitgründen natürlich nur die nötigsten Verbindungen raus schreibt... Ich hätte also völlig Hilflos mitten in der Pampa enden können... Gut, es nochmal alles gut gegangen, da ein ich paar Orte weiter eine <abbr title="Oberrheinische Eisenbahngesellschaft AG">OEG</abbr> Haltestelle fand, aber es geht hier ja ums Prinzip.

Und da sind wir schon bei meiner Kritik:

<em>Wieso kann ich mir Bahnverbindungen nicht ohne größeren Aufwand aufs Handy, den PDA oder meinen iPod laden.</em>

<!--more-->Klar könnte ich mir verschiedene, alternative Verbindungen raus suchen und ausdrucken, aber das setzt einen Drucker voraus.

Viel einfacher wäre es doch, wenn die Bahn ihren Fahrplan mit <a href="http://microformats.org/wiki/hcalendar">hCalendar</a> auszeichnen würde, so könnte ich mir meine Verbindung schön aussuchen und mit <a href="http://www.kaply.com/weblog/operator/">Operator</a> als <a href="http://www.ietf.org/rfc/rfc2445.txt">iCalendar</a> abspeichern...

<img src='http://notiz.blog/wp-content/uploads/2007/11/bild-3.png' alt='hTimetable' />

...oder mir <a href="http://www.johnmckerrell.com/files/tailsexport-0.3.1-jmck2.xpi">Tails-Export</a> direkt über <a href="http://notiz.blog/2007/05/19/microformats-und-bluetooth/">Bluetooth</a> ans Handy schicken.

Der Code könnte wie folgend aussehen:
<pre class="code">
&lt;tr class=&quot;vevent&quot;&gt;<br>
  &lt;td class=&quot;summary&quot;&gt;<br>
    &lt;a class=&quot;url&quot; href=&quot;http://example.com&quot;&gt;&lt;span class=&quot;location&quot;&gt;Abfahrtsort &lt;br /&gt;<br>
    Zielort&lt;/span&gt;&lt;/a&gt;<br>
  &lt;/td&gt;<br>
  &lt;td&gt;<br>
    Ab &lt;abbr class=&quot;dtstart&quot; title=&quot;2007-10-13&quot;&gt;13. Oktober 22:43&lt;/abbr&gt;  &lt;br /&gt;<br>
    An &lt;abbr class=&quot;dtend&quot; title=&quot;2007-10-13&quot;&gt;13. Oktober 22:43&lt;/abbr&gt;<br>
  &lt;/td&gt;<br>
  &lt;td&gt;<br>
    ...<br>
  &lt;/td&gt;<br>
&lt;/tr&gt;
</pre>

Liebe <abbr title="Deutsche Bahn">DB</abbr> bitte ändert euer Template und führt Microformats ein.

Und am Wochenende muss ich mit der Bahn in den tiefsten Schwarzwald und es sind Streiks angesagt... Ich hoffe das geht gut :)