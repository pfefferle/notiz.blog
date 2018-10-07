---
ID: 813
post_title: XRDS-Simple und DataPortability
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/04/15/xrds-simple-und-dataportability/
published: true
post_date: 2008-04-15 08:00:39
---
<!-- wp:paragraph -->
<p>Vor ein paar Wochen wurde <a href="http://xrds-simple.net/core/1.0/">XRDS-Simple 1.0 (Draft 1)</a> veröffentlicht. XRDS-Simple ist ein Standard, der auf bestehenden Standards der <a href="http://www.oasis-open.org/committees/xri/">XRI Community</a> aufbaut, auf den z.B. auch das von <a href="http://openid.net">OpenID</a> bekannte <a href="http://yadis.org">Yadis-Format</a> basiert.</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote"><p>XRDS-Simple provides a format and workflow for the discovery of resources metadata, and other linked resources. As web services continue to grow, applications utilize a wider range of web services and resources across multiple providers. XRDS-Simple allows providers to document their resources in a machine-readable way, which can be automatically discovered by consumer applications.</p></blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>XRDS-Simple bietet also ein recht simples Format um auf Services und andere "linked recources" zu verweisen.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>XRDS-Simple als zentraler ServiceCatalogue</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Wie man dieses Format für das DataPortability Projekt nutzen kann hat Christian Scholz in seinem Post "<a href="http://mrtopf.de/blog/web20/the-first-data-portability-use-case-somewhat-technical/">The first Data Portability Use Case (somewhat technical)</a>" schön zusammengefasst.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Nehmen wir an, ich melde mich bei einem neuen Dienst an und möchte meine Daten, die ich an anderen Stellen im Internet angegeben habe, wiederverwenden. Um nicht alle meine Profil-URLs immer wieder per Hand angeben zu müssen, kam die Idee eines ServiceCatalogues auf.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Der <strong>ServiceCatalogue</strong> soll an zentraler Stelle alle Informationen die über mich im Web verfügbar sind (z.B. als <a href="http://microformats.org/wiki/hcard">hCard</a>, <a href="http://microformats.org/wiki/xfn">XFN</a>, <a href="http://www.foaf-project.org/">FoaF</a>, usw. formatiert) bereitstellen.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;XRDS xmlns="xri://$xrds">
  &lt;XRD xmlns:simple="http://xrds-simple.net/core/1.0" xmlns="xri://$XRD*($v*2.0)" version="2.0">
    &lt;Type>xri://$xrds*simple&lt;/Type>
    &lt;Service priority="10">
      &lt;Type>http://www.w3.org/2006/03/hcard&lt;/Type>
      &lt;URI simple:httpMethod="GET">http://pownce.com/pfefferle&lt;/URI>
    &lt;/Service>
    &lt;Service priority="20">
      &lt;Type>http://gmpg.org/xfn/11&lt;/Type>
      &lt;URI simple:httpMethod="GET" priority="10">http://twitter.com/pfefferle&lt;/URI>
      &lt;URI simple:httpMethod="GET" priority="20">http://pownce.com/pfefferle&lt;/URI>
    &lt;/Service>
  &lt;/XRD>
&lt;/XRDS></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Das Beispiel zeigt z.B. die URL zu meiner hCard bei Pownce und meinen Freundesnetzen bei Pownce und Twitter. Um diese Information vor unerlaubten Zugriffen zu schützen, könnte die XRDS-Simple URL mit <a href="http://oauth.net/">OAuth</a> geschützt oder per <a href="http://openid.net/specs/openid-attribute-exchange-1_0.html">OpenID <abbr title="Attribute Exchange">AX</abbr></a> angefragt werden.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>XRDS-Simple mit AX abfragen</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Um XRDS-Simple via AX anzufragen, müsste man zuerst ein <a href="http://www.axschema.org/">AX-Schema</a> definieren:<strong>http://dataportability.org/schema/serviceCatalogue</strong> Label service catalogue Description The url to a XRDS-Simple formatted service catalogue Example http://example.org/sc.xrds Formatting
	<a href="http://www.w3.org/2001/XMLSchema#anyURI">http://www.w3.org/2001/XMLSchema#anyURI</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>und unter <code>http://dataportability.org/schema/serviceCatalogue</code> bereitstellen. Leider funktioniert diese Art der Bereitstellung nur wenn einige OpenID-Provider diese AX-ServiceCatalogue-URL auch implementieren.</p>
<!-- /wp:paragraph -->