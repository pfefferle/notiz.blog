---
ID: 920
post_title: >
  BBC und das alte hAccessibility
  Problemchen
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/06/24/bbc-und-das-alte-haccessibility-problemchen/
published: true
post_date: 2008-06-24 18:15:52
---
<!-- wp:paragraph -->
<p>Dass die <a href="http://microformats.org/wiki/abbr-design-pattern">abbr-design-pattern</a> nicht das gelbe vom Ei sind (massive Probleme mit Screen-Readern), hat das <a href="http://www.webstandards.org/">Web Standards Project (WaSP)</a> schon vor <a href="https://notiz.blog/2007/04/28/die-abbr-design-pattern/">mehr als einem Jahr festgestellt</a>, aber es bedarf meistens etwas Druck von außen damit sich wirklich etwas ändert.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Nach der <a href="http://www.bbc.co.uk/blogs/radiolabs/2008/06/removing_microformats_from_bbc.shtml">Ankündigung der <abbr title="British Broadcasting Corporation">BBC</abbr></a>, alle <a href="http://microformats.org">Microformats</a> (die das abbr-design-pattern verwenden) von ihren Seiten (speziell bbc.co.uk/programmes) zu nehmen, ist <a href="http://microformats.org/discuss/mail/microformats-discuss/2007-April/009350.html">die alte Diskussion</a> <a href="http://microformats.org/discuss/mail/microformats-dev/2008-June/000552.html">wieder in vollem Gange</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Diskutierte Lösungen:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><code>&lt;span class="dtstart data-20051010T10:10:10-0100">10 o'clock on the 10th&lt;/span></code></li>
	<li><code>&lt;span class="dtstart{2005-10-10T10:10:10-0100}">10 o'clock&lt;/span></code></li>
	<li><code>&lt;abbr class="dtstart data{2008-06-23}" title=June 23rd, 2008">Today&lt;/abbr></code></li>
	<li><code>&lt;abbr class="fancy data{2008-06-23} dstart" title=June 23rd, 2008">Today&lt;/abbr></code></li>
	<li><code>&lt;span class="dtstart" content="2008-06-23">Today&lt;/span></code> (Nicht XHTML 1.x valide)</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Noch mehr Infos zu dem Thema bekommt man im <a href="http://microformats.org/wiki/datetime-design-pattern#Machine-data_in_class">Wiki</a> oder über die <a href="http://microformats.org/discuss/mail/microformats-dev/2008-June/000552.html">Mailing-Liste</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>(via <a href="http://hackr.de/2008/06/24/accessibility-vs-machines">hackr</a>)</p>
<!-- /wp:paragraph -->