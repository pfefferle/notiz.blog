---
ID: 2677
post_title: ActivityStrea.ms Addon für Chrome
author: Matthias Pfefferle
post_date: 2010-05-19 21:49:46
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2010/05/19/activitystrea-ms-addon-fuer-chrome/
published: true
---
Inspiriert durch <a href="http://notiz.blog/2010/04/28/michromeformats/">Michromeformats</a>, hab ich mich auch mal an ein <a href="https://chrome.google.com/extensions/detail/fdhfcnnephnhamkbfeohddpflahcdado">Chrome-Addon</a> gemacht :)

<img src="http://notiz.blog/wp-content/uploads/2010/05/activitystreams-addon.jpg" alt="" title="ActivityStrea.ms-Chrome Addon" width="480" height="162" class="aligncenter size-full wp-image-2678" />

Das Addon erkennt auf der Seite <a href="http://wiki.activitystrea.ms/Autodiscovery">verlinkte</a> ActivityStrea.ms:

<pre>&lt;link <strong>rel="activitystream"</strong>
      type="application/atom+xml"
      href="..." /&gt;</pre>

oder:

<pre>&lt;link rel="alternate"
      <strong>class="activitystream"</strong> 
      type="application/atom+xml"
      href="..." /&gt;</pre>

Kein Hexenwerk, aber immerhin mal ein Anfang :) Falls euch noch ein paar Features einfallen, immer raus damit.