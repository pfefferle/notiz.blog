---
ID: 844
post_title: ULML und der Tag der Arbeit
author: Matthias Pfefferle
post_date: 2008-05-03 19:29:41
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/05/03/ulml-und-der-tag-der-arbeit/
published: true
aktt_tweeted:
  - "1"
---
Am "<a href="http://de.wikipedia.org/wiki/Erster_Mai">Tag der Arbeit</a>" (1. Mai) wurde ein <a href="http://userlabor.org/">neues Format</a> veröffentlicht, was sich genau mit dem Thema (Arbeit) befasst (wenn das nicht Liebe zum Detail ist :)). <strong><abbr title="User Labor Markup Language"><a href="http://userlabor.org/">ULML</a></abbr></strong> steht für <strong>User Labor Markup Language</strong> und stellt die <em>Arbeit</em> eines Users in einem Sozialen-Netz (z.B. eine Community oder ein Weblog) dar.

Vom Aufbau und der Idee her ist das ULML sehr ähnlich wie <abbr title="Attention Profiling Mark-up Language"><a href="http://notiz.blog/2007/11/23/apml-attention-profiling-mark-up-language/">APML</a></abbr> aufgebaut:

<pre class="code">&lt;?xml version="1.0" encoding="UTF-8"?&gt;
&lt;ulml version="0.1"&gt;
  &lt;channel&gt;
    &lt;record&gt;
      &lt;actions&gt;
        &lt;item name="photo" type="upload"&gt;120&lt;/item&gt;
        &lt;item name="photo" type="tag"&gt;330&lt;/item&gt;
      &lt;/actions&gt;
      &lt;reactions&gt;
        &lt;item name="photo" type="comment"&gt;15&lt;/item&gt;
      &lt;/reactions&gt;
      &lt;network&gt;
       &lt;item name="connection"&gt;256&lt;/item&gt;
      &lt;/network&gt;
    &lt;/record&gt;
  &lt;/channel&gt;
&lt;/ulml&gt;</pre>

Ein <code>record</code> besteht aus folgenden Tags:

<ul><li><code>&lt;actions&gt;</code> — a person's actions (video uploads, bookmarks, tags, comments, votes etc.)</li>
<li><code>&lt;reactions&gt;</code> — other's reactions to the person's actions (same types as in actions)</li>
<li><code>&lt;network&gt;</code> — efficiency of the personal social network</li></ul>

Mehr Infos zum Aufbau der XML-Datei findet ihr auf <a href="http://userlabor.org/">userlabor.org</a>.

Der genaue Sinn dieses Formats hat sich mir noch nicht ganz erschlossen:

<blockquote cite="http://userlabor.org/">We believe that universality, transparency, and accessibility of user labor metrics will ultimately lead to more sustainable service cycles in social web.</blockquote>

Die einzige Möglichkeit die mir spontan einfällt, ist der "Wert" eines Nutzers wenn es z.B. um die Schaltung von Werbung geht.

...ein ULML WordPress Plugin sollte auch nicht wirklich viel Arbeit bereiten :)