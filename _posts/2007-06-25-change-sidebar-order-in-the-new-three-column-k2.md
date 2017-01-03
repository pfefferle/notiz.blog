---
ID: 499
post_title: >
  Change sidebar order in the new three
  column K2
author: Matthias Pfefferle
post_date: 2007-06-25 22:32:50
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/06/25/change-sidebar-order-in-the-new-three-column-k2/
published: true
---
<p class="info">The CSS Code has changed with Version 1, so try this <a href="http://notiz.blog/2007/09/23/k2-sidebar-hack-2/">new code</a>.</p>

The new version of the <strong><a href="http://getk2.com/">K2</a></strong> <a href="http://wordpress.org">WordPress</a> Theme supports a three column layout (you can change it in the K2 Options). I prefer both sidebars on one side (like the <strong><a href="http://www.obharath.net/blog/3columnk2/">3 column K2</a></strong> Theme) but K2 only supports <em>sidebar-content sidebar</em>.

<a href="http://www.flickr.com/photos/pfefferle/623460625/" title="Fotosharing"><img src="http://farm2.static.flickr.com/1141/623460625_b42fef2ebe_t.jpg" width="100" height="85" alt="Original K2" />
Original Version</a>

<a href="http://www.flickr.com/photos/pfefferle/623461381/" title="Fotosharing"><img src="http://farm2.static.flickr.com/1109/623461381_1b35a53d74_t.jpg" width="100" height="85" alt="Both sidebars on one side" />
New Version</a> 

To change this default order to content-sidbar-sidebar, you can download my small custom theme hack.

<p class="download"><a href='http://notiz.blog/wp-content/uploads/2007/06/hack.css' title='hack.css'>hack.css</a></p>
<small>put this file into the "styles" folder and activate it through the K2-Options panel</small>

Or you can change it by hand:

open <code>styles.css</code> and search

<pre class="code">.sidebar-dual #primary {
	margin-left: 170px;
	padding: 10px;
	}
</pre>

and replace it with

<pre class="code">.sidebar-dual #primary {
	padding: 10px;
	}
</pre>

and search

<pre class="code">#sidebar-alt {
	float: left;
	width: 150px;
	padding: 10px;
	left: -740px;
	margin-left: -170px;
	}
</pre>

and replace it with

<pre class="code">#sidebar-alt {
	float: left;
	width: 150px;
	padding: 10px;
	}
</pre>

That's All Folks...