---
ID: 836
post_title: 'MyBlogLog mit hCard &amp; vCard support'
author: Matthias Pfefferle
post_date: 2008-04-25 18:30:19
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/04/25/mybloglog-mit-hcard-und-vcard-support/
published: true
aktt_tweeted:
  - "1"
---
Im <a href="http://mybloglogb.typepad.com/my_weblog/2008/04/mybloglog-hcard.html">MyBlogLog-Blog</a> wurden gestern die neuen v/hCard Features von MyBlogLog vorgestellt.

<img class="aligncenter" src="http://notiz.blog/wp-content/uploads/2008/04/pfefferle-mybloglog.jpg" alt="Pfefferle-MyBlogLog.jpg" border="0" width="480" height="199" />

Der vCard-Export spricht ja eigentlich für sich selbst, aber die hCard-Implementierung bedarf ein paar zusätzlicher Worte. Wie schon in den <a href="http://notiz.blog/2008/04/23/maholo-unterstuetzt-microformats/#comment-8071">Kommentaren des letzten Posts</a> so treffend bemerkt wurde, ist es ja eigentlich kein wirkliches Hexenwerk seine Seite zu microfromatieren, umso schöner finde ich es wenn sich jemand dabei Mühe gibt.

MyBlogLog hat der hCard eine eigene Seite spendiert, die man über das <a href="http://microformats.org/wiki/icons">hCard-Icon</a> (siehe Bild 1) erreicht... 

<img class="aligncenter" src="http://notiz.blog/wp-content/uploads/2008/04/pfefferle-mybloglog-hcard.jpg" alt="Pfefferle-MyBlogLog-hCard.jpg" border="0" width="480" height="300" />

Aber warum macht es Sinn die hCard auf eine extra Seite zu verbannen? Bei mehreren hCards auf einem Profil, wie im Falle von MyBlogLog (auch die Kontakte sind mit hCards ausgezeichnet), bekommt man beim interpretieren (parsen) der Seite das folgende Problem: <a href="http://notiz.blog/2008/03/16/welche-hcard-ist-die-richtige/">Welche hCard ist die Richtige</a>?

Der einfachste Weg um auf eine <em><a href="http://microformats.org/wiki/representative-hcard">representative Identity</a></em> zu verweisen ist, eine externe hCard auf der Profil-Seite mit <a href="http://microformats.org/wiki/rel-me">rel-me</a> zu verlinken. Im Fall von <abbr title="MyBlogLog">MBL</abbr> sollte man dies über <code>&lt;link rel="me" /&gt;</code> im Header der Profilseite realisieren, da der Action-Stream auch eine hohe Anzahl an rel-me Links aufweist.

<code>&lt;link rel="me" href="http://www.mybloglog.com/buzz/members/pfefferle/hcard" type="text/html" /&gt;</code>

Alternativ könnte man auch mit <a href="http://xrds-simple.net/core/1.0/">XRDS-Simple</a> auf die hCard-Seite verweisen (siehe auch <em><a href="http://notiz.blog/2008/04/15/xrds-simple-und-dataportability/#service-catalogue">Service Catalogue</a></em>):

<pre><code>&lt;XRDS xmlns="xri://$xrds"&gt;
  &lt;XRD xmlns:simple="http://xrds-simple.net/core/1.0"
          xmlns="xri://$XRD*($v*2.0)" version="2.0"&gt;
    &lt;Type&gt;xri://$xrds*simple&lt;/Type&gt;
    &lt;Service priority="10"&gt;
      &lt;Type&gt;http://www.w3.org/2006/03/hcard&lt;/Type&gt;
      &lt;URI simple:httpMethod="GET"&gt;
        http://www.mybloglog.com/buzz/members/pfefferle/hcard
      &lt;/URI&gt;
    &lt;/Service&gt;
    &lt;Service priority="20"&gt;
      &lt;Type&gt;http://gmpg.org/xfn/11&lt;/Type&gt;
      &lt;URI simple:httpMethod="GET"&gt;
        http://www.mybloglog.com/buzz/members/pfefferle/hcard
      &lt;/URI&gt;
    &lt;/Service&gt;
  &lt;/XRD&gt;
&lt;/XRDS&gt;</code></pre>

Mal sehen was MyBlogLog als nächstes vor hat :)