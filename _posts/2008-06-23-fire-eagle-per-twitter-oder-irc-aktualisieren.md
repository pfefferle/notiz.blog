---
ID: 919
post_title: >
  Fire Eagle per Twitter oder IRC
  aktualisieren
author: Matthias Pfefferle
post_date: 2008-06-23 22:17:28
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/06/23/fire-eagle-per-twitter-oder-irc-aktualisieren/
published: true
aktt_tweeted:
  - "1"
---
Was ist eigentlich <a href="http://fireeagle.yahoo.net">Fire Eagle</a>?

<blockquote>Fire Eagle is a site that stores information about your location. With your permission, other services and devices can either update that information or access it. By helping applications respond to your location, Fire Eagle is designed to make the world around you more interesting!</blockquote>

Man kann Fire Eagle natürlich auch über ein Webfrontend oder per Dopplr/Places aktualisieren... aber das kann ja jeder :)

<h4>Der twitter-firebot</h4>

Um den <a href="http://twitter.com/firebot">Fire-Bot</a> testen zu können muss man ihm zuerst folgen und ihn um eine Einladung bitten (falls man noch keinen Invite hat).

<ul><li>d firebot invite</li></ul>

Nach der Einladung erfolgt die Authentifizierung des Bots.

<ul><li>d firebot auth</li></ul>

Der Bot antwortet (mir hat er leider noch nicht geantwortet) mit einem Authentifizierungs-Link über welchen der Firebot für Fireeagle freischaltet wird.

Danach kann man seine <em>Location</em> bequem über Twitter ändern:

<ul><li>d firebot u Weinheim, Germany</li>
<li>d firebot u Ettlingen</li>
<li>d firebot u 69469</li>
<li>etc</li></ul>

(<a href="http://soylentfoo.jnewland.com/articles/2008/03/06/fire-eagle-location-aware-applications-without-the-hassle#instructions">via</a>)

<h4>Der IRC-firebot</h4>

Die Jungs von <a href="irc://irc.oftc.net/geo">#geo</a> haben sich einen ganz ähnlichen <a href="http://fireeagle.yahoo.net/">Fireeagle</a>-Bot für ihren Channel gebaut.

Nachdem man den Bot auf sich aufmerksam gemacht hat...

<code>[19:02] pfefferle: fireup, help?</code>
<code>[19:02] fireeagle: pfefferle: I have just sent you a URL in privmsg, please click on it to authorize.</code>

...bekommt man eine Private-Message mit einer Authentifizierungs-URL...

<code>fireeagle: Try Again! You must authorize first: https://fireeagle.yahoo.net/oauth/authorize?oauth_token=XXXXX</code>

...(gleiches Prinzip wie bei Twitter) und man kann seinen Status auch über IRC ändern.

<code>[19:23] pfefferle: fireup Weinheim, Germany</code>
<code>[19:23] fireeagle: Updating pfefferle to Weinheim, Deutschland</code>

Zur Kontrolle nochmal im Fire Eagle nachschaun:

<blockquote>Fire Eagle last spotted you about 1 hour ago in Weinheim, Deutschland using Fire Eagle GeoIRC bot. If you've gone somewhere else, then you should update your location!</blockquote>

(<a href="http://danbri.org/words/2008/06/22/331">via</a>)