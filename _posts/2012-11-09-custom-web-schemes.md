---
ID: 4861
post_title: web+custom://scheme
author: Matthias Pfefferle
post_date: 2012-11-09 23:26:28
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2012/11/09/custom-web-schemes/
published: true
---
Ich habe in den letzten Monaten eine Menge über <em><a href="http://notiz.blog/2012/05/21/web-intents-die-losung-fur-das-nascar-problem/">Web Intents</a></em> gelesen und ich finde immer noch dass der <a href="http://www.webmonkey.com/2012/05/webkit-offers-early-preview-of-web-intents/">Webmonkey</a> die Thematik bisher am treffendsten beschrieben hat:

<blockquote>In practice Web Intents work a bit like <code>mailto:</code> links, defining an action and then passing it along to the browser, which allows the user to choose how to handle the action. The difference is that instead of opening a desktop app, Web Intents connect to web services.</blockquote>

Der Vergleich ist simple und ich habe mir die Frage gestellt: Wieso nicht einfach wirklich unterschiedliche Schemes für die jeweiligen Anforderungen definieren? Eine App kann beim Browser anmelden dass sie <code>share://</code> oder <code>subscribe://</code> unterstützt und bei einem Klick auf einen entsprechenden Link, öffnet sich (statt der E-Mail App) eben die entsprechende Web-App.

...vor kurzem hab ich dann mal ein wenig mit <a href="http://superfeedr.com">Superfeedrs</a> <a href="http://www.msgboy.com/">msgboy</a> herumgespielt und entdeckt dass es bei HTML5 wirklich <a href="http://www.whatwg.org/specs/web-apps/current-work/multipage/timers.html#custom-handlers">Custom-Schemes</a> gibt die man frei definieren kann!

Mit folgendem Befehl kann man beim Browser einen eigenen Protocol-Handler setzen:

<pre><code data-programming-language="JavaScript">navigator.registerProtocolHandler('web+share', 'http://spread.ly/?url=%s', 'Spread.ly');</code></pre>

Alle neuen Schemes sollten mit "<code>web+</code>" beginnen, ausnahmen sind schon bestehende Schemes, wie z.B. "<code>mailto</code>", "<code>mms</code>", "<code>nntp</code>", "<code>rtsp</code>" oder "<code>webcal</code>".

Der passende a-Tag zum oben genannten Beispiel müsste also folgendermaßen aussehen:

<pre><code data-programming-language="HTML">&lt;a href="web+share:http://pfefferle.org"&gt;Share this Page&lt;/a&gt;</code></pre>

Klickt ein User den Link, wird einfach das <code>%s</code> vom Handler mit dem <code>href</code> ersetzt und aufgerufen:

<pre><code>http://spread.ly/?url=web+share:http://pfefferle.org</code></pre>

Bisher war ich ja ein großer <em>Web Intents</em> Fan (und bin es auch immer noch), aber für solche simplen Aktionen wie "Share", "Like", "Subscribe" oder "Follow" reicht doch ein simples Custom-Scheme vollkommen aus. Kein unnötiges JavaScript (mal abgesehen vom Registrieren des Handlers), nur ein wenig HTML. Großartig!

Protocol-Handler lassen sich übrigens auch abhängig vom Mime-Type setzen:

<pre><code data-programming-language="JavaScript">navigator.registerContentHandler('application/atom+xml', 'http://www.google.com/ig/add?feedurl=%s', 'Google Reader')</code></pre>

Bei allen Web-Dokumenten mit dem Mime-Type <code>application/atom+xml</code> sollte der Browser jetzt nachfragen ob er die URL mit dem Google-Reader öffnen soll.