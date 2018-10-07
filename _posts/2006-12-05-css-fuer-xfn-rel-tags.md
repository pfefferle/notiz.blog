---
ID: 280
post_title: CSS für XFN rel-tags
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2006/12/05/css-fuer-xfn-rel-tags/
published: true
post_date: 2006-12-05 15:15:37
---
<!-- wp:paragraph -->
<p>Da mir die neuen <a href="http://www.factorycity.net/projects/microformats-icons/">XFN Icons</a> von <a href="http://www.bartelme.at/">Wolfgang Bartelme</a> und <a href="http://factoryjoe.com/blog/">Chris Messina</a> recht gut gefallen, hab ich sie mal in mein CSS eingebaut. Das schwierige daran war, kombinationen von XFN Beziehungen mit CSS abzubilden. Ein Beispiel:
</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">&lt;a href="https://notiz.blog" rel="friend met colleague">...&lt;/a></pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>Deshalb hab ich für mich die Hierarchie festgelegt:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li>me</li>
	<li>professional: co-worker, colleague</li>
	<li>friendship (at most one): friend, acquaintance, contact</li>
	<li>romantic: muse crush date sweetheart</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Das heißt im Klartext: Wenn ich einen rel-tag wie z.B. <code>rel="friend met colleague"</code> wird nur <em>friend</em> und <em>met</em> berücksichtigt weil das für mich höherwertig is. Wenn ihr ne andere Reihenfolge wollt, könnt ihr das ganze einfach in der CSS Datei umstellen (das Wichtigste unten).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ich habe das ganze mit den in CSS 2.1 definierten <a href="http://www.w3.org/TR/CSS21/selector.html#attribute-selectors">Selectors</a> realisiert und mit Firefox 2.0 und IE7 getestet.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Beispiel CSS Code:</strong>
</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">a:hover[rel~="me"] {
	background: url(images/xfn-me.png) 
no-repeat right;
	padding-right: 25px;
	}

a:hover[rel~="co-worker"], 
a:hover[rel~="colleague"] {
	background: url(images/xfn-colleague.png) 
no-repeat right;
	padding-right: 25px;
	}
	
a:hover[rel~="co-worker"][rel~="met"], 
a:hover[rel~="colleague"][rel~="met"] {
	background: url(images/xfn-colleague.png) 
no-repeat right;
	padding-right: 25px;
	}</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p><a href="https://notiz.blog/wp-content/uploads/2006/12/xfn.css">Komplette CSS Datei runterladen</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Beispiele: <a href="https://notiz.blog">ME</a>, <a href="#">FRIEND COLLEAGUE</a>, <a href="#">COLLEAGUE</a>, <a href="#">COLLEAGUE MET</a>, <a href="#">FRIEND MUSE</a>, <a href="#">FRIEND MUSE MET</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Würde mich sehr über Kommentare und Anregungen freuen...</p>
<!-- /wp:paragraph -->