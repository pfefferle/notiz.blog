---
ID: 184
post_title: Simple linklog using the K2 theme
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2006/10/26/simple-linklog-using-the-k2-theme/
published: true
post_date: 2006-10-26 11:44:35
---
<!-- wp:paragraph -->
<p>HowTo get a linklog like <a href="http://www.kottke.org">Kottkes</a> <a href="http://kottke.org/remainder/">remaindered links</a> or something like the asides hack from <a href="http://photomatt.net/2004/05/19/asides/">Matt</a> using <a href="http://wordpress.org">wordpress</a>, the <a href="http://getk2.com">K2 theme</a> and some CSS.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>First of all you have to create a category you want to use, for example <em>"linkdump"</em>, then create your own <a href="http://www.johntp.com/2006/06/09/how-to-create-a-custom-k2-scheme-part-1/">custom style</a> (<a href="http://k2.stikipad.com/docs/show/Page+Structure">K2 page structure</a>).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Add the following code to your custom css...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>CSS code to hide the title (header), the noteworthy-link and the entry meta:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>.category-linkdump .entry-title, .category-linkdump .noteworthyLink, .category-linkdump .entry-meta {
    display: none;
}</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Example code to format the new linkdump category:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>.category-linkdump .entry-content a, .category-linkdump .entry-content a:hover {
    border-bottom: 1px dotted #CCC; text-decoration: none !important;
}</code></pre>
<!-- /wp:code -->

<!-- wp:code -->
<pre class="wp-block-code"><code>.category-linkdump .entry-content {
    /*background-color: #F8F8F8;*/
    border-top: 1px dotted #CCC;
    border-bottom: 1px dotted #CCC;
    padding: 15px; font-size: 10px;
}</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Demo: <a href="http://www.notiz.blog/category/links/">http://www.notiz.blog/category/links/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>If you want to use your del.icio.us account for the linkdump/linklog try "<a href="http://nozell.com/blog/2005/01/30/updated-yet-another-daily-delicious-hack/">Yet Another Weekly del.icio.us</a>"</p>
<!-- /wp:paragraph -->