---
ID: 767
post_title: Über IE8s Webslices und hAtom
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/03/06/ueber-ie8s-webslices-und-hatom/
published: true
post_date: 2008-03-06 08:45:50
---
<!-- wp:image {"align":"right","linkDestination":"custom"} -->
<div class="wp-block-image"><figure class="alignright"><a href="http://www.flickr.com/photos/factoryjoe/283007494/"><img src="https://notiz.blog/wp-content/uploads/2008/03/283007494_62c470f75d_o.png" alt="Bild von Chris Messina"/></a></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Ich habe heute morgen bei <a href="http://keasone.de/software/2008-03/microsoft-internet-explorer-8-beta-1-am-start">Keasone</a> schon den ersten (deutschsprachigen) Bericht über den <a href="http://www.microsoft.com/windows/products/winfamily/ie/ie8/default.mspx">Internet Explorer 8</a> (beta) gelesen. In den <em>Genuss</em>, ihn selber zu testen, bin ich leider noch nicht gekommen, habe aber gerade ein paar interessanten Artikel über ein neues <abbr title="InternetExplorer">IE</abbr>8 Feature gelesen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Mit dem neuen Internet Explorer ist es möglich Teile einer Webseite direkt zu abonnieren, um über Änderungen dieser Bereiche Informiert zu werden, ohne den Umweg über einen RSS-Feed gehen zu müssen. Das Besondere an den so genannten "<a href="http://www.microsoft.com/windows/products/winfamily/ie/ie8/webslices.mspx">WebSlices</a>" ist, dass sie dem <a href="http://microformats.org/wiki/hAtom">hAtom</a> Microformat bis auf ein paar kleine Unterschiede gleichen.</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote"><p>WebSlices are enabled by adding HTML annotations directly to the Web page. WebSlices use a combination of the hAtom Microformat and the WebSlice format to describe a subscribable portion of a Web page. This section covers the primary, expiration, and bandwidth properties of a WebSlice.</p></blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Das heißt, Microsoft hat weitestgehend die Attribute des hAtom Formats verwendet und einen eigenen "Container" darum gesetzt. Statt <code>class="hfeed hentry"</code> heißt es in der WebSlices-Definition <code>class="hslice"</code>...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Der Aufbau eines WebSlices sieht folgendermassen aus:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class="hslice" id="1"> 
 &lt;p class="entry-title">Item - $66.00&lt;/p> 
  &lt;div class="entry-content">high bidder: buyer1 
  ...
 &lt;/div> 
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Das hAtom Format im Vergleich:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class="hfeed hentry" id="1"> 
 &lt;p class="entry-title">Item - $66.00&lt;/p> 
  &lt;div class="entry-content">high bidder: buyer1 
  ...
 &lt;/div> 
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Prinzipiell ist die Idee hinter WebSlices, Teile einer Webseite abonnieren zu können, super... schade ist nur, dass sie nicht auf bestehende/etablierte Formate wie hAtom zurückgreifen, sondern wieder ein eigenes proprietäres Format schaffen müssen.<br/> Ich verstehe auch nicht ganz den Sinn hinter diesem Schritt... hAtom ist mittlerweile ein relativ weit verbreiteter Standard (<a href="http://microformats.org/wiki/hatom-examples-in-wild">einige Beispiele</a>) und würde dem WebSlices-System sofort einen Anwendungsfall bieten. Durch das Schaffen eines eigenen Formates dauert es seine Zeit, bis Webseiten-Betreiber dieses auch umsetzen (wenn sie es überhaupt umsetzen).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ich hoffe dass Microsoft seinen Kurs ändern wird oder zumindest das hAtom Format als alternative zu ihrem hSlice ermöglicht.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Weiterführende Links:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><a href="http://blogmatrix.blogmatrix.com/:entry:blogmatrix-2008-03-05-0000/">Microsoft's webslices</a></li>
	<li><a href="http://microformatique.com/?p=229">hAtom and IE8’s “WebSlices”</a></li>
	<li><a href="http://code.msdn.microsoft.com/Release/ProjectReleases.aspx?ProjectName=ie8whitepapers&amp;ReleaseId=567">WebSlices Whitepaper</a></li>
</ul>
<!-- /wp:list -->