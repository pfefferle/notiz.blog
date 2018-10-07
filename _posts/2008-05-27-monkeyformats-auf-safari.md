---
ID: 883
post_title: Monkeyformats auf Safari
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/05/27/monkeyformats-auf-safari/
published: true
post_date: 2008-05-27 18:45:35
---
<!-- wp:image {"align":"right"} -->
<figure class="wp-block-image alignright"><img src="https://notiz.blog/wp-content/uploads/2008/04/monkeyformats.gif" alt="monkeyformats logo" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Mit Hilfe des vorhin erwähnten <a href="https://notiz.blog/2008/05/27/greasekit-greasemonkey-fuer-safari/">GreaseKit</a> funktionieren die <a href="http://monkeyformats.org">Monkeyformats</a> jetzt auch im Safari :)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Benötigt wird:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><a href="http://www.culater.net/software/SIMBL/SIMBL.php">SIMBL</a></li>
	<li><a href="http://8-p.info/greasekit/">GreaseKit</a> (SIMBL Plugin)</li>
	<li><a href="http://zappatic.net/safarimicroformats/">Safari Microformats Plugin</a> (SIMBL Plugin)</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Und genau in der Reihenfolge sollte man die Tools auch installieren...</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/05/monkeyformats-safari.jpg" alt="monkeyformats-safari.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Leider funktioniert das Szenario nicht ganz so reibungslos wie auf mit <a href="https://notiz.blog/2008/04/08/monkeyformats/">Firefox + Greasemonkey + Operator</a> da die SIMBL-Plugins wohl in umgekehrter Reihenfolge (zuerst Microformats-Plugin und dann GreaseKit + Monkeyformats) die Seite abarbeiten.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Es gibt aber 'nen kleinen Workaround:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li>Zuerst die Monkeyformats Seite aufrufen (z.B. Telefonbuch.de wie im Screenshot) - Kein <abbr title="Microformats">µF</abbr>-Icon Sichtbar</li>
	<li>Eine Seite mit (nativen) Microformats (z.B. notiz.blog) in neuem Tab öffnen - <abbr title="Microformats">µF</abbr>-Icon Sichtbar</li>
	<li>Wieder auf ersten Tab wechseln - <abbr title="Microformats">µF</abbr>-Icon Sichtbar</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Das <a href="http://zappatic.net/safarimicroformats/">Safari-Microformats-Plugin</a> ist leider auch noch etwas spartanisch und nicht ganz so komfortabel und flexibel wie <a href="https://notiz.blog/tag/operator/">Operator für Firefox</a>, aber es reicht um <a href="http://microformats.org/wiki/hCard">hCards</a> und <a href="http://microformats.org/wiki/hCal">hCalendars</a> zu verarbeiten.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Schön dass die Idee mit etwas Mehraufwand (aber ohne Anpassungen) auch im Safari funktioniert :)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>(via: <a href="http://monkeyformats.org/2008/05/11/safari-support-for-monkeyformats/">monkeyformats.org</a>)</p>
<!-- /wp:paragraph -->