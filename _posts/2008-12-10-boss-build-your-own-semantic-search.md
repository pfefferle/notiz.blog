---
ID: 1349
post_title: BOSS = Build your Own Semantic Search
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/12/10/boss-build-your-own-semantic-search/
published: true
post_date: 2008-12-10 13:30:03
---
Yahoo! hat den <a href="http://developer.yahoo.com/searchmonkey/">SearchMonkey</a> jetzt auch in ihren Suchdienst <strong><abbr title="Build your Own Search Service"><a href="http://developer.yahoo.com/search/boss/">BOSS</a></abbr></strong> (Build your Own Search Service) integriert.

Einfach die entsprechende SearchMonkey - Konstante als <code>{query}</code> übergeben (eine Liste von Konstanten findet ihr <a href="https://notiz.blog/2008/12/09/searchmonkey-bekommt-neue-formate/">hier</a>):

<pre><code>http://boss.yahooapis.com/ysearch/web/v1/<strong>{query}</strong>?appid={youBOSSappid}</code></pre>

<pre><code>http://boss.yahooapis.com/ysearch/web/v1/<strong>searchmonkeyid:com.yahoo.page.uf.hcard</strong>?appid={youBOSSappid}</code></pre>

oder mit normalen Suchbegriffen kombinieren (alle hCards von Mr. T):

<pre><code>http://boss.yahooapis.com/ysearch/web/v1/<strong>searchmonkeyid:com.yahoo.page.uf.hcard+mr.t</strong>?appid={youBOSSappid}</code></pre>

: (|)