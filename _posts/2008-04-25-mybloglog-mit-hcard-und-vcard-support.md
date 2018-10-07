---
ID: 836
post_title: 'MyBlogLog mit hCard &amp; vCard support'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/04/25/mybloglog-mit-hcard-und-vcard-support/
published: true
post_date: 2008-04-25 18:30:19
---
<!-- wp:paragraph -->
<p>Im <a href="http://mybloglogb.typepad.com/my_weblog/2008/04/mybloglog-hcard.html">MyBlogLog-Blog</a> wurden gestern die neuen v/hCard Features von MyBlogLog vorgestellt.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<div class="wp-block-image"><figure class="aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/04/pfefferle-mybloglog.jpg" alt="Pfefferle-MyBlogLog.jpg"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Der vCard-Export spricht ja eigentlich für sich selbst, aber die hCard-Implementierung bedarf ein paar zusätzlicher Worte. Wie schon in den <a href="https://notiz.blog/2008/04/23/maholo-unterstuetzt-microformats/#comment-8071">Kommentaren des letzten Posts</a> so treffend bemerkt wurde, ist es ja eigentlich kein wirkliches Hexenwerk seine Seite zu microfromatieren, umso schöner finde ich es wenn sich jemand dabei Mühe gibt.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>MyBlogLog hat der hCard eine eigene Seite spendiert, die man über das <a href="http://microformats.org/wiki/icons">hCard-Icon</a> (siehe Bild 1) erreicht... </p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<div class="wp-block-image"><figure class="aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/04/pfefferle-mybloglog-hcard.jpg" alt="Pfefferle-MyBlogLog-hCard.jpg"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Aber warum macht es Sinn die hCard auf eine extra Seite zu verbannen? Bei mehreren hCards auf einem Profil, wie im Falle von MyBlogLog (auch die Kontakte sind mit hCards ausgezeichnet), bekommt man beim interpretieren (parsen) der Seite das folgende Problem: <a href="https://notiz.blog/2008/03/16/welche-hcard-ist-die-richtige/">Welche hCard ist die Richtige</a>?</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Der einfachste Weg um auf eine <em><a href="http://microformats.org/wiki/representative-hcard">representative Identity</a></em> zu verweisen ist, eine externe hCard auf der Profil-Seite mit <a href="http://microformats.org/wiki/rel-me">rel-me</a> zu verlinken. Im Fall von <abbr title="MyBlogLog">MBL</abbr> sollte man dies über <code>&lt;link rel="me" /></code> im Header der Profilseite realisieren, da der Action-Stream auch eine hohe Anzahl an rel-me Links aufweist.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;link rel="me" href="http://www.mybloglog.com/buzz/members/pfefferle/hcard" type="text/html" />﻿</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Alternativ könnte man auch mit <a href="http://xrds-simple.net/core/1.0/">XRDS-Simple</a> auf die hCard-Seite verweisen (siehe auch <em><a href="https://notiz.blog/2008/04/15/xrds-simple-und-dataportability/#service-catalogue">Service Catalogue</a></em>):</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;XRDS xmlns="xri://$xrds">
  &lt;XRD xmlns:simple="http://xrds-simple.net/core/1.0"
          xmlns="xri://$XRD*($v*2.0)" version="2.0">
    &lt;Type>xri://$xrds*simple&lt;/Type>
    &lt;Service priority="10">
      &lt;Type>http://www.w3.org/2006/03/hcard&lt;/Type>
      &lt;URI simple:httpMethod="GET">
        http://www.mybloglog.com/buzz/members/pfefferle/hcard
      &lt;/URI>
    &lt;/Service>
    &lt;Service priority="20">
      &lt;Type>http://gmpg.org/xfn/11&lt;/Type>
      &lt;URI simple:httpMethod="GET">
        http://www.mybloglog.com/buzz/members/pfefferle/hcard
      &lt;/URI>
    &lt;/Service>
  &lt;/XRD>
&lt;/XRDS></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Mal sehen was MyBlogLog als nächstes vor hat :)</p>
<!-- /wp:paragraph -->