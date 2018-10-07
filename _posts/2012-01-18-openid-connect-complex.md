---
ID: 4130
post_title: 'OpenID <del datetime="2012-01-18T09:33:25+00:00">Connect</del> Complex'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2012/01/18/openid-connect-complex/
published: true
post_date: 2012-01-18 11:31:08
---
<!-- wp:image {"id":4138,"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2012/01/openid-complex.jpg" alt="openid-complex" class="wp-image-4138" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Hat der erste Entwurf von <a href="http://web.archive.org/web/20110720081501/http://openidconnect.com/"><em>OpenID Connect</em></a> noch auf eine (übersichtliche) Seite gepasst, braucht der <a href="http://openid.net/connect/">Draft</a> der OpenID Foundation schon <strong>7 unterschiedliche Spezifikationen</strong>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Wieso müssen "Standard"-Organisationen wie das W3C (z.B. RDFa) oder der OpenID Foundation denn alles so unnötig kompliziert machen? Immerhin schafft es ja sogar Facebook seinen Authentifizierungsprozess auf <a href="http://developers.facebook.com/docs/authentication/">einer Seite</a> zu erklären. ...und noch besser! Er lässt in drei Sätzen zusammenfassen:</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol>
	<li>Hol dir über folgende URL einen Access-Token:<br/>
		<code>https://www.facebook.com/dialog/oauth?<br/>
     client_id=YOUR_APP_ID&amp;redirect_uri=YOUR_URL</code></li>
	<li>Häng ihn an folgende URL, auf den du den User weiterleitest:<br/>
		<code>https://www.facebook.com/dialog/oauth?<br/>
     client_id=YOUR_APP_ID&amp;redirect_uri=YOUR_URL&amp;<br/>
     scope=email,read_stream</code></li>
	<li>Fertsch!</li>
</ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>...dazu kommen eine weitere <a href="http://openid.net/specs/openid-connect-discovery-1_0.html">Discovery-Variante</a> die Webfinger, host-meta, XRD, XRDS oder YADIS komplett ignoriert und eine <a href="http://openid.net/specs/openid-connect-messages-1_0.html#anchor14">Identity-API</a> die SREG oder AX noch nicht einmal ähnelt!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Mike Jones, einer der Hauptentwickler der Spezifikation, <a href="http://self-issued.info/?p=619">schreibt zwar</a>:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>The design philosophy behind OpenID Connect is “make simple things simple and make complex things possible”.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Das ist aber nur die halbe Wahrheit. Webseitenbetreiber, die zukünftig einen <em>OpenID Connect</em> Login anbieten wollen, haben es in der Tat etwas einfacher, da sie sich auf die "<a href="http://openid.net/specs/openid-connect-basic-1_0.html">Minimalanforderungen</a>" konzentrieren können. Seiten die einen <em>OpenID Connect</em> Provider stellen wollen haben aber <a href="http://openid.net/specs/openid-connect-basic-1_0.html#anchor2">folgendes Problem</a>:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Authorization Requests can follow one of two paths; the Implicit Flow or the Authorization Code Flow. [...]<br/> The OpenID Connect Basic Client profile only documents Clients using the Implicit Flow. OpenID Providers MUST support both flows. [...]</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Damit begeht die <em>OpenID Foundation</em> wieder den gleichen Fehler wie bei OpenID 2.0. Am Schluss gibt es so viele unterschiedliche und halbfertige Implemenrierungen, dass man wieder auf <abbr title="Software As A Service">SaaS</abbr>-Dienste wie <a href="http://www.janrain.com/products/engage/social-login">Janrain</a> oder <a href="http://www.gigya.com/">Gigaya</a> zurückgreifen muss. Wozu braucht es dann noch einen "Standard"?</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Warum denn immer <a href="https://notiz.blog/2011/11/15/oalternative/">1000 Alternativen</a> anbieten? Bei Facebook klappts ja auch ohne...</p>
<!-- /wp:paragraph -->