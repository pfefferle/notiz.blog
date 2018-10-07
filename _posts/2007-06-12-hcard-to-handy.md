---
ID: 472
post_title: hCard to Phone
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/06/12/hcard-to-handy/
published: true
post_date: 2007-06-12 19:37:12
---
<!-- wp:paragraph -->
<p>Wie schon erwähnt, hat <a href="http://pixelsebi.com/">Sebastian Küppers</a> auf seinem Weblog eine schöne <a href="http://pixelsebi.com/2007-06-11/hcard-via-qr-code-via-vcard-to-phone/">Anleitung</a> geschrieben wie man eine <a href="http://microformats.org/wiki/hcard">hCard</a> über <a href="http://de.wikipedia.org/wiki/QR_Code">QR-Taggs</a> auf das Handy bekommt. Das Problem bei der Sache ist nur, dass bei langen URLs der Tagg sehr groß wird und dadurch schwer mit Handys zu lesen ist. Deshalb würde ich noch einen Schritt mehr einfügen...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ursprüngliche URL um die hCard mit Hilfe von <a href="http://suda.co.uk/projects/X2V/">Brian Surdas XSLT</a> in eine vCard zu parsen: http://suda.co.uk/projects/microformats/hcard/get-contact.php
	<br/> ?uri=https://notiz.blog/kontakt/
</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Der Tagg würde für diese URL so aussehen:</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="http://qrcode.kaywa.com/img.php?s=6&amp;d=http%3A%2F%2Fsuda.co.uk%2Fprojects%2Fmicroformats%2Fhcard%2Fget-contact.php%3Furi%3Dhttp%3A%2F%2Fnotiz.blog%2Fkontakt%2F" alt="qrcode" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Mein Idee wäre, die URL mit einem Dienst wie <a href="http://tinyurl.com/">TinyUrl</a> oder <a href="http://urltea.com/">urlTea</a> zu verkürzen: http://urltea.com/r43
</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Der entsprechende Tagg ist somit viel kleiner und für Handys besser lesbar:</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="http://qrcode.kaywa.com/img.php?s=6&amp;d=http%3A%2F%2Furltea.com%2Fr43" alt="qrcode" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Ich hab das Ganze mit meinem Sony Ericsson W810i getestet und es funktioniert super. Um das ganze zu automatisieren gibt es für QR-Code eine <a href="http://api.qrcode.kaywa.com/">API von Kayawa</a> und auch urlTea hat eine <a href="http://urltea.com/api/">API</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Mal schaun ob sich da was basteln lässt oder ob es doch ne sinnvollere Variante gibt die vCard direkt in den Code zu packen, ohne dass dieser zu groß wird...</p>
<!-- /wp:paragraph -->