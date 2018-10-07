---
ID: 586
post_title: 'K2 Sidebar Hack #2'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/09/23/k2-sidebar-hack-2/
published: true
post_date: 2007-09-23 10:13:02
---
<!-- wp:paragraph -->
<p>Um die zwei Sidebars des <a href="http://getk2.com/">K2 (WordPress) Themes</a> auf die rechte Seite zu bekommen, und nicht wie standardmäßig vorgegeben links und rechts vom Content, müsst ihr eurem <a href="http://k2.stikipad.com/docs/show/K2+Styles+and+Mods">Custom Style</a> einfach folgende Zeilen hinzufügen:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>.columns-three #primary {
	margin-left: 0px !important;
	}
	
.columns-three #sidebar-alt {
	left: 0px !important;
	margin-left: 0px !important;
	}</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Da sich das StyleSheet in der Version 1.0 nochmal geändert hat, funktioniert der <a href="https://notiz.blog/2007/06/25/change-sidebar-order-in-the-new-three-column-k2/">alte Code</a> nicht mehr.
</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Download <a href="https://notiz.blog/wp-content/uploads/2007/10/hack.css">hack.css</a> als Custom Style (CSS Sidebar Hack .2)</p>
<!-- /wp:paragraph -->