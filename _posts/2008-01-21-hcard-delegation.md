---
ID: 719
post_title: hCard Delegation
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/01/21/hcard-delegation/
published: true
post_date: 2008-01-21 19:24:54
---
<!-- wp:paragraph -->
<p>OpenID Delegation ermöglicht es den OpenID Nutzern eine beliebige <abbr title="Uniform Resource Locator">URL</abbr> als <a href="http://openid.net">OpenID</a> zu verwenden. Für die "Delegation" sind zwei <code>&lt;link /></code> Einträge im <a href="http://de.selfhtml.org/html/kopfdaten/index.htm">HTML-Header</a> notwendig:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><code>&lt;link rel="openid.server" href="http://example.com" /></code><br/>
	<code>&lt;link rel="openid.delegate me" href="http://id.example.com/" /></code></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Der erste Eintrag (<code>openid.server</code>) gibt den Server an, der den eigentlichen OpenID Service anbietet, der zweite Eintrag (<code>openid.delegate</code>) gibt an, welches die eigentliche OpenID <abbr title="Uniform Resource Locator">URL</abbr> ist.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Bei den Arbeiten an <a href="https://notiz.blog/projects/wp-hcard-commenting/">hCard-Commenting</a> kam mir die Idee, diese Art der "Delegation" auch für Microformats, speziell hCards, zu verwenden.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><code>&lt;link rel="hcard.delegate me" href="http://example.com/hcard/" /></code></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Der Vorteil dieser Variante wäre, dass man schon bestehende <a href="http://microformats.org/wiki/hCard">hCards</a> wie z.B. die Profilseite von <a href="http://www.flickr.com">flickr</a> (http://flickr.com/people/&lt;username>) oder das Public-Profile von <a href="http://www.myopenid.com">myOpenID</a> (http://&lt;username>.myopenid.com) wiederverwenden könnte, ohne sie nochmals im eigenen Blog veröffentlichen zu müssen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><code>&lt;link rel="hcard.delegate me" href="http://www.flickr.com/people/pfefferle" /></code></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ein weiterer Vorteil der "Delegation" ist, dass die Weblog <abbr title="Uniform Resource Locator">URL</abbr> meistens kürzer und viel einfacher zu merken ist, als ein Community Profil:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Weblog <abbr title="Uniform Resource Locator">URL</abbr>: <code>https://notiz.blog</code><br/> flickr <abbr title="Uniform Resource Locator">URL</abbr>: <code>http://www.flickr.com/people/pfefferle</code></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Einige WordPress Plugins wie z.B. das oben erwähnte <a href="https://notiz.blog/projects/wp-hcard-commenting/">hCard-Commenting</a> oder <a href="http://fourstarters.com/2008/01/20/havatar-wordpress-plugin/">hAvatar</a> nutzen das <em>Website</em> Feld eines Blogs, um die <abbr title="Uniform Resource Locator">URL</abbr> einer hCard anzugeben und widersprechen dabei eigentlich ein wenig der Idee des "adapting to current behaviors"<sup><a href="http://microformats.org/about/">1</a></sup> der Microformats Community. Wenn ich einen Weblog Eintrag kommentiere gebe ich eigentlich meine normale Blog-URL in das <em>Website</em> Feld ein, das heißt ich müsste <em>eigentlich</em> ein Verhalten ändern, was ich mit hCard-Delegation beibehalten könnte ;)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Aber der eigentliche Vorteil der "Delegation" liegt in der zentralen Nutzung der hCard. Ich müsste im besten Fall also nur noch eine hCard anlegen und pflegen.</p>
<!-- /wp:paragraph -->