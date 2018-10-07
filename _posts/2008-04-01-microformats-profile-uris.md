---
ID: 788
post_title: Microformats Profile URIs
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/04/01/microformats-profile-uris/
published: true
post_date: 2008-04-01 15:08:32
---
<!-- wp:paragraph -->
<p>Um auf die im HTML-Quellcode verwendeten <a href="http://microformats.org/wiki/microformats">Microformats</a> hinweisen zu können, wurden vom Microformats-Team jetzt einheitliche <a href="http://de.selfhtml.org/html/kopfdaten/meta.htm#profil">Profile <abbr title="Uniform Resource Identifier">URI</abbr>s</a> veröffentlicht. Berücksichtigt wurden alle non-draft Microformats (Stand: März 2008) ausgenommen <a href="http://microformats.org/wiki/XOXO">XOXO</a> und <a href="http://gmpg.org/xmdp/">XMDP</a>:</p>
<!-- /wp:paragraph -->

<!-- wp:table -->
<table class="wp-block-table"><thead><tr><th>Specification</th><th>Profile(s)</th></tr></thead><tbody><tr><td> <a href="http://microformats.org/wiki/geo">geo</a></td><td> <a href="http://purl.org/uF/geo/0.9/">http://purl.org/uF/geo/0.9/</a></td></tr><tr><td> <a href="http://microformats.org/wiki/hAtom">hAtom</a></td><td> <a href="http://purl.org/uF/hAtom/0.1/">http://purl.org/uF/hAtom/0.1/</a></td></tr><tr><td> <a href="http://microformats.org/wiki/hCalendar">hCalendar</a></td><td> <a href="http://purl.org/uF/hCalendar/1.0/">http://purl.org/uF/hCalendar/1.0/</a></td></tr><tr><td> <a href="http://microformats.org/wiki/hCard">hCard</a></td><td> <a href="http://www.w3.org/2006/03/hcard">http://www.w3.org/2006/03/hcard</a> <strong>or</strong> <a href="http://purl.org/uF/hCard/1.0/">http://purl.org/uF/hCard/1.0/</a></td></tr><tr><td> <a href="http://microformats.org/wiki/hResume">hResume</a></td><td> <a href="http://microformats.org/wiki/hresume-profile">http://microformats.org/wiki/hresume-profile</a></td></tr><tr><td> <a href="http://microformats.org/wiki/rel-license">rel-license</a></td><td> <a href="http://purl.org/uF/rel-license/1.0/">http://purl.org/uF/rel-license/1.0/</a></td></tr><tr><td> <a href="http://microformats.org/wiki/rel-nofollow">rel-nofollow</a></td><td> <a href="http://purl.org/uF/rel-nofollow/1.0/">http://purl.org/uF/rel-nofollow/1.0/</a></td></tr><tr><td> <a href="http://microformats.org/wiki/rel-tag">rel-tag</a></td><td> <a href="http://purl.org/uF/rel-tag/1.0/">http://purl.org/uF/rel-tag/1.0/</a></td></tr><tr><td> <a href="http://microformats.org/wiki/vote-links">VoteLinks</a></td><td> <a href="http://purl.org/uF/VoteLinks/1.0/">http://purl.org/uF/VoteLinks/1.0/</a></td></tr><tr><td> <a href="http://microformats.org/wiki/xfn">XFN</a></td><td> <a href="http://gmpg.org/xfn/11">http://gmpg.org/xfn/11</a></td></tr></tbody></table>
<!-- /wp:table -->

<!-- wp:paragraph -->
<p>Eine komplette Übersicht findet man auch über <a href="http://purl.org/uF/2008/03/">purl.org/uF/2008/03/</a> oder im <a href="http://microformats.org/wiki/profile-uris">Microformats Wiki</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Diese URIs können, gemäß der <a href="http://www.w3.org/2005/07/13-nsuri">W3C namespace policy</a> <code>&lt;head /></code> der HTML Datei angegeben werden. Beispiel:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;head profile="http://www.ietf.org/rfc/rfc2731.txt http://www.w3.org/2006/03/hcard http://purl.org/uF/hAtom/0.1/"></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Quelle: ‘<a href="http://microformats.org/blog/2008/04/01/this-fortnight-in-microformats-march-17th%e2%80%9330th/">This Week in Microformats</a>’ für März.</p>
<!-- /wp:paragraph -->