---
ID: 660
post_title: 'APML &#8211; Attention Profiling Mark-up Language'
author: Matthias Pfefferle
post_date: 2007-11-23 09:14:25
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/11/23/apml-attention-profiling-mark-up-language/
published: true
---
<img src='http://notiz.blog/wp-content/uploads/2007/11/apml-logo.png' alt='APML Logo' />

Bei <a href="http://pixelsebi.com/2007-06-04/attention-daten-in-metaversen/">Sebastian Küpers</a> habe ich das erste Mal etwas über <a href="http://www.apml.org"><abbr title="Attention Profiling Mark-up Language">APML</abbr></a> gelesen, mich aber nicht weiter damit beschäftigt... Jetzt bin ich letzte Woche über <a href="http://dataportability.org/">dataportability.org</a> nochmal auf das Thema gestoßen und hab mir das ganze mal etwas näher angesehen.

APML steht für <em>Attention Profiling Mark-up Language</em> und bietet ein Format, Attention Daten darzustellen und portabel zu machen.
<blockquote cite="http://apml.org">APML allows users to share their own personal Attention Profile in much the same way that OPML allows the exchange of reading lists between News Readers.</blockquote>

Die Idee hinter APML ist, einen Offenen Standard zu schaffen, der es Benutzern erlaubt Attention Daten zu erstellen und diese Systemunabhängig zu nutzen. Mit APML wäre es z.B. möglich seine Interessen von einer Community in eine andere mit zu nehmen um schon gleich nach der Anmeldung, den eigenen Interessen entsprechende Inhalte angezeigt zu bekommen.

Eine Attention sieht folgendermaßen aus:
<code>&lt;Concept key=&quot;Microformats&quot; value=&quot;1&quot; from=&quot;notiz.blog&quot; updated=&quot;2007-11-23T08:39:04&quot;/&gt;</code>

Beschreibung:
<ul><li><em>key</em> bezeichnet die Attention, also das <em>Interesse</em> das ich habe.</li>
<li><em>value</em> gibt an wie groß das Interesse ist.</li></ul>

Der Wert <em>value</em> muss zwischen 1 (sehr interessant) und -1 (nicht interessant) liegen.

... und da ich das Ganze natürlich auch immer ausprobieren muss, habe ich ein kleines Script geschrieben welches die WordPress Tags und Categories im APML Format ausgibt.

Link: <a href="http://notiz.blog/wp-apml.php">http://notiz.blog/wp-apml.php</a>

Wenn ihr noch Anregungen habt lasst sie mich bitte wissen, wenn nicht biete ich das Script demnächst mal zum Download an.