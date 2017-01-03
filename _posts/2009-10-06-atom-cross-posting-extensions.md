---
ID: 1939
post_title: Atom Cross-posting Extensions
author: Matthias Pfefferle
post_date: 2009-10-06 20:20:31
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/10/06/atom-cross-posting-extensions/
published: true
---
<strong>Problem</strong>:

<img src="http://notiz.blog/wp-content/uploads/2009/09/Lifestream.fm-_-pfefferle.png" alt="Problem: Cross-posting and duplicates" title="Lifestream.fm" width="480" height="200" class="aligncenter size-full wp-image-1938" /><br /><small>Quelle: <a href="http://lifestream.fm/pfefferle">Lifestream.fm</a></small>

<strong>Lösung</strong>: <a href="http://martin.atkins.me.uk/specs/atomcrosspost">Atom Cross-posting Extensions</a> von <span class="vcard"><a href="http://www.apparently.me.uk/" class="url fn">Martin Atkins</a></span>

<pre>&lt;entry&gt;
  &lt;title&gt;Using Microformats: Gateway to the Semantic Web | Professional Communication Society&lt;/title&gt;
  &lt;link rel="alternate" href="http://pfefferle.yiid.com/activity/11891"&gt;&lt;/link&gt;
  &lt;updated&gt;2009-10-06T13:10:11Z&lt;/updated&gt;
  &lt;author&gt;
    &lt;name&gt;Matthias Pfefferle&lt;/name&gt;
  &lt;/author&gt;
  &lt;id&gt;tag:www.yiid.com,2009-10-06:/activity/11891&lt;/id&gt;
  &lt;summary type="text"&gt;...&lt;/summary&gt;
  &lt;content type="html"&gt;&lt;![CDATA[...]]&gt;&lt;/content&gt;
  <strong>
  &lt;crosspost:source&gt;
    &lt;id&gt;http://delicious.com/url/29ff30b281955db394f2c399c028c480#pfefferle&lt;/id&gt;
    &lt;link rel="alternate" href="http://delicious.com/url/29ff30b281955db394f2c399c028c480#pfefferle" type="text/html" /&gt;
  &lt;/crosspost:source&gt;
  </strong>
&lt;/entry&gt;</pre>

Wenn ihr so kommentierfaul seid, dann bin ich mal schreibfaul ;)