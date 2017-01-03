---
ID: 472
post_title: hCard to Phone
author: Matthias Pfefferle
post_date: 2007-06-12 19:37:12
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/06/12/hcard-to-handy/
published: true
---
Wie schon erwähnt, hat <a href="http://pixelsebi.com/">Sebastian Küppers</a> auf seinem Weblog eine schöne <a href="http://pixelsebi.com/2007-06-11/hcard-via-qr-code-via-vcard-to-phone/">Anleitung</a> geschrieben wie man eine <a href="http://microformats.org/wiki/hcard">hCard</a> über <a href="http://de.wikipedia.org/wiki/QR_Code">QR-Taggs</a> auf das Handy bekommt. Das Problem bei der Sache ist nur, dass bei langen URLs der Tagg sehr groß wird und dadurch schwer mit Handys zu lesen ist. Deshalb würde ich noch einen Schritt mehr einfügen...

Ursprüngliche URL um die hCard mit Hilfe von <a href="http://suda.co.uk/projects/X2V/">Brian Surdas XSLT</a> in eine vCard zu parsen:

<div class="info">http://suda.co.uk/projects/microformats/hcard/get-contact.php
?uri=http://notiz.blog/kontakt/</div>

Der Tagg würde für diese URL so aussehen:

<img src="http://qrcode.kaywa.com/img.php?s=6&d=http%3A%2F%2Fsuda.co.uk%2Fprojects%2Fmicroformats%2Fhcard%2Fget-contact.php%3Furi%3Dhttp%3A%2F%2Fnotiz.blog%2Fkontakt%2F" alt="qrcode"  />

Mein Idee wäre, die URL mit einem Dienst wie <a href="http://tinyurl.com/">TinyUrl</a> oder <a href="http://urltea.com/">urlTea</a> zu verkürzen:

<div class="info">http://urltea.com/r43</div>

Der entsprechende Tagg ist somit viel kleiner und für Handys besser lesbar:

<img src="http://qrcode.kaywa.com/img.php?s=6&d=http%3A%2F%2Furltea.com%2Fr43" alt="qrcode"  />

Ich hab das Ganze mit meinem Sony Ericsson W810i getestet und es funktioniert super. Um das ganze zu automatisieren gibt es für QR-Code eine <a href="http://api.qrcode.kaywa.com/">API von Kayawa</a> und auch urlTea hat eine <a href="http://urltea.com/api/">API</a>.

Mal schaun ob sich da was basteln lässt oder ob es doch ne sinnvollere Variante gibt die vCard direkt in den Code zu packen, ohne dass dieser zu groß wird...