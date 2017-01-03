---
ID: 257
post_title: Microformats
author: Matthias Pfefferle
post_date: 2006-11-20 19:53:43
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2006/11/20/microformats/
published: true
---
<img id="image258" src="http://notiz.blog/wp-content/uploads/2006/11/microformats.jpg" alt="microformats.jpg" style="float: right; border: 0 none;" />Wenn man in letzter Zeit durchs Internet surft, stolpert man immer häufiger über den Begriff "<a href="http://microformats.org/">Microformats</a>" oder sieht das grüne Symbol auf Kontaktseiten. Aber was genau sind Microformats und für was sind sie gut?

<a href="http://de.wikipedia.org/wiki/Microformats">Wikipedia</a> meint dazu:
<blockquote>Ein Mikroformat ist ein Markup-Format zur semantischen Annotation von HTML oder XHTML. Mikroformat-Annotationen können leicht aus Webseiten extrahiert werden und machen weiteren Programmen (etwa Suchmaschinen) die Bedeutung des Seiteninhalts verständlich.</blockquote>
<!--more-->
Das heißt, es werden vorhantenen Attributen (class, rel, rev) von <abbr title="(Extensible) HyperText Markup Language">(X)HTML</abbr> verwendet um neue Formate zu speziellen Themen- oder Wissensgebieten zu erstellen.

Eines der ersten Formate war <abbr title="Xhtml Friends Network"><a href="http://gmpg.org/xfn/">XFN</a></abbr>, es verwendt den "rel" Tag um persönliche Verbindungen über Links anzuzeigen.
<div class="info">&lt;a href="http://pinki-tine.blogspot.com/" rel="friend met colleague"&gt;...</div>Eine Anleitung und eine Liste von möglichen "rel"-Tags findet ihr <a href="http://gmpg.org/xfn/join">hier</a>.

Ein zweites erwähnenswertes Format ist "<a href="http://microformats.org/wiki/hcard">hCard</a>". Es ist ein Versuch einen Onlinestandard für Kontakte zu erstellen.
<pre><p class="code">&lt;div class="vcard"&gt;
  &lt;a class="url fn" href="http://example.com">
    Max Mustermann&lt;/a&gt;
  &lt;a class="email" href="
    mailto:max.mustermann@example.com"&gt;
    max.mustermann@example.com&lt;/a&gt;
  &lt;div class="adr"&gt;
    &lt;div class="street-address"&gt;Musterstr.&lt;/div&gt;
    &lt;span class="locality"&gt;Musterstadt&lt;/span&gt;,
    &lt;span class="region"&gt;MP&lt;/span&gt;, 
    &lt;span class="postal-code"&gt;11111&lt;/span&gt;
    &lt;span class="country-name"&gt;Germany&lt;/span&gt;
  &lt;/div&gt;
  &lt;div class="tel"&gt;111 111 111&lt;/div&gt;
&lt;/div&gt;</p></pre>
(Für Faule: Ein <a href="http://microformats.org/code/hcard/creator">hCard Creator</a>)
Der Vorteil eines solchen Formates, er ist maschinen-lesbar. Das heißt es ist möglich über z.B. <abbr title="Extensible Stylesheet Language">XSL</abbr> Schnittstellen eine <a href="http://de.wikipedia.org/wiki/VCard">vCard</a> zu erstellen. <a href="http://technorati.com">Technorati</a> z.B. bietet eine solche <a href="http://technorati.com/contact/">Schnittstelle</a>:
<div class="info">http://technorati.com/contact/http://notiz.blog/kontakt/</div>
Die Technorati Engine sucht auf der übermittelten Seite nach einer hCard und wandelt diese in eine vCard um. Auch die Firma Apple, welche die vCard für ihr <a href="http://www.apple.com/de/macosx/features/addressbook/">Adressbuch</a> verwendet, nutzt das <a href="http://microformats.org/blog/2006/10/31/dotmac-webmail-implements-hcard/">hCard-Format für ihr Onlineangebot</a> <a href="http://www.apple.com/de/dotmac/">.Mac</a>.
Auf der Seite <a href="http://suda.co.uk/projects/X2V/">suda.co.uk</a> gibt es Links und Informationen zu weiteren Implementierungs-Möglichkeiten.
Das Problem bei dem ganzen ist, dass es Spammer dadurch noch leichter haben an komplette Adressen zu kommen...

Ein enormer Vorteil dieser Formate ist die Möglichkeit Search Engines in soweit anzupassen, dass sie anhand von XFN Soziale Netzte abzubilden oder dank hCard sogar telefonbuch.de abzulösen. Mal schaun wohin die Reise geht...

Weitere Formate sind <a href="http://microformats.org/wiki/hcalendar">vCalendar</a>, <a href="http://microformats.org/wiki/xoxo">XOXO</a>, <a href="http://microformats.org/wiki/hreview">hReview</a>, <a href="http://microformats.org/wiki/">uvm.</a>