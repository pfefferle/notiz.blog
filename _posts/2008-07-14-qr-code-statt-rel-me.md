---
ID: 953
post_title: QR-Code statt rel-me
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/07/14/qr-code-statt-rel-me/
published: true
post_date: 2008-07-14 13:25:02
---
<!-- wp:paragraph -->
<p>Um einen <em>guten</em> sozialen Graphen abbilden zu können ist es wichtig, dass die Verlinkung über z.B. <a href="http://microformats.org/wiki/rel-me">rel-me</a> (oder <a href="http://xmlns.com/foaf/spec/#term_weblog">FoaF</a> oder <a href="http://wiki.openid.net/Delegation">OpenID-Delegation</a>) bidirektional statt findet.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Beispiel:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><code>&lt;a rel="me" href="http://twitter.com/pfefferle" /></code> (notizBlog.org -> twitter.com)</li>
	<li><code>&lt;a rel="me" href="https://notiz.blog" /></code> (twitter.com -> notiz.blog)</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Um auch Community-Profile ohne Backlink-Möglichkeiten (z.B. facebook) verifizieren zu können, kam <a href="http://brad.livejournal.com/profile">Brad Fitzpatrick</a> (der Mann hinter Googles <em><a href="http://code.google.com/apis/socialgraph/">Social Graph <abbr title="Application Programming Interface">API</abbr></a></em>) auf die <a href="http://brad.livejournal.com/2387582.html">geniale Idee</a>, den fehlenden Link mit einer <abbr title="quick response">qr</abbr>-codierten <abbr title="Uniform Resource Locator">URL</abbr> in <a href="http://www.facebook.com/people/Brad_Fitzpatrick/500033387">seinem Profilbild</a> zu ersetzen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>...jetzt müssen die QR-Codes nur noch in die <abbr title="Social Graph">SG</abbr>-<abbr title="Application Programming Interface">API</abbr> aufgenommen werden.</p>
<!-- /wp:paragraph -->