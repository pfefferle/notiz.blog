---
ID: 848
post_title: 'XRDSType.net &#8211; Type URIs für XRDS-Simple'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/05/05/xrdstypenet-type-uris-fuer-xrds-simple/
published: true
post_date: 2008-05-05 21:00:38
---
<!-- wp:paragraph -->
<p>Angelehnt an die, für Profile-URIs geschaffene URI-Services wie z.B. <a href="http://purl.com/"><abbr title="Persistent Uniform Resource Locator">PURL</abbr></a> (oder <a href="http://xmlns.com/"><abbr title="XML namespaces">XMLNS</abbr></a> für XML-Namespaces), schafft <a href="http://xrdstype.net/">XRDSType.net</a> einen zentralen und "community-neutral URIspace" für <a href="http://xrds-simple.net/core/1.0/#rfc.section.6.3">XRDS-Simple Types</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Zum besseren Verständnis hier zwei Beispiele...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Profile-URI:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
&lt;html xmlns="http://www.w3.org/1999/xhtml" dir="ltr">

  &lt;head profile="http://gmpg.org/xfn/11">
...</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>XRDS-Simple Type:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;Service>
  &lt;Type>http://gmpg.org/xfn/11&lt;/Type>
  &lt;URI simple:httpMethod="POST">http://twitter.com/pfefferle&lt;/URI>
&lt;/Service></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Zwei wesentliche Aspekte für den Einsatz von XRDSTypes.net (<a href="http://blog.wachob.com/2008/05/announcing-xrds.html">via</a>):</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li>Besteht schon eine Profile-URI bzw. XMLNS wird dieser verwendet.</li>
	<li>XRDSTypes soll ein community-unabhängiger Platz sein, um Type-URIs zu definieren.</li>
	<li>...</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Für Microformats könnten also die im <a href="http://microformats.org/wiki/">Microformats Wiki</a> definierten <a href="http://microformats.org/wiki/profile-uris">Profile URIs</a> genutzt werden.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>(via <a href="http://mrtopf.de/blog/en/xrds-and-its-service-types-technical/">Mr. Topf</a>)</p>
<!-- /wp:paragraph -->