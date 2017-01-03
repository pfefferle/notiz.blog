---
ID: 883
post_title: Monkeyformats auf Safari
author: Matthias Pfefferle
post_date: 2008-05-27 18:45:35
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/05/27/monkeyformats-auf-safari/
published: true
aktt_tweeted:
  - "1"
---
<img src="http://notiz.blog/wp-content/uploads/2008/04/monkeyformats.gif" alt="monkeyformats logo" style="float: right; border: none;" />Mit Hilfe des vorhin erwähnten <a href="http://notiz.blog/2008/05/27/greasekit-greasemonkey-fuer-safari/">GreaseKit</a> funktionieren die <a href="http://monkeyformats.org">Monkeyformats</a> jetzt auch im Safari :)

Benötigt wird:

<ul><li><a href="http://www.culater.net/software/SIMBL/SIMBL.php">SIMBL</a></li>
<li><a href="http://8-p.info/greasekit/">GreaseKit</a> (SIMBL Plugin)</li>
<li><a href="http://zappatic.net/safarimicroformats/">Safari Microformats Plugin</a> (SIMBL Plugin)</li></ul>

Und genau in der Reihenfolge sollte man die Tools auch installieren...

<img src="http://notiz.blog/wp-content/uploads/2008/05/monkeyformats-safari.jpg" alt="monkeyformats-safari.jpg" border="0" width="480" height="280" />

Leider funktioniert das Szenario nicht ganz so reibungslos wie auf mit <a href="http://notiz.blog/2008/04/08/monkeyformats/">Firefox + Greasemonkey + Operator</a> da die SIMBL-Plugins wohl in umgekehrter Reihenfolge (zuerst Microformats-Plugin und dann GreaseKit + Monkeyformats) die Seite abarbeiten.

Es gibt aber 'nen kleinen Workaround:
<ul><li>Zuerst die Monkeyformats Seite aufrufen (z.B. Telefonbuch.de wie im Screenshot) - Kein <abbr title="Microformats">&micro;F</abbr>-Icon Sichtbar</li>
<li>Eine Seite mit (nativen) Microformats (z.B. notiz.blog) in neuem Tab öffnen - <abbr title="Microformats">&micro;F</abbr>-Icon Sichtbar</li>
<li>Wieder auf ersten Tab wechseln - <abbr title="Microformats">&micro;F</abbr>-Icon Sichtbar</li></ul>

Das <a href="http://zappatic.net/safarimicroformats/">Safari-Microformats-Plugin</a> ist leider auch noch etwas spartanisch und nicht ganz so komfortabel und flexibel wie <a href="http://notiz.blog/tag/operator/">Operator für Firefox</a>, aber es reicht um <a href="http://microformats.org/wiki/hCard">hCards</a> und <a href="http://microformats.org/wiki/hCal">hCalendars</a> zu verarbeiten.

Schön dass die Idee mit etwas Mehraufwand (aber ohne Anpassungen) auch im Safari funktioniert :)

(via: <a href="http://monkeyformats.org/2008/05/11/safari-support-for-monkeyformats/">monkeyformats.org</a>)