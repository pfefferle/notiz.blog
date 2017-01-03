---
ID: 813
post_title: XRDS-Simple und DataPortability
author: Matthias Pfefferle
post_date: 2008-04-15 08:00:39
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/04/15/xrds-simple-und-dataportability/
published: true
aktt_notify_twitter:
  - 'no'
aktt_tweeted:
  - "1"
---
Vor ein paar Wochen wurde <a href="http://xrds-simple.net/core/1.0/">XRDS-Simple 1.0 (Draft 1)</a> veröffentlicht. XRDS-Simple ist ein Standard, der auf bestehenden Standards der <a href="http://www.oasis-open.org/committees/xri/">XRI Community</a> aufbaut, auf den z.B. auch das von <a href="http://openid.net">OpenID</a> bekannte <a href="http://yadis.org">Yadis-Format</a> basiert.

<blockquote cite="http://xrds-simple.net/core/1.0/">XRDS-Simple provides a format and workflow for the discovery of resources metadata, and other linked resources. As web services continue to grow, applications utilize a wider range of web services and resources across multiple providers. XRDS-Simple allows providers to document their resources in a machine-readable way, which can be automatically discovered by consumer applications.</blockquote>

XRDS-Simple bietet also ein recht simples Format um auf Services und andere "linked recources" zu verweisen.

<h4 id="service-catalogue">XRDS-Simple als zentraler ServiceCatalogue</h4>

Wie man dieses Format für das DataPortability Projekt nutzen kann hat Christian Scholz in seinem Post "<a href="http://mrtopf.de/blog/web20/the-first-data-portability-use-case-somewhat-technical/">The first Data Portability Use Case (somewhat technical)</a>" schön zusammengefasst.

Nehmen wir an, ich melde mich bei einem neuen Dienst an und möchte meine Daten, die ich an anderen Stellen im Internet angegeben habe, wiederverwenden. Um nicht alle meine Profil-URLs immer wieder per Hand angeben zu müssen, kam die Idee eines ServiceCatalogues auf.

Der <strong>ServiceCatalogue</strong> soll an zentraler Stelle alle Informationen die über mich im Web verfügbar sind (z.B. als <a href="http://microformats.org/wiki/hcard">hCard</a>, <a href="http://microformats.org/wiki/xfn">XFN</a>, <a href="http://www.foaf-project.org/">FoaF</a>, usw. formatiert) bereitstellen.

<pre class="code">&lt;XRDS xmlns="xri://$xrds"&gt;
  &lt;XRD xmlns:simple="http://xrds-simple.net/core/1.0" xmlns="xri://$XRD*($v*2.0)" version="2.0"&gt;
    &lt;Type&gt;xri://$xrds*simple&lt;/Type&gt;
    &lt;Service priority="10"&gt;
      &lt;Type&gt;http://www.w3.org/2006/03/hcard&lt;/Type&gt;
      &lt;URI simple:httpMethod="GET"&gt;http://pownce.com/pfefferle&lt;/URI&gt;
    &lt;/Service&gt;
    &lt;Service priority="20"&gt;
      &lt;Type&gt;http://gmpg.org/xfn/11&lt;/Type&gt;
      &lt;URI simple:httpMethod="GET" priority="10"&gt;http://twitter.com/pfefferle&lt;/URI&gt;
      &lt;URI simple:httpMethod="GET" priority="20"&gt;http://pownce.com/pfefferle&lt;/URI&gt;
    &lt;/Service&gt;
  &lt;/XRD&gt;
&lt;/XRDS&gt;</pre>

Das Beispiel zeigt z.B. die URL zu meiner hCard bei Pownce und meinen Freundesnetzen bei Pownce und Twitter. Um diese Information vor unerlaubten Zugriffen zu schützen, könnte die XRDS-Simple URL mit <a href="http://oauth.net/">OAuth</a> geschützt oder per <a href="http://openid.net/specs/openid-attribute-exchange-1_0.html">OpenID <abbr title="Attribute Exchange">AX</abbr></a> angefragt werden.

<h4>XRDS-Simple mit AX abfragen</h4>

Um XRDS-Simple via AX anzufragen, müsste man zuerst ein <a href="http://www.axschema.org/">AX-Schema</a> definieren:

<div id="desc"><strong>http://dataportability.org/schema/serviceCatalogue</strong><dl><dt>Label</dt><dd>service catalogue</dd><dt>Description</dt><dd>The url to a XRDS-Simple formatted service catalogue</dd><dt>Example</dt><dd>http://example.org/sc.xrds</dd><dt>Formatting</dt><dd><a href="http://www.w3.org/2001/XMLSchema#anyURI" class="formatlink">http://www.w3.org/2001/XMLSchema#anyURI</a></dd></dl></div>

und unter <code>http://dataportability.org/schema/serviceCatalogue</code> bereitstellen. Leider funktioniert diese Art der Bereitstellung nur wenn einige OpenID-Provider diese AX-ServiceCatalogue-URL auch implementieren.