---
ID: 986
post_title: Email Address to URL Transformation
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/07/27/email-address-to-url-transformation/
published: true
post_date: 2008-07-27 19:13:53
---
<!-- wp:paragraph -->
<p><a href="http://emailtoid.net/">Email <em>to</em> ID</a> hat seine <a href="https://notiz.blog/2008/07/03/openid-per-e-mail/">Spezifikation</a>. <strong><a href="http://eaut.org/">Email Address to URL Translation</a></strong> (kurz <abbr title="Email Address to URL Translation">EAUT</abbr>) ist ein offenes Protokoll um E-Mail - Adressen zu URLs zu transformieren um sie für Services wie z.B. <a href="http://openid.net">OpenID</a> verwenden zu können.</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Email Address to URL Transformation (EAUT) defines a mechanism for transforming the "addr-spec" portion of an RFC2822 email address into an associated URL. The transform options outlined in this document are designed to be flexible enough such that every DNS domain-owner can specify unlimited email address to URL transformations that services can easily discover and utilize in their URL-based transactions.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Das Prinzip ist einfach:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li>Zuerst wird die <a href="http://eaut.org/specs/1.0/#obtaining-discovery-endpoint">EAUT Discovery Endpoint URL</a> ermittelt. Bei der E-Mail - Adresse <code>matthias@pfefferle.org</code> wäre die URL <code>pfefferle.org</code>.</li>
	<li>Als nächstes wird unter der URL nach <a href="http://eaut.org/specs/1.0/#discovered_info"><em>Discovered Information</em></a> (<a href="http://xrds-simple.net/">XRDS-Simple</a>) gesucht.</li>
	<li>Sind Informationen verfügbar, wird die <a href="http://eaut.org/specs/1.0/#anchor9">E-Mail - Adresse entsprechend der Vorgaben gemappt</a>.</li>
	<li>Gibt es keine passenden XRDS-Simple Daten, werden Mapper wie z.B. <a href="http://emailtoid.net/">Email <em>to</em> ID</a> empfohlen.</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Wen interessiert welche Schritte genau durchgeführt werden oder ob der eigene E-Mail - Provider ein entsprechendes Mapping unterstützt, kann seine E-Mail - Adresse <a href="http://eaut.org/example/">hier</a> testen (Beispiel: <a href="http://eaut.org/example/?email=matthias@pfefferle.org">matthias@pfefferle.org</a>).</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Examples in the wild</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Der erste Service, der die <strong><a href="http://eaut.org/">Email Address to URL Translation</a></strong> Spezifikation umgesetzt hat ist <a href="http://groups.google.com/group/eaut/browse_thread/thread/17018f869c9d3f4a">Ma.gnolia.com</a>:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Just wanted to let everyone know that we just deployed EAUT support over at Ma.gnolia (http://ma.gnolia.com). You can now type in your email address in the OpenID field and we'll resolve using EAUT with http://emailtoid.net/ as the default.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/07/magnoliacom-find-web-sites-build-community-online-1.jpg" alt="Ma.gnolia.com - Email Address to URL Transformation" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><a href="http://willnorris.com/">Will Norris</a> hat <abbr title="Email Address to URL Translation">EAUT</abbr> außerdem in sein <a href="http://willnorris.com/2008/07/wp-openid-220-released"><strong>OpenID WordPress Plugin</strong> (Version 2.2.0)</a> implementiert.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>(via <a href="http://feeds.feedburner.com/CarstenPoetterSharedItems">Carsten Pötters Shared Items</a>)</p>
<!-- /wp:paragraph -->