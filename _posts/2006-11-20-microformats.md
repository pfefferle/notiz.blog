---
ID: 257
post_title: Microformats
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2006/11/20/microformats/
published: true
post_date: 2006-11-20 19:53:43
---
<!-- wp:image {"align":"right"} -->
<figure class="wp-block-image alignright"><img src="https://notiz.blog/wp-content/uploads/2006/11/microformats.jpg" alt="microformats.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Wenn man in letzter Zeit durchs Internet surft, stolpert man immer häufiger über den Begriff "<a href="http://microformats.org/">Microformats</a>" oder sieht das grüne Symbol auf Kontaktseiten. Aber was genau sind Microformats und für was sind sie gut?</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="http://de.wikipedia.org/wiki/Microformats">Wikipedia</a> meint dazu:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Ein Mikroformat ist ein Markup-Format zur semantischen Annotation von HTML oder XHTML. Mikroformat-Annotationen können leicht aus Webseiten extrahiert werden und machen weiteren Programmen (etwa Suchmaschinen) die Bedeutung des Seiteninhalts verständlich.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p><br/> Das heißt, es werden vorhantenen Attributen (class, rel, rev) von <abbr title="(Extensible) HyperText Markup Language">(X)HTML</abbr> verwendet um neue Formate zu speziellen Themen- oder Wissensgebieten zu erstellen.</p>
<!-- /wp:paragraph -->

<!-- wp:more -->
<!--more-->
<!-- /wp:more -->

<!-- wp:paragraph -->
<p>Eines der ersten Formate war <abbr title="Xhtml Friends Network"><a href="http://gmpg.org/xfn/">XFN</a></abbr>, es verwendt den "rel" Tag um persönliche Verbindungen über Links anzuzeigen. &lt;a href="http://pinki-tine.blogspot.com/" rel="friend met colleague">...
</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Eine Anleitung und eine Liste von möglichen "rel"-Tags findet ihr <a href="http://gmpg.org/xfn/join">hier</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ein zweites erwähnenswertes Format ist "<a href="http://microformats.org/wiki/hcard">hCard</a>". Es ist ein Versuch einen Onlinestandard für Kontakte zu erstellen.
</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">&lt;div class="vcard">
  &lt;a class="url fn" href="http://example.com">
    Max Mustermann&lt;/a>
  &lt;a class="email" href="
    mailto:max.mustermann@example.com">
    max.mustermann@example.com&lt;/a>
  &lt;div class="adr">
    &lt;div class="street-address">Musterstr.&lt;/div>
    &lt;span class="locality">Musterstadt&lt;/span>,
    &lt;span class="region">MP&lt;/span>, 
    &lt;span class="postal-code">11111&lt;/span>
    &lt;span class="country-name">Germany&lt;/span>
  &lt;/div>
  &lt;div class="tel">111 111 111&lt;/div>
&lt;/div></pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>(Für Faule: Ein <a href="http://microformats.org/code/hcard/creator">hCard Creator</a>)<br/> Der Vorteil eines solchen Formates, er ist maschinen-lesbar. Das heißt es ist möglich über z.B. <abbr title="Extensible Stylesheet Language">XSL</abbr> Schnittstellen eine <a href="http://de.wikipedia.org/wiki/VCard">vCard</a> zu erstellen. <a href="http://technorati.com">Technorati</a> z.B. bietet eine solche <a href="http://technorati.com/contact/">Schnittstelle</a>: http://technorati.com/contact/https://notiz.blog/kontakt/
</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Die Technorati Engine sucht auf der übermittelten Seite nach einer hCard und wandelt diese in eine vCard um. Auch die Firma Apple, welche die vCard für ihr <a href="http://www.apple.com/de/macosx/features/addressbook/">Adressbuch</a> verwendet, nutzt das <a href="http://microformats.org/blog/2006/10/31/dotmac-webmail-implements-hcard/">hCard-Format für ihr Onlineangebot</a> <a href="http://www.apple.com/de/dotmac/">.Mac</a>.<br/> Auf der Seite <a href="http://suda.co.uk/projects/X2V/">suda.co.uk</a> gibt es Links und Informationen zu weiteren Implementierungs-Möglichkeiten.<br/> Das Problem bei dem ganzen ist, dass es Spammer dadurch noch leichter haben an komplette Adressen zu kommen...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ein enormer Vorteil dieser Formate ist die Möglichkeit Search Engines in soweit anzupassen, dass sie anhand von XFN Soziale Netzte abzubilden oder dank hCard sogar telefonbuch.de abzulösen. Mal schaun wohin die Reise geht...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Weitere Formate sind <a href="http://microformats.org/wiki/hcalendar">vCalendar</a>, <a href="http://microformats.org/wiki/xoxo">XOXO</a>, <a href="http://microformats.org/wiki/hreview">hReview</a>, <a href="http://microformats.org/wiki/">uvm.</a></p>
<!-- /wp:paragraph -->