---
ID: 1031
post_title: MicroID ohne URI-Normalisierung
author: Matthias Pfefferle
post_date: 2008-08-06 08:37:51
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/08/06/microid-ohne-uri-normalisierung/
published: true
aktt_tweeted:
  - "1"
---
Vor ungefähr drei Monaten hatte ich mir schon mal Gedanken zu den <a href="http://notiz.blog/2008/04/16/das-kleine-problem-mit-microids/">Schwierigkeiten der MicroID-Verifizierung</a> gemacht:

<blockquote>Eine <abbr title="Uniform Resource Locator">URL</abbr> kann man auf zu viele verschieden Weisen schreiben, als dass sie eine valide ID abgeben könnte.</blockquote>

Schwierigkeiten bereiten die Seiten, die unterschiedliche URLs zulassen...
<ul>
<li><code>http://example.com</code></li>
<li><code>http://<strong>www.</strong>example.com</code></li>
<li><code>http://example.com<strong>/</strong></code></li>
</ul>

...da sie zusammen mit der E-Mail - Adresse drei unterschiedliche Hash-Werte ergeben.

Ein möglicher Lösungsansatz wäre eine <a href="http://openid.net/specs/openid-authentication-2_0.html#normalization_example">URI-Normalisierung</a>, wie sie z.B. OpenID vorschlägt, einzusetzen.

Eine viel einfachere und fehlerunanfälligere Lösung ist das dynamische zusammenbauen der MicroID über die direkt aufgerufenen URI als Identifier:

<ul>
<li><code>http://example.com</code> -&gt; <code>19358536d8c443614bc7d861f4b050ee34a549b9</code></li>
<li><code>http://<strong>www.</strong>example.com</code> -&gt; <code>05c732700bfa89cd234bb7fc08cb673f7c0d88b8</code></li>
<li><code>http://example.com<strong>/</strong></code> -&gt; <code>9275b4dcd7cc2c997b2a5249420b422e937d36e0</code></li>
</ul>
<small>(Benutzte E-Mail - Adresse: <code>mustermann@example.com</code>)</small>

Beim verifizieren bräuchte man sich also nur noch auf die E-Mail - Adresse konzentrieren anstatt alle in Frage kommenden URI/E-Mail - Kombinationen durchspielen zu müssen.