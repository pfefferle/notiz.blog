---
ID: 3129
post_title: 'OpenWeb-Notizen: Mozilla, Thunderbird, AOL, Webfinger'
author: Matthias Pfefferle
post_date: 2010-08-11 20:26:51
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2010/08/11/openweb-notizen-mozilla-thunderbird-aol-webfinger/
published: true
---
Letztes Mal sind die <em>Notizen</em> dank <em>zu viel Arbeit</em> und <em>StarCraft II</em> leider ausgefallen, aber das wird nicht einreißen... hoffe ich zumindest :)

<h2>Der Browser und das <em>Federated Web</em></h2>
Ein großes Problem im dezentralen Web: Der gemeine User kann nichts mit <em>Identifiern</em> anfangen, weder mit URLs (wie es NoseRub versucht hat) noch mit E-Mail Adressen (wie es Status.Net mit Webfinger versucht). Austin King zeigt auf <em>Mozilla Webdev</em> wie man dem, mit Hilfe des Browsers und der JavaScript Methoden <em>registerProtocolHandler</em> und <em>postMessage</em>, entgegen wirken kann. <a href="http://xauth.org">XAuth</a> funktioniert übrigens nach einem ähnlichen Prinzip.

&raquo; <a href="http://blog.mozilla.com/webdev/2010/07/26/registerprotocolhandler-enhancing-the-federated-web/">RegisterProtocolHandler Enhancing the Federated Web</a>

<h2>Thunderbird Contacts</h2>
Endlich gibt es das <em>Contacts</em>-Addon auch für den Thunerbird, denn da gehören sie ja auch hin.

<blockquote>The goal of add-on is to experiment in evolving the address book of Thunderbird beyond what it currently is today. Thunderbird Contacts isn’t a standalone address book, instead it understands that your contacts live on the web as much as they do inside Thunderbird. The add-on can pull in contact data from various services where your contacts already exist.</blockquote>

&raquo; <a href="http://mozillalabs.com/messaging/2010/08/04/thunderbird-contacts/" rel="bookmark">Thunderbird Contacts</a>

<h2>AOL und der Webfinger</h2>
AOL implementiert Webfinger für <em>@aol.com</em> und <em>@aim.com</em>.

<pre class="brush: xml;">&lt;?xml version='1.0' encoding='UTF-8'?&gt;
&lt;XRD xmlns='http://docs.oasis-open.org/ns/xri/xrd-1.0'&gt;
    &lt;!-- Host-wide Information --&gt;
    &lt;Link rel='http://specs.openid.net/auth/2.0/provider' href='https://api.screenname.aol.com/auth/openidServer'&gt;
        &lt;Title&gt;OpenID 2.0 Provider&lt;/Title&gt;
    &lt;/Link&gt;
    &lt;!-- Resource-specific Information --&gt;
    &lt;Link rel='lrdd' template='https://api.screenname.aol.com/auth/describe?uri={uri}'&gt;
        &lt;Title&gt;Resource Descriptor&lt;/Title&gt;
    &lt;/Link&gt;
&lt;/XRD&gt;
</pre>

&raquo; <a href="http://practicalid.blogspot.com/2010/08/webfinger-enabled-for-aolcom.html" rel="bookmark">Webfinger enabled for @aol.com</a>