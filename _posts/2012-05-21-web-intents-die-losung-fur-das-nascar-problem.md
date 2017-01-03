---
ID: 4215
post_title: 'Web Intents &#8211; Die Lösung für das NASCAR-Problem?'
author: Matthias Pfefferle
post_date: 2012-05-21 23:41:11
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2012/05/21/web-intents-die-losung-fur-das-nascar-problem/
published: true
---
Die Idee der <em>Web Intents</em> ist nicht mehr <a href="http://indiewebcamp.com/Standardizing_Web_Intents">ganz so neu</a> und ich hatte auch schon seit einer ganzen Weile mal vor darüber zu schreiben, aber... naja... jedenfalls hat sich Google der Idee jetzt mal angenommen und unter den Fittichen des W3C mal einen einen <a href="http://dvcs.w3.org/hg/web-intents/raw-file/tip/spec/Overview.html">Editor's Draft</a> gestartet.

Das Problem: Für die meisten Bedürfnisse im Web gibt es eine Reihe an Services, die diese befriedigen... und das ist eigentlich auch gut so... Leider führt es aber dazu dass Seitenbetreiber, um es jedem Besucher recht zu machen, zu folgendem neigen:

<img src="http://notiz.blog/wp-content/uploads/2012/04/need_for_webintents.jpg" alt="" title="need_for_webintents" width="598" height="377" class="aligncenter size-full wp-image-4216" />

In der OpenID-Community (welche mit dem gleichen Problem zu kämpfen hat), nennt man dieses Phänomen "NASCAR Problem" in Analogie zu den bunten Stickern der Rennwagen.

<h2>Das große Problem des dezentralen Webs!</h2>

Im Idealfall sollte aber nicht der Seitenbetreiber die Services auswählen sondern der Seitenbesucher ...und genau das ist das Dilemma bei verteilten Diensten (wenn man mal nicht davon ausgeht dass eh alle Welt bei Facebook ist). 

OpenID, Diaspora, StatusNET, Addthis, ShareThis und viele andere haben bisher relativ erfolglose Versuche gestartet die Icon-Flut einzudämmen. OpenID & Co. hat es mit diversen "Identifiern" (URL, XRI, E-Mail, Webfinger, ...) versucht und die User dadurch nur noch mehr verwirrt und die Share-Services verschleiern das Problem in dem sie die Buttons einfach in einem Popup/Layer verstecken.

<h2>Wie können <em>Web Intents</em> helfen?</h2>

<em><a href="http://webintents.org/">Web Intents</a></em> funktionieren nach einem ganz ähnlichen Prinzip wie XAuth (<a href="http://notiz.blog/2010/06/02/openweb-notizen-xauth-oexchange-firefox-sync-rdfa/">hier</a> erklärt). Beim Surfen merkt sich der Browser welche Dienste ein User benutzt und gibt diese, bei bedarf an besuchte Seiten weiter. Ein Beispiel:

<ol><li>Ein User besucht Google (oder Yahoo oder MyOpenID)</li>
<li>Der Browser fragt nach, ob er sich Google als Login-Dienst (in dem Fall OpenID) merken soll</li>
<li>Der User bestätigt und besucht weitere Seiten</li>
<li>Er entdeckt Plaxo und möchte sich anmelden</li>
<li>Beim Klick auf den Login-Button wird die Liste aller, beim Browser registierten Login-Dienste (in unserem Beispiel nur Google) an die Webseite übertragen (sofern der User einverstanden ist)</li>
<li>Statt wahrlose ausgewählte Diensten anzuzeigen, ist Plaxo jetzt in der Lage gleich den Authentifizierungs-Prozess mit Google zu starten</li></ol>

Dank <em>Web Intents</em> brauchen Service-Anbieter fortan nur noch ihre Dienste beim Browser registrieren und Seitenbetreiber können einen Platz auf ihrer Seite anbieten, an dem diese Aktionen ausgeführt werden sollen... so zu sagen eine Art "Universal Button". Der <a href="http://www.webmonkey.com/2012/05/webkit-offers-early-preview-of-web-intents/">Webmonkey</a> fasst das Thema <em>Web Intents</em> folgendermaßen zusammen:

<blockquote>In practice Web Intents work a bit like <code>mailto:</code> links, defining an action and then passing it along to the browser, which allows the user to choose how to handle the action. The difference is that instead of opening a desktop app, Web Intents connect to web services.</blockquote>

Keine Identifier, keine langen Button-Leisten/Popups/Layer und den ganzen komplizierten Käse übernimmt der Browser! Vielleicht wird es so ja doch noch was mit dem <em>synaptic</em>, <em>distributed</em> bzw. <em>federated social web</em> :)

In den kommenden Artikeln werde ich etwas mehr auf die Technik und die Implementierung in Chrome/WebKit eingehen.

Hier noch ein paar Links:

<ul><li><a href="http://glennjones.net/2011/08/web-intentsgluing-web-functionality-together/">Web Intents – Gluing web functionality together</a></li>
<li><a href="http://www.flatfrogblog.com/2011/08/07/web-actions/">Button Sluts and Web Actions</a></li>
<li><a href="http://www.webmonkey.com/2012/05/webkit-offers-early-preview-of-web-intents/">WebKit Offers Early Preview of ‘Web Intents’</a></li>
<li><a href="http://demos.webintents.org/">Web Intents: Demos</a></li>
<li><a href="http://examples.webintents.org/">Web Intents: Examples</a></li></ul>