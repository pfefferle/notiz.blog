---
ID: 908
post_title: hCard microformat Validator
author: Matthias Pfefferle
post_date: 2008-06-16 18:07:04
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/06/16/hcard-microformat-validator/
published: true
aktt_tweeted:
  - "1"
---
<img src="http://notiz.blog/wp-content/uploads/2008/06/hcard-validator.jpg" alt="hcard-validator.jpg" border="0" width="480" height="85" />

Der <a href="http://hcard.geekhood.net/">hCard Validator</a> "<em>...is an unofficial validator/conformance checker of the hCard microformat</em>". Während der <a href="http://microformatique.com/optimus/">Optimus-Validator</a> ein breites Spektrum an Microformats unterstützt, bring der <em>hCard Validator</em> (wie der Name schon sagt) ein paar schicke extra Features zum validieren von hCards mit sich.

Im Gegensatz zu Optimus, muss die <a href="http://microformats.org/wiki/hCard">hCard</a> nicht zwingend über eine <abbr title="Uniform Resource Locator">URL</abbr> erreichbar sein, sondern kann auch bequem über ein Textfeld oder einen statischen Upload überprüft werden.

Weitere tolle Features sind z.B. der <a href="http://microformats.org/wiki/hcard-profile#Usage">Profile-URI</a> check:

<blockquote><code>&lt;head&gt;</code> uses profile “<samp>http://gmpg.org/xfn/11</samp>” which is unrelated to <code>'http://www.w3.org/2006/03/hcard'</code>
This may suggest that document does <strong>not</strong> use hCard microformat.</blockquote>

oder der E-Mail - Adressen - Check:

<blockquote>Value of <code>email</code> property doesn't look like an e-mail
Found “<samp>webmaster-at-notiz.blog</samp>”, but expected simple syntax in form <code>mailto:joe@example.com?subject=is%20optional</code>.</blockquote>

<small>(<a href="http://hcard.geekhood.net/?url=http%3A%2F%2Fnotiz.blog%2Fkontakt%2F#result">Test-hCard</a>)</small>

Zum Test habe ich die gleiche <a href="http://microformatique.com/optimus/?uri=http%3A%2F%2Fnotiz.blog%2Fkontakt%2F&function=&amp;format=validate&amp;filter=hcard">URL auch noch mit dem Chef-Transformer validiert</a>, dem aber (leider) diese Liebe fürs Detail fehlt...