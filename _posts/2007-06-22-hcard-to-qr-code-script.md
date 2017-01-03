---
ID: 495
post_title: hCard to QR-Code Script
author: Matthias Pfefferle
post_date: 2007-06-22 19:47:05
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/06/22/hcard-to-qr-code-script/
published: true
---
<a href="http://pixelsebi.com/2007-06-11/hcard-via-qr-code-via-vcard-to-phone/">Sebastian Küpers</a> hatte ja vor kurzem die tolle Idee <a href="http://microformats/wiki/hCard">hCards</a> mittels <a href="http://de.wikipedia.org/wiki/QR_Code">QR-Code</a> aufs Handy zu bekommen...
Ich hab mir jetzt mal alle möglichen Varianten überlegt um das ganze zu automatisieren und eine kleine PHP Klasse geschrieben. 
Die Klasse verwendet <a href="http://suda.co.uk/projects/X2V/">Brian Sudas X2V</a> um die vCard zu parsen, die <a href="http://urltea.com/api/">urlTea API</a> um die URLs zu verkürzen und die <a href="http://api.qrcode.kaywa.com/">Kaywa API</a> um den QR-Code zu erstellen.

Ausprobieren könnt ihr das ganze auf: <a href="http://www.microform.at/hcard2qrcode/">www.microform.at/hcard2qrcode/</a>

Download: <a href="http://www.microform.at/download/hqr_v1.rar">hqr_v1.rar</a>