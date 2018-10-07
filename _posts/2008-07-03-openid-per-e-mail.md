---
ID: 922
post_title: OpenID per E-Mail
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/07/03/openid-per-e-mail/
published: true
post_date: 2008-07-03 19:57:23
---
<!-- wp:image {"align":"right"} -->
<figure class="wp-block-image alignright"><img src="https://notiz.blog/wp-content/uploads/2008/07/emailtoidlogo.png" alt="emailtoid.logo.png" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><em><a href="http://emailtoid.net/">EMAIL to ID</a></em> ist ein Service, der eine E-Mail - Adresse zu OpenIDs macht.</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Emailtoid is a simple mapping service that enables the use of email addresses as OpenID identifiers.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p><em>EMAIL to ID</em> will kein neuer Provider sein, sondern sieht sich selbst nur als Übergangslösung bis E-Mail Services (z.B. GMX oder GMail) selbst diesen Dienst anbieten.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Der Login-Prozess soll folgendermaßen ablaufen:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>When a user enters in an email address, there is an xrds discovery made on the top level domain (eg, gmail.com). If the XRDS document contains an Emailtoid mapper or email transformation template, use that. If not, then you make the same request on emailtoid.net to get the mapper document and send the email to there. <strong>Emailtoid is a fallback.</strong></p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Wie genau das Mapping oder das <a href="http://xrds-simple.net/">XRDS-Dokument</a> aussehen soll ist noch nicht spezifiziert, wird aber demnächst <a href="http://emailtoid.net/developers/#adding_emailtoid">hier</a> zu finden sein.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>Macht eine E-Mail - Adresse als OpenID Sinn?</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>In Zukunft steht sicherlich die URL im Zentrum des Authentifizierungsprozesses, da sich über sie einfach mehr Informationen transportieren lassen (seien es Meta-Information oder Semantisches HTML). Auch das Semantische Web basiert auf <abbr title="Uniform Resource Identifier">URI</abbr>s, um verschiedene Informationen zu vernetzen. Aus diesen Gründen sollte man den User mal so langsam an diese neuen Umstände gewöhnen ;)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Mit <em>EMAIL to ID</em> kann der Nutzer seine bestehenden Gewohnheiten (Anmelden per E-Mail - Adresse) beibehalten und trotzdem die Vorteile von <a href="http://openid.net/">OpenID</a> nutzen (Simple Lösung für ein scheinbar schwieriges Problem... hat was vom Ei des Kolumbus).</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>Warum kein eigener Standard?</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Ein neuer OpenID Standard auf Basis von E-Mail - Adressen (wie <a href="http://www.sappenin.com/openid/ext/oet/openid-email-transform-extension-1_0.html">hier</a> angedacht) würde zusätzlichen und unnötigen Implementierungsaufwand bedeuten (nimmt man an, die <abbr title="Uniform Resource Locator">URL</abbr>s sind die Zukunft), den man sich bei <em>EMAIL to ID</em> sparen kann. <em>EMAIL to ID</em> mappt eigentlich <em>nur</em> eine E-Mail - Adresse auf eine <abbr title="Uniform Resource Locator">URL</abbr> <code>http://emailtoid.net/mapper?email=jane@example.com</code> und entspricht somit einer vollwertigen OpenID (keine Anpassungen am bisherigen Standard nötig).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>(<a href="http://factoryjoe.com/blog/2008/06/22/announcing-emailtoid-mapping-email-addresses-to-openids/">via</a>)</p>
<!-- /wp:paragraph -->