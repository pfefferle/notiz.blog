---
ID: 4861
post_title: web+custom://scheme
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2012/11/09/custom-web-schemes/
published: true
post_date: 2012-11-09 23:26:28
---
<!-- wp:paragraph -->
<p>Ich habe in den letzten Monaten eine Menge über <em><a href="https://notiz.blog/2012/05/21/web-intents-die-losung-fur-das-nascar-problem/">Web Intents</a></em> gelesen und ich finde immer noch dass der <a href="http://www.webmonkey.com/2012/05/webkit-offers-early-preview-of-web-intents/">Webmonkey</a> die Thematik bisher am treffendsten beschrieben hat:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
    <p>In practice Web Intents work a bit like <code>mailto:</code> links, defining an action and then passing it along to the browser, which allows the user to choose how to handle the action. The difference is that instead of opening a desktop app, Web Intents connect to web services.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Der Vergleich ist simple und ich habe mir die Frage gestellt: Wieso nicht einfach wirklich unterschiedliche Schemes für die jeweiligen Anforderungen definieren? Eine App kann beim Browser anmelden dass sie <code>share://</code> oder <code>subscribe://</code> unterstützt und bei einem Klick auf einen entsprechenden Link, öffnet sich (statt der E-Mail App) eben die entsprechende Web-App.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>...vor kurzem hab ich dann mal ein wenig mit <a href="http://superfeedr.com">Superfeedrs</a> <a href="http://www.msgboy.com/">msgboy</a> herumgespielt und entdeckt dass es bei HTML5 wirklich <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/timers.html#custom-handlers">Custom-Schemes</a> gibt die man frei definieren kann!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Mit folgendem Befehl kann man beim Browser einen eigenen Protocol-Handler setzen:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>navigator.registerProtocolHandler(&#x27;web+share&#x27;, &#x27;http://spread.ly/?url=%s&#x27;, &#x27;Spread.ly&#x27;);</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Alle neuen Schemes sollten mit &quot;<code>web+</code>&quot; beginnen, ausnahmen sind schon bestehende Schemes, wie z.B. &quot;<code>mailto</code>&quot;, &quot;<code>mms</code>&quot;, &quot;<code>nntp</code>&quot;, &quot;<code>rtsp</code>&quot; oder &quot;<code>webcal</code>&quot;.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Der passende a-Tag zum oben genannten Beispiel müsste also folgendermaßen aussehen:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;a href=&quot;web+share:http://pfefferle.org&quot;&gt;Share this Page&lt;/a&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Klickt ein User den Link, wird einfach das <code>%s</code> vom Handler mit dem <code>href</code> ersetzt und aufgerufen:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>http://spread.ly/?url=web+share:http://pfefferle.org</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Bisher war ich ja ein großer <em>Web Intents</em> Fan (und bin es auch immer noch), aber für solche simplen Aktionen wie &quot;Share&quot;, &quot;Like&quot;, &quot;Subscribe&quot; oder &quot;Follow&quot; reicht doch ein simples Custom-Scheme vollkommen aus. Kein unnötiges JavaScript (mal abgesehen vom Registrieren des Handlers), nur ein wenig HTML. Großartig!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Protocol-Handler lassen sich übrigens auch abhängig vom Mime-Type setzen:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>navigator.registerContentHandler(&#x27;application/atom+xml&#x27;, &#x27;http://www.google.com/ig/add?feedurl=%s&#x27;, &#x27;Google Reader&#x27;)</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Bei allen Web-Dokumenten mit dem Mime-Type <code>application/atom+xml</code> sollte der Browser jetzt nachfragen ob er die URL mit dem Google-Reader öffnen soll.</p>
<!-- /wp:paragraph -->