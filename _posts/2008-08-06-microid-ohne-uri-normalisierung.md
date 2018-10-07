---
ID: 1031
post_title: MicroID ohne URI-Normalisierung
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/08/06/microid-ohne-uri-normalisierung/
published: true
post_date: 2008-08-06 08:37:51
---
<!-- wp:paragraph -->
<p>Vor ungefähr drei Monaten hatte ich mir schon mal Gedanken zu den <a href="https://notiz.blog/2008/04/16/das-kleine-problem-mit-microids/">Schwierigkeiten der MicroID-Verifizierung</a> gemacht:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Eine <abbr title="Uniform Resource Locator">URL</abbr> kann man auf zu viele verschieden Weisen schreiben, als dass sie eine valide ID abgeben könnte.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Schwierigkeiten bereiten die Seiten, die unterschiedliche URLs zulassen...</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><code>http://example.com</code></li>
	<li><code>http://<strong>www.</strong>example.com</code></li>
	<li><code>http://example.com<strong>/</strong></code></li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>...da sie zusammen mit der E-Mail - Adresse drei unterschiedliche Hash-Werte ergeben.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ein möglicher Lösungsansatz wäre eine <a href="http://openid.net/specs/openid-authentication-2_0.html#normalization_example">URI-Normalisierung</a>, wie sie z.B. OpenID vorschlägt, einzusetzen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Eine viel einfachere und fehlerunanfälligere Lösung ist das dynamische zusammenbauen der MicroID über die direkt aufgerufenen URI als Identifier:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><code>http://example.com</code> -> <code>19358536d8c443614bc7d861f4b050ee34a549b9</code></li>
	<li><code>http://<strong>www.</strong>example.com</code> -> <code>05c732700bfa89cd234bb7fc08cb673f7c0d88b8</code></li>
	<li><code>http://example.com<strong>/</strong></code> -> <code>9275b4dcd7cc2c997b2a5249420b422e937d36e0</code></li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>(Benutzte E-Mail - Adresse: <code>mustermann@example.com</code>)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Beim verifizieren bräuchte man sich also nur noch auf die E-Mail - Adresse konzentrieren anstatt alle in Frage kommenden URI/E-Mail - Kombinationen durchspielen zu müssen.</p>
<!-- /wp:paragraph -->