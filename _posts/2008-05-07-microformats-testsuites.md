---
ID: 852
post_title: Microformats Testsuites
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/05/07/microformats-testsuites/
published: true
post_date: 2008-05-07 20:09:47
---
<!-- wp:paragraph -->
<p>In den letzten Tagen wurde in der Microformats-Community viel über das Thema standardisiertes Parsen und einheitliches Darstellen der verschiedenen Mikroformate (<a href="http://microformats.org/wiki/hCard">hCard</a> im speziellen) diskutiert.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Leider gab es bisher keinen einheitlichen "Microformats-Acid-Tests" sondern nur <a href="http://examples.tobyinkster.co.uk/hcalendar-acid1.html">vereinzelte</a> (projektspezifische) <a href="http://microformatique.com/optimus/test.html">Seiten</a> um einige Spezialfälle zu testen.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/05/microformats-testsuites.jpg" alt="microformats-testsuites.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><a href="http://www.glennjones.net/">Glenn Jones</a>, einer der Macher von <a href="http://lab.backnetwork.com/ufXtract/">ufXtract</a> hat jetzt eine sehr schöne <a href="http://www.ufxtract.com/testsuite/">Microformats-Testsuite</a> erstellt, die parser-unabhängig funktionieren soll um eventuelle Interpretationsfehler erkennen und vergleichen zu können.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>The Testrunner</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Um die Tests so einfach wie möglich zu gestalten, hat Glenn einen einen JavaScript-Testrunner entwickelt (siehe Screenshot). Testen kann man den <em>Runner</em> unter z.B. <a href="http://ufxtract.com/testsuite/hcard/1.0/hcard1.htm">http://ufxtract.com/testsuite/hcard/1.0/hcard1.htm</a> in dem man einfach <strong>Alt + X</strong> drückt (<strong>CTRL + ALT + X</strong> auf dem Mac).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Hier sei nochmal erwähnt warum es so wichtig ist, dass jeder Parser das gleiche (micro)JSON-Format nutzt:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Please note that at this stage the JSON standardisation process can cause a test to be marked as failed when it could be judged to have passed. <a href="http://www.glennjones.net/Post/836/Microformatstest-suiteconcept.htm">#</a></p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Nur bei einer gleichen JSON-Struktur kann der Output sinnvoll verglichen werden. Eine erste Version der <abbr title="JSON hCard">jCard</abbr> (danke nochmal an <a href="http://lib.omnia-computing.de/hcardmapper">Gordon Oheim</a> für sein Engagement) findet man im <a href="http://microformats.org/wiki/jcard">Microformats-Wiki</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>Testsuite-API</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Wer die Testsuite für seinen eigenen Parser einsetzen will, sollte sich mal die <a href="http://ufxtract.com/proxies/proxy.aspx">Testsuite-API</a> zu Gemüte führen.</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Rather than just build something in isolation I thought it would be nice to find a way to share this work with the community. <a href="http://www.glennjones.net/Post/836/Microformatstest-suiteconcept.htm">#</a></p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Großartige Arbeit!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Interessante Links zu dem Thema:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><a href="http://www.glennjones.net/Post/836/Microformatstest-suiteconcept.htm">Microformats test-suite concept</a></li>
	<li><a href="http://groups.google.com/group/microformats/browse_thread/thread/f0e2baa3ace94448">hCalendar Acid Test #1</a></li>
</ul>
<!-- /wp:list -->