---
ID: 767
post_title: Über IE8s Webslices und hAtom
author: Matthias Pfefferle
post_date: 2008-03-06 08:45:50
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/03/06/ueber-ie8s-webslices-und-hatom/
published: true
aktt_tweeted:
  - "1"
---
<a href="http://www.flickr.com/photos/factoryjoe/283007494/" title="Bild von Chris Messina"><img src='http://notiz.blog/wp-content/uploads/2008/03/283007494_62c470f75d_o.png' alt='Bild von Chris Messina' style='float: right; margin-left: 5px; border: none;' /></a>Ich habe heute morgen bei <a href="http://keasone.de/software/2008-03/microsoft-internet-explorer-8-beta-1-am-start">Keasone</a> schon den ersten (deutschsprachigen) Bericht über den <a href="http://www.microsoft.com/windows/products/winfamily/ie/ie8/default.mspx">Internet Explorer 8</a> (beta) gelesen. In den <em>Genuss</em>, ihn selber zu testen, bin ich leider noch nicht gekommen, habe aber gerade ein paar interessanten Artikel über ein neues <abbr title="InternetExplorer">IE</abbr>8 Feature gelesen.

Mit dem neuen Internet Explorer ist es möglich Teile einer Webseite direkt zu abonnieren, um über Änderungen dieser Bereiche Informiert zu werden, ohne den Umweg über einen RSS-Feed gehen zu müssen. Das Besondere an den so genannten "<a href="http://www.microsoft.com/windows/products/winfamily/ie/ie8/webslices.mspx">WebSlices</a>" ist, dass sie dem <a href="http://microformats.org/wiki/hAtom">hAtom</a> Microformat bis auf ein paar kleine Unterschiede gleichen.

<blockquote cite="http://code.msdn.microsoft.com/Release/ProjectReleases.aspx?ProjectName=ie8whitepapers&amp;ReleaseId=567">WebSlices are enabled by adding HTML annotations directly to the Web page. WebSlices use a combination of the hAtom Microformat and the WebSlice format to describe a subscribable portion of a Web page. This section covers the primary, expiration, and bandwidth properties of a WebSlice.</blockquote>

Das heißt, Microsoft hat weitestgehend die Attribute des hAtom Formats verwendet und einen eigenen "Container" darum gesetzt. Statt <code>class="hfeed hentry"</code> heißt es in der WebSlices-Definition <code>class="hslice"</code>...

Der Aufbau eines WebSlices sieht folgendermassen aus:

<pre class="code">&lt;div class="hslice" id="1"&gt; 
 &lt;p class="entry-title"&gt;Item - $66.00&lt;/p&gt; 
  &lt;div class="entry-content">high bidder: buyer1 
  ...
 &lt;/div&gt; 
&lt;/div&gt;</pre>

Das hAtom Format im Vergleich:

<pre class="code">&lt;div class="hfeed hentry" id="1"&gt; 
 &lt;p class="entry-title"&gt;Item - $66.00&lt;/p&gt; 
  &lt;div class="entry-content">high bidder: buyer1 
  ...
 &lt;/div&gt; 
&lt;/div&gt;</pre>

Prinzipiell ist die Idee hinter WebSlices, Teile einer Webseite abonnieren zu können, super... schade ist nur, dass sie nicht auf bestehende/etablierte Formate wie hAtom zurückgreifen, sondern wieder ein eigenes proprietäres Format schaffen müssen.
Ich verstehe auch nicht ganz den Sinn hinter diesem Schritt... hAtom ist mittlerweile ein relativ weit verbreiteter Standard (<a href="http://microformats.org/wiki/hatom-examples-in-wild">einige Beispiele</a>) und würde dem WebSlices-System sofort einen Anwendungsfall bieten. Durch das Schaffen eines eigenen Formates dauert es seine Zeit, bis Webseiten-Betreiber dieses auch umsetzen (wenn sie es überhaupt umsetzen).

Ich hoffe dass Microsoft seinen Kurs ändern wird oder zumindest das hAtom Format als alternative zu ihrem hSlice ermöglicht.

Weiterführende Links:
<ul><li><a href="http://blogmatrix.blogmatrix.com/:entry:blogmatrix-2008-03-05-0000/">Microsoft's webslices</a></li>
<li><a href="http://microformatique.com/?p=229">hAtom and IE8’s “WebSlices”</a></li>
<li><a href="http://code.msdn.microsoft.com/Release/ProjectReleases.aspx?ProjectName=ie8whitepapers&amp;ReleaseId=567">WebSlices Whitepaper</a></li></ul>