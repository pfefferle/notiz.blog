---
ID: 872
post_title: Die Zukunft der Microformats
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/05/24/die-zukunft-der-microformats/
published: true
post_date: 2008-05-24 14:12:12
---
<!-- wp:image {"align":"right"} -->
<figure class="wp-block-image alignright"><img src="https://notiz.blog/wp-content/uploads/2006/11/microformats.jpg" alt="microformats.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Da ich mich in den letzten Monaten viel mit Themen wie <a href="https://notiz.blog/tag/dataportability/">DataPortability</a> oder dem <a href="https://notiz.blog/tag/semantic-web/">Semantic Web</a> beschäftigt habe, kam mir die Frage welche Rolle <a href="http://microformats.org">Microformats</a> in Zukunft einnehmen werden.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>Microformats und DataPortability</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Bisher sind zwei (mit hAtom drei) Mikroformate im DataPortability-Konzept enthalten:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><a href="http://wiki.dataportability.org/display/dpmain/DP-REC-006+Profile+Definitions">hCard</a> - zum Austausch von Profildaten</li>
	<li><a href="http://wiki.dataportability.org/display/dpmain/DP-REC-007+Contact+List+Definitions">XFN</a> - zum Austausch von Freundschafts-Netzen</li>
	<li>(hAtom - als Alternative zu ATOM oder RSS)</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Ich denke aber nicht, dass Microformats (zumindest in der klassischen HTML-Version) über längeren Zeitraum diese Position in der DataPortability-Idee einnehmen werden. Microformats sind zwar weit verbreitete und simple Formate um Informationen semantisch aufzubereiten, sind aber schwer zu parsen (HTML) und bieten keinen wirklichen Authentifizierungsmechanismus (da sie direkt im HTML-Quelltext stehen).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ich bin der Meinung dass OpenID und FoaF alle Eigenschaften von Microformats auf eine wesentlich bessere Weise lösen können. FoaF ist losgelöst von der normalen Webseite und kann so problemlos über OAuth oder OpenID geschützt werden und bildet sogar Profildaten und Freundesnetze ab. Noch einfacher wäre <a href="http://openid.net/specs/openid-attribute-exchange-1_0.html">OpenID Attribute Exchange</a>, da so SingleSignOn, Portabilität und Authentifizierung mit einem Standard abgedeckt sind.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Den einzigen <abbr title="DataPortability">DP</abbr>-Anwendungsfall den ich mir für Microformats vorstellen könnte wäre eine Alternativ-Form (zu HTML) wie z.B. <a href="http://microformats.org/wiki/jcard">JSON</a> oder <a href="http://microformatique.com/optimus/?uri=http%3A%2F%2Fnotiz.blog&amp;format=xml&amp;function=&amp;filter=hcard">XML</a>, da sie sich im Gegensatz zu <a href="https://notiz.blog/2007/11/04/hcard-als-attribute-exchange-fuer-openid/">Attribute Exchange</a> oder FoaF an bestehende Standards (z.B. vCard) halten und wohl definiert sind, würde aber nicht mehr viel mit der klassischen Idee der Microformats zu tun haben.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>Microformats und das Semantic Web</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Microformats werden auch immer wieder (fälschlicherweise) als Teil des Semantic Web bezeichnet und lassen sich dank <a href="http://pixelsebi.com/2006-10-24/grddl-schlagt-die-brucke-zu-rdf/">GRDDL</a> auch problemlos in dieses integrieren, bieten aber sonst keinerlei Semantic-Web-Eigenschaften. Nach der Veröffentlichung von RDFa haben Microformats aber auch einen schlechten Stand als "real world semantics".</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ein wesentliches Defizit der <abbr title="Microformats">µF</abbr> im Vergleich zu RDFa ist die schlechte Skalierbarkeit und das Problem der fehlenden <a href="http://www.w3.org/TR/rdf-concepts/#section-triples">Triples</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Sieht man das <em>Semantische Web</em> als Zukunft des Internets, werden <abbr title="Microformats">µF</abbr> wohl in nächster Zeit auch auf diesem Gebiet von dem wesentlich semantischeren RDFa abgelöst.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>Jedem offenen Standard eine Nische</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Bei Medientheoretikern gibt es die <a href="http://viadrina.euv-frankfurt-o.de/~sk/soemz03/verdraengung.html">These</a> dass "<em>bislang noch kein Medium von einem anderen überflüssig oder verdrängt worden wäre</em>", warum sollte das nicht auch für offene Standards gelten :)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ich kann mir zwei sinnvolle Anwendungsgebiete für Microformats vorstellen (über die ich auch noch etwas detaillierter schreiben möchte), in denen es (noch) keine bessere Alternative gibt.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"left"} -->
<figure class="wp-block-image alignleft"><img src="https://notiz.blog/wp-content/uploads/2008/05/searchmonkeylogo147x150.gif" alt="searchmonkeyLogo147x150.gif" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Microformats sind direkt in die Webseite integriert und benötigen keinen Backchannel wie z.B. bei XML-Schnittstellen wie RSS, deshalb bietet es auch eine Ideallösung für Semantische Suchmaschinen wie z.B. <a href="http://developer.yahoo.com/searchmonkey/">Yahoo!s Search Monkey</a> oder <a href="http://kitchen.technorati.com/">Technorati Kitchen</a>. Suchmaschinen haben durch <abbr title="Microformats">µF</abbr> die einmalige Möglichkeit, strukturierte Inhalte zu indexieren und auf deren Basis, Systeme wie z.B. Kalender, online Telefonbücher und Musiksuchen abzubilden. Hier haben Mikroformate durch die Anzahl der schon definierten Formate und deren weite Verbreitung auch einen enormen Vorteil gegenüber RDFa.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Eine zweite Niesche beschreibt Sascha Konietzke in seinem Artikel <em><a href="http://www.funkfeuer.net/2008/04/14/what-are-microformats-and-what-do-they-mean-to-mobile/">What Are Microformats and What Do They Mean to Mobile?</a></em>. Die meisten Handys unterstützen mittlerweile normales XHTML und wären somit ein idealer Client für Microformats. Der Hauptfokus neben dem Telefonieren und dem SMS schreiben liegt bei Handys auf dem Adressbuch oder dem Kalender, also genau den zwei weit verbreitetsten Mikroformaten <a href="http://microformats.org/wiki/hCard">hCard</a> und <a href="http://microformats.org/wiki/hCal">hCalendar</a>. Auch die, ursprünglich für Twitter entworfenen, <a href="http://microformats.org/wiki/microblogging-nanoformats">Nanoformats</a> wären ein idealer Standard um semantisch zu <abbr title="Short Message Service">SMS</abbr>en :)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Auch wenn Microformats keine Ideallösungen für DataPortability sind und nicht der Semantic Web Idee entsprechen, gibt es sicherlich genug sinnvolle Anwendungsgebiete.</p>
<!-- /wp:paragraph -->