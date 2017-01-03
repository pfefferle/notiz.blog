---
ID: 763
post_title: RDFa in XHTML 1.0 verwenden
author: Matthias Pfefferle
post_date: 2008-03-02 15:42:12
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/03/02/rdfa-in-xhtml-10-verwenden/
published: true
aktt_tweeted:
  - "1"
---
Als ich in <a href="http://notiz.blog/2008/03/02/rdfa-basics/">RDFa Basics</a> meinte es sei nicht möglich <abbr title="Resource Description Framework using Attributes">RDFa</abbr> in <abbr title="Extensible Hypertext Markup Language">XHTML</abbr> 1 zu verwenden, war das nicht die volle Wahrheit. Um das eigene Format so schnell wie möglich zu verbreiten hat der <a href="http://www.w3.org">W3C</a> einen Doctype für den Übergang veröffentlicht:

<pre><code>&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML+RDFa 1.0//EN" "http://www.w3.org/MarkUp/DTD/xhtml-rdfa-1.dtd"&gt;</code></pre>

Außerdem wurde der <a href="http://validator.w3.org/">W3C Markup Validation Service</a> so angepasst, dass er XHTML/RDFa auch erkennt und entsprechend validiert.

<img src="http://www.w3.org/Icons/valid-xhtml-rdfa" alt="RDFa valid" /> oder <img src="http://www.w3.org/Icons/valid-xhtml-rdfa-blue" alt="RDFa valid" />

Also viel Spaß beim ausprobieren...

<small>Quelle: <a href="http://rdfa.info/2007/08/07/w3c-htmlrdfa-validator/">RDFa.info</a></small>