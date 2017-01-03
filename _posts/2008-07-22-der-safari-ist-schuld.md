---
ID: 964
post_title: Der Safari ist schuld!
author: Matthias Pfefferle
post_date: 2008-07-22 08:41:08
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/07/22/der-safari-ist-schuld/
published: true
aktt_tweeted:
  - "1"
---
Gestern habe ich durch Zufall den Schuldigen für die <a href="http://notiz.blog/2008/06/24/bbc-und-das-alte-haccessibility-problemchen/"><em>abbr-desing-pattern</em> - Misere</a> gefunden... Der Safari ist Schuld!

Ursprünglich war das <code>object</code>-Tag zum Anzeigen des Datums vorgesehen:

<code>&lt;object data="20050125"&gt;January 25&lt;/object&gt;</code>

Aber...

<blockquote cite="http://tantek.com/log/2005/01.html#d26t0100">Unfortunately, to put it mildly, Safari's <code>&lt;object&gt;</code> support  <em>sucks</em>.  It doesn't handle <code>&lt;object&gt;</code> fallbacks, it doesn't know when not to handle <code>&lt;object&gt;</code> mime types that it doesn't support, it doesn't support <code>display:inline</code> on <code>&lt;object&gt;</code>, and it doesn't do proper intrinsic sizing of <code>&lt;object&gt;</code> replaced elements.</blockquote>

DANKE SAFARI! ;)

Quelle: <a href="http://tantek.com/log/2005/01.html#d26t0100">Tantek's Thoughts</a>