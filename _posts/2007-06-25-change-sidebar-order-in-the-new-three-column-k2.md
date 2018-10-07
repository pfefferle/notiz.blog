---
ID: 499
post_title: >
  Change sidebar order in the new three
  column K2
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/06/25/change-sidebar-order-in-the-new-three-column-k2/
published: true
post_date: 2007-06-25 22:32:50
---
<!-- wp:paragraph -->
<p>The CSS Code has changed with Version 1, so try this <a href="https://notiz.blog/2007/09/23/k2-sidebar-hack-2/">new code</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The new version of the <strong><a href="http://getk2.com/">K2</a></strong> <a href="http://wordpress.org">WordPress</a> Theme supports a three column layout (you can change it in the K2 Options). I prefer both sidebars on one side (like the <strong><a href="http://www.obharath.net/blog/3columnk2/">3 column K2</a></strong> Theme) but K2 only supports <em>sidebar-content sidebar</em>.</p>
<!-- /wp:paragraph -->

<!-- wp:image -->
<figure class="wp-block-image"><img src="http://farm2.static.flickr.com/1141/623460625_b42fef2ebe_t.jpg" alt="Original K2" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><a href="http://www.flickr.com/photos/pfefferle/623460625/"><br/>
Original Version</a></p>
<!-- /wp:paragraph -->

<!-- wp:image -->
<figure class="wp-block-image"><img src="http://farm2.static.flickr.com/1109/623461381_1b35a53d74_t.jpg" alt="Both sidebars on one side" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><a href="http://www.flickr.com/photos/pfefferle/623461381/"><br/>
New Version</a> </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>To change this default order to content-sidbar-sidebar, you can download my small custom theme hack.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="https://notiz.blog/wp-content/uploads/2007/06/hack.css">hack.css</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>put this file into the "styles" folder and activate it through the K2-Options panel</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Or you can change it by hand:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>open <code>styles.css</code> and search</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">.sidebar-dual #primary {
	margin-left: 170px;
	padding: 10px;
	}
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>and replace it with</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">.sidebar-dual #primary {
	padding: 10px;
	}
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>and search</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">#sidebar-alt {
	float: left;
	width: 150px;
	padding: 10px;
	left: -740px;
	margin-left: -170px;
	}
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>and replace it with</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">#sidebar-alt {
	float: left;
	width: 150px;
	padding: 10px;
	}
</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>That's All Folks...</p>
<!-- /wp:paragraph -->