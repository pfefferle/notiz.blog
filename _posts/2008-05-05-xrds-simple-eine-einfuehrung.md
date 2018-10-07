---
ID: 847
post_title: XRDS-Simple, eine Einführung
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/05/05/xrds-simple-eine-einfuehrung/
published: true
post_date: 2008-05-05 18:56:56
---
<!-- wp:paragraph -->
<p>Da <a href="http://xrds-simple.net/">XRDS-Simple</a> auch eine zentrale Rolle bei <a href="http://dataportability.org">DataPortability</a> spielen wird, hab ich mir das Format <a href="https://notiz.blog/2008/04/15/xrds-simple-und-dataportability/">nochmal</a> vorgenommen. (Im folgenden Text setze ich, der Einfachheit halber, XRDS mit XRDS-Simple gleich auch wenn es technisch nicht ganz korrekt ist)</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<div class="wp-block-image"><figure class="aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/05/xrds-simple-large.png" alt="XRDS-Simple-Large.png"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>XRDS-Simple ist in erster Linie eine <strong>einfache</strong> Form der Service-Discovery, von der Idee her ähnlich wie z.B. die <a href="http://de.wikipedia.org/wiki/Web_Services_Description_Language">Web Services Description Language</a> (WSDL).<br/> XRDS beschränkt sich, im Gegensatz zu dem wesentlich komplexeren <abbr title="Web Services Description Language">WSDL</abbr>, auf die Beschreibung der Service <abbr title="Uniform Resource Locator">URL</abbr>s/<abbr title="Uniform Resource Identifier">URI</abbr>s und wie man sie nutzt (<a href="http://en.wikipedia.org/wiki/HTTP">POST oder GET</a>).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Vom Aufbau her ist XRDS-Simple dem <a href="http://yadis.org/wiki/Yadis_1.0_(HTML)">YADIS Format</a> (OpenID-Autodetection) sehr ähnlich:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;XRDS xmlns="xri://$xrds">
  &lt;XRD xmlns:simple="http://xrds-simple.net/core/1.0"
          xmlns="xri://$XRD*($v*2.0)" version="2.0">
    &lt;Type>xri://$xrds*simple&lt;/Type>
    &lt;Service>
      &lt;Type>http://example.net/some_type&lt;/Type>
      &lt;URI simple:httpMethod="POST">
        http://example.com/resource
      &lt;/URI>
    &lt;/Service>
  &lt;/XRD>
&lt;/XRDS></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Der wichtigste Teil eines <code>Services</code> ist der <code>Type</code> welcher den Typ der URI beschreibt und die <code>URI</code> welche beschreibt unter welcher URI der Service zu erreichen ist.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ein paar Beispiele für ein paar klassische Services:</p>
<!-- /wp:paragraph -->

<!-- wp:html -->
<dl>
<dt>FOAF</dt>
<dd>
<dl>
<dt>type</dt>
<dd>http://xmlns.com/foaf/0.1/</dd>
<dt>url</dt>
<dd>http://www.mybloglog.com/buzz/members/pfefferle/foaf</dd>
</dl>
</dd>
<dt>hCard</dt>
<dd>
<dl>
<dt>type</dt>
<dd>http://purl.org/uF/hCard/1.0/</dd>
<dt>url</dt>
<dd>http://www.mybloglog.com/buzz/members/pfefferle/hcard</dd>
</dl>
</dd>
<dt>APML</dt>
<dd>
<dl>
<dt>type</dt>
<dd>http://www.apml.org/apml-0.6</dd>
<dt>url</dt>
<dd>http://notizblog.org/apml/</dd>
</dl>
</dd>
<dt>OPML</dt>
<dd>
<dl>
<dt>type</dt>
<dd>http://www.opml.org/spec2</dd>
<dt>url</dt>
<dd>http://ma.gnolia.com/opml/default/people/pfefferle</dd>
</dl>
</dd>
</dl>
<!-- /wp:html -->

<!-- wp:paragraph -->
<p>Neben dem <code>&lt;Type></code> kann für die URI auch noch ein <code>&lt;MediaType></code> (nichts anderes als der <abbr title="Multipurpose Internet Mail Extensions">MIME</abbr>-Type (<a href="http://tools.ietf.org/html/rfc2046">RFC2046</a>)) gesetzt werden, der beschreibt um was es sich bei dem Verlinkten handelt. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Beispiel: <code>&lt;MediaType>text/html&lt;/MediaType></code></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Mit diesem einfachen Prinzip lassen sich auf einfache Weise nahezu alle Services beschreiben.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Vorteile von XRDS-Simple? Meiner Meinung nach gibt es zwei wesentliche Gründe XRDS einzusetzen.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>Einheitliche Erkennung</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>XRDS vereinfacht die automatische Service-Erkennung, da nur noch ein Meta-Tag interpretiert werden muss:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;meta http-equiv="X-XRDS-Location" content="http://example.com/xrds" /></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>statt jeder Meta-Tag einzeln:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;link rel="meta" type="text/xml" title="APML" href="..." />
&lt;link rel="meta" type="text/xml" title="OPML" href="..." /></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>One file to detect them all :)</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>Information Hiding</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Ein weiterer wesentlicher Aspekt der Autodetection ist die Sicherheit... nicht jeder möchte seine Attention-Daten (<abbr title="Attention Profiling Mark-up Language"><a href="http://www.apml.org/">APML</a></abbr>) oder seine hCard frei zur Verfügung stellen. Über XRDS-Simple ist es möglich, diese Informationen zu bündeln und z.B. nur über <a href="http://www.axschema.org/">OpenID AX</a> oder <a href="http://oauth.net/">OAuth</a> zugänglich zu machen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ein Beispiel dazu: <a href="https://notiz.blog/2008/04/15/xrds-simple-und-dataportability/#service-catalogue">XRDS-Simple als zentraler ServiceCatalogue</a></p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>OAuth discovery</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Der Vollständigkeit halber sollte man erwähnen dass XRDS-Simple eigentlich ein "Nebenprodukt" von <a href="http://oauth.net/discovery/">OAuth Discovery</a> ist.</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote"><p>The first draft of OAuth Discovery published four months ago started a dialog and was the main driver behind the development of XRDS-Simple. <a href="http://www.hueniverse.com/hueniverse/2008/04/oauth-discovery.html">#</a></p></blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Mehr zu diesem Thema bei <a href="http://www.hueniverse.com/hueniverse/2008/04/oauth-discovery.html">hueniverse</a> oder <a href="http://factoryjoe.com/blog/2008/04/08/oauth-discovery-10-draft-2-released-with-support-from-magnolia-fire-eagle-and-satisfaction/">Chris Messina</a>.</p>
<!-- /wp:paragraph -->