---
ID: 788
post_title: Microformats Profile URIs
author: Matthias Pfefferle
post_date: 2008-04-01 15:08:32
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/04/01/microformats-profile-uris/
published: true
aktt_tweeted:
  - "1"
aktt_notify_twitter:
  - 'no'
---
Um auf die im HTML-Quellcode verwendeten <a href="http://microformats.org/wiki/microformats">Microformats</a> hinweisen zu können, wurden vom Microformats-Team jetzt einheitliche <a href="http://de.selfhtml.org/html/kopfdaten/meta.htm#profil">Profile <abbr title="Uniform Resource Identifier">URI</abbr>s</a> veröffentlicht. Berücksichtigt wurden alle non-draft Microformats (Stand: März 2008) ausgenommen <a href="http://microformats.org/wiki/XOXO">XOXO</a> und <a href="http://gmpg.org/xmdp/">XMDP</a>:

<table><thead><tr><th>Specification</th><th style="text-align: center;">Profile(s)</th></tr></thead><tbody><tr><td> <a href="http://microformats.org/wiki/geo" title="geo">geo</a></td><td> <a href="http://purl.org/uF/geo/0.9/" class="external" rel="nofollow">http://purl.org/uF/geo/0.9/</a></td></tr><tr class="alt"><td> <a href="http://microformats.org/wiki/hAtom" title="hAtom">hAtom</a></td><td> <a href="http://purl.org/uF/hAtom/0.1/" class="external" rel="nofollow">http://purl.org/uF/hAtom/0.1/</a></td></tr><tr><td> <a href="http://microformats.org/wiki/hCalendar" title="hCalendar">hCalendar</a></td><td> <a href="http://purl.org/uF/hCalendar/1.0/" class="external" rel="nofollow">http://purl.org/uF/hCalendar/1.0/</a></td></tr><tr class="alt"><td> <a href="http://microformats.org/wiki/hCard" title="hCard">hCard</a></td><td> <a href="http://www.w3.org/2006/03/hcard" class="external" rel="nofollow">http://www.w3.org/2006/03/hcard</a> <strong>or</strong> <a href="http://purl.org/uF/hCard/1.0/" class="external" rel="nofollow">http://purl.org/uF/hCard/1.0/</a></td></tr><tr><td> <a href="http://microformats.org/wiki/hResume" title="hResume">hResume</a></td><td> <a href="http://microformats.org/wiki/hresume-profile" class="external" rel="nofollow">http://microformats.org/wiki/hresume-profile</a></td></tr><tr class="alt"><td> <a href="http://microformats.org/wiki/rel-license" title="rel-license">rel-license</a></td><td> <a href="http://purl.org/uF/rel-license/1.0/" class="external" rel="nofollow">http://purl.org/uF/rel-license/1.0/</a></td></tr><tr><td> <a href="http://microformats.org/wiki/rel-nofollow" title="rel-nofollow">rel-nofollow</a></td><td> <a href="http://purl.org/uF/rel-nofollow/1.0/" class="external" rel="nofollow">http://purl.org/uF/rel-nofollow/1.0/</a></td></tr><tr class="alt"><td> <a href="http://microformats.org/wiki/rel-tag" title="rel-tag">rel-tag</a></td><td> <a href="http://purl.org/uF/rel-tag/1.0/" class="external" rel="nofollow">http://purl.org/uF/rel-tag/1.0/</a></td></tr><tr><td> <a href="http://microformats.org/wiki/vote-links" title="vote-links">VoteLinks</a></td><td> <a href="http://purl.org/uF/VoteLinks/1.0/" class="external" rel="nofollow">http://purl.org/uF/VoteLinks/1.0/</a></td></tr><tr class="alt">
<td> <a href="http://microformats.org/wiki/xfn" title="xfn">XFN</a></td><td> <a href="http://gmpg.org/xfn/11" class="external" rel="nofollow">http://gmpg.org/xfn/11</a></td></tr></tbody></table>
Eine komplette Übersicht findet man auch über <a href="http://purl.org/uF/2008/03/">purl.org/uF/2008/03/</a> oder im <a href="http://microformats.org/wiki/profile-uris">Microformats Wiki</a>.

Diese URIs können, gemäß der <a href="http://www.w3.org/2005/07/13-nsuri" class="external" title="http://www.w3.org/1999/10/nsuri" rel="nofollow">W3C namespace policy</a> <code>&lt;head /&gt;</code> der HTML Datei angegeben werden. Beispiel:

<code>&lt;head profile="http://www.ietf.org/rfc/rfc2731.txt http://www.w3.org/2006/03/hcard http://purl.org/uF/hAtom/0.1/"&gt;</code>

Quelle: ‘<a href="http://microformats.org/blog/2008/04/01/this-fortnight-in-microformats-march-17th%e2%80%9330th/">This Week in Microformats</a>’ für März.