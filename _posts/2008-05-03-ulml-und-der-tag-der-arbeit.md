---
ID: 844
post_title: ULML und der Tag der Arbeit
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/05/03/ulml-und-der-tag-der-arbeit/
published: true
post_date: 2008-05-03 19:29:41
---
<!-- wp:paragraph -->
<p>Am "<a href="http://de.wikipedia.org/wiki/Erster_Mai">Tag der Arbeit</a>" (1. Mai) wurde ein <a href="http://userlabor.org/">neues Format</a> veröffentlicht, was sich genau mit dem Thema (Arbeit) befasst (wenn das nicht Liebe zum Detail ist :)). <strong><abbr title="User Labor Markup Language"><a href="http://userlabor.org/">ULML</a></abbr></strong> steht für <strong>User Labor Markup Language</strong> und stellt die <em>Arbeit</em> eines Users in einem Sozialen-Netz (z.B. eine Community oder ein Weblog) dar.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Vom Aufbau und der Idee her ist das ULML sehr ähnlich wie <abbr title="Attention Profiling Mark-up Language"><a href="https://notiz.blog/2007/11/23/apml-attention-profiling-mark-up-language/">APML</a></abbr> aufgebaut:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;?xml version="1.0" encoding="UTF-8"?>
&lt;ulml version="0.1">
  &lt;channel>
    &lt;record>
      &lt;actions>
        &lt;item name="photo" type="upload">120&lt;/item>
        &lt;item name="photo" type="tag">330&lt;/item>
      &lt;/actions>
      &lt;reactions>
        &lt;item name="photo" type="comment">15&lt;/item>
      &lt;/reactions>
      &lt;network>
       &lt;item name="connection">256&lt;/item>
      &lt;/network>
    &lt;/record>
  &lt;/channel>
&lt;/ulml></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Ein <code>record</code> besteht aus folgenden Tags:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><code>&lt;actions></code> — a person's actions (video uploads, bookmarks, tags, comments, votes etc.)</li>
	<li><code>&lt;reactions></code> — other's reactions to the person's actions (same types as in actions)</li>
	<li><code>&lt;network></code> — efficiency of the personal social network</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Mehr Infos zum Aufbau der XML-Datei findet ihr auf <a href="http://userlabor.org/">userlabor.org</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Der genaue Sinn dieses Formats hat sich mir noch nicht ganz erschlossen:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote"><p>We believe that universality, transparency, and accessibility of user labor metrics will ultimately lead to more sustainable service cycles in social web.</p></blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Die einzige Möglichkeit die mir spontan einfällt, ist der "Wert" eines Nutzers wenn es z.B. um die Schaltung von Werbung geht.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>...ein ULML WordPress Plugin sollte auch nicht wirklich viel Arbeit bereiten :)</p>
<!-- /wp:paragraph -->