---
ID: 4039
post_title: oAlternative
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2011/11/15/oalternative/
published: true
post_date: 2011-11-15 02:07:50
---
<!-- wp:paragraph -->
<p>Was das OpenWeb so kompliziert macht ist das Wörtchen "<strong>alternativ</strong>"!</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li>OpenID Discovery basiert auf Meta-Tags, <strong>alternativ</strong> funktioniert aber auch XRDS(-Simple)/Yadis oder Webfinger.</li>
	<li>OpenID stellt über SREG Profilinformationen bereit, <strong>alternativ</strong> aber auch über Attribute Exchange.</li>
	<li> RDFa 1.1 ist folgendermaßen aufgebaut:
		<code>&lt;html
  prefix="foaf: http://xmlns.com/foaf/0.1/"
  >
  ...
  &lt;span property="foaf:name">John Doe&lt;/span>
  ...
&lt;/html></code>
		<strong>alternativ</strong> aber auch:
		<code>&lt;div vocab="http://xmlns.com/foaf/0.1/" about="#me">
  &lt;span property="name">John Doe&lt;/span>
&lt;/div></code> ...oder:
		<code>&lt;div profile="http://xmlns.com/foaf/0.1/" about="#me">
  &lt;span property="foaf:name">John Doe&lt;/span>
&lt;/div></code>
	</li>
	<li>OpenSocial, oEmbed, ActivityStrea.ms und host-meta benutzen JSON, <strong>alternativ</strong> aber auch XML</li>
	<li>OAuth verschlüsselt mit HMAC-SHA1, <strong>alternativ</strong> aber auch mit RSA-SHA1 oder PLAINTEXT</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>To be continued...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Wie viel Komplexität man sich sparen könnte wenn man sich auf eine Variante beschränken würde.</p>
<!-- /wp:paragraph -->