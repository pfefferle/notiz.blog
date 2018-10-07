---
ID: 1939
post_title: Atom Cross-posting Extensions
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/10/06/atom-cross-posting-extensions/
published: true
post_date: 2009-10-06 20:20:31
---
<!-- wp:paragraph -->
<p><strong>Problem</strong>:</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1938,"align":"center"} -->
<div class="wp-block-image"><figure class="aligncenter"><img src="https://notiz.blog/wp-content/uploads/2009/09/Lifestream.fm-_-pfefferle.png" alt="Problem: Cross-posting and duplicates" class="wp-image-1938"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><br/>Quelle: <a href="http://lifestream.fm/pfefferle">Lifestream.fm</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Lösung</strong>: <a href="http://martin.atkins.me.uk/specs/atomcrosspost">Atom Cross-posting Extensions</a> von <a href="http://www.apparently.me.uk/">Martin Atkins</a></p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;entry>
  &lt;title>Using Microformats: Gateway to the Semantic Web | Professional Communication Society&lt;/title>
  &lt;link rel="alternate" href="http://pfefferle.yiid.com/activity/11891">&lt;/link>
  &lt;updated>2009-10-06T13:10:11Z&lt;/updated>
  &lt;author>
    &lt;name>Matthias Pfefferle&lt;/name>
  &lt;/author>
  &lt;id>tag:www.yiid.com,2009-10-06:/activity/11891&lt;/id>
  &lt;summary type="text">...&lt;/summary>
  &lt;content type="html">&lt;![CDATA[...]]>&lt;/content>
  
  &lt;crosspost:source>
    &lt;id>http://delicious.com/url/29ff30b281955db394f2c399c028c480#pfefferle&lt;/id>
    &lt;link rel="alternate" href="http://delicious.com/url/29ff30b281955db394f2c399c028c480#pfefferle" type="text/html" />
  &lt;/crosspost:source>
  
&lt;/entry></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Wenn ihr so kommentierfaul seid, dann bin ich mal schreibfaul ;)</p>
<!-- /wp:paragraph -->