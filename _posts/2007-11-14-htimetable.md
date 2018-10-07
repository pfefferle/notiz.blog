---
ID: 646
post_title: hTimetable
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/11/14/htimetable/
published: true
post_date: 2007-11-14 09:19:34
---
<!-- wp:paragraph -->
<p><strong>...oder "Warum nutzt Bahn.de keine Microformats"?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ich war am Wochenende ein wenig unterwegs und wegen nicht vorhandenem Auto auf öffentliche Verkehrsmittel angewiesen. Das ist ja an sich nichts schlimmes, nur wenn dann noch eine gewisse Ortsunkundigkeit hinzu kommt, wird es problematisch. Dank einem Busfahrer, der die Haltestelle an der ich aussteigen musste (um einen Anschlusszug zu bekommen) einfach ignorierte, durfte ich dann etwas mehr von der Weinheimer Umgebung kennen lernen als mir lieb war.<br/> Jetzt bin ich einer von der Sorte, der aus Zeitgründen natürlich nur die nötigsten Verbindungen raus schreibt... Ich hätte also völlig Hilflos mitten in der Pampa enden können... Gut, es nochmal alles gut gegangen, da ein ich paar Orte weiter eine <abbr title="Oberrheinische Eisenbahngesellschaft AG">OEG</abbr> Haltestelle fand, aber es geht hier ja ums Prinzip.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Und da sind wir schon bei meiner Kritik:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><em>Wieso kann ich mir Bahnverbindungen nicht ohne größeren Aufwand aufs Handy, den PDA oder meinen iPod laden.</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Klar könnte ich mir verschiedene, alternative Verbindungen raus suchen und ausdrucken, aber das setzt einen Drucker voraus.</p>
<!-- /wp:paragraph -->

<!-- wp:more -->
<!--more-->
<!-- /wp:more -->

<!-- wp:paragraph -->
<p>Viel einfacher wäre es doch, wenn die Bahn ihren Fahrplan mit <a href="http://microformats.org/wiki/hcalendar">hCalendar</a> auszeichnen würde, so könnte ich mir meine Verbindung schön aussuchen und mit <a href="http://www.kaply.com/weblog/operator/">Operator</a> als <a href="http://www.ietf.org/rfc/rfc2445.txt">iCalendar</a> abspeichern...</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<div class="wp-block-image"><figure class="aligncenter"><img src="https://notiz.blog/wp-content/uploads/2007/11/bild-3.png" alt="hTimetable"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>...oder mir <a href="http://www.johnmckerrell.com/files/tailsexport-0.3.1-jmck2.xpi">Tails-Export</a> direkt über <a href="https://notiz.blog/2007/05/19/microformats-und-bluetooth/">Bluetooth</a> ans Handy schicken.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Der Code könnte wie folgend aussehen:
</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;tr class="vevent">
  &lt;td class="summary">
    &lt;a class="url" href="http://example.com">&lt;span class="location">Abfahrtsort &lt;br />
    Zielort&lt;/span>&lt;/a>
  &lt;/td>
  &lt;td>
    Ab &lt;abbr class="dtstart" title="2007-10-13">13. Oktober 22:43&lt;/abbr>  &lt;br />
    An &lt;abbr class="dtend" title="2007-10-13">13. Oktober 22:43&lt;/abbr>
  &lt;/td>
  &lt;td>
    ...
  &lt;/td>
&lt;/tr></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Liebe <abbr title="Deutsche Bahn">DB</abbr> bitte ändert euer Template und führt Microformats ein.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Und am Wochenende muss ich mit der Bahn in den tiefsten Schwarzwald und es sind Streiks angesagt... Ich hoffe das geht gut :)</p>
<!-- /wp:paragraph -->