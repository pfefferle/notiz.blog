---
ID: 2388
post_title: OneSocialWeb
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2010/02/11/onesocialweb/
published: true
post_date: 2010-02-11 23:33:46
---
<div class="alert alert-info">Die verlinkten Spezifikationen wurden gemäß den <a href="http://onesocialweb.org/docs-protocol.html">aktuellen Änderungen</a> (vom 13. April 2010) angepasst. Letztes Update 04.05.2010.</div>

<a href="http://onesocialweb.org/">OneSocialWeb</a> ist ein Projekt der <a href="http://www.vodafone.com/static/annual_report09/business/tech_and_resources/research_and_dev.html">Vodafone Group Research and Development</a> und definiert ein Protokoll basierend auf <a href="http://www.xmpp.org">XMPP</a> (besser bekannt unter dem Namen Jabber) welches <em>free, open, and decentralized social applications</em> ermöglichen soll.

<a href="https://notiz.blog/2010/02/11/onesocialweb/onesocialweb-creating-a-free-open-and-decentralized-social-networking-platform/" rel="attachment wp-att-2404"><img src="https://notiz.blog/wp-content/uploads/2010/02/OneSocialWeb-Creating-a-free-open-and-decentralized-social-networking-platform..jpg" alt="OneSocialWeb - Creating a free, open, and decentralized social networking platform." title="OneSocialWeb - Creating a free, open, and decentralized social networking platform." width="480" height="145" class="aligncenter size-full wp-image-2404" /></a>

Die Idee ist gar nicht so doof... Immerhin besitzt das XMPP Protokoll fast alle Eigenschaften die für ein dezentrales <em>Social Network</em> wichtig sind:
<ul>
<li>Eindeutiger Identifier (z.B. <em>username@jabber.org</em>) (mit <a href="http://code.google.com/p/webfinger/">Webfinger</a> auch OpenID möglich)</li>
<li>Profil-Informationen (<a href="http://xmpp.org/extensions/xep-0054.html">XEP-0054</a>)</li>
<li>Kontakte (<a href="http://xmpp.org/extensions/xep-0083.html">XEP-0083</a>)</li>
<li>Dezentraler Aufbau</li>
</ul>

...und die Gruppe arbeitet an diversen XMPP Erweiterungen um das Protokoll noch sozialer zu machen:

<ul>
<li><a href="http://onesocialweb.org/spec/1.0/osw-activities.html">Social Activities</a>: Erweitert das XMPP Protokoll mit der <a href="http://activitystrea.ms">ActivityStreams</a> Syntax.</li>
<li><a href="http://onesocialweb.org/spec/1.0/osw-vcard4.html">Social Profile</a>: <del datetime="2010-05-04T11:13:23+00:00">Die <a href="http://portablecontacts.net">Portable Contacts API</a> für XMPP</del> <ins datetime="2010-05-04T11:13:23+00:00"><a href="http://microformats.org/wiki/vcard4">vCard4</a> Support für XMPP</ins></li>
<li><a href="http://onesocialweb.org/spec/1.0/osw-relations.html">Social Relationships</a>: Eine Art <a href="http://gmpg.org/xfn/">XFN</a> für XMPP.</li>
<li><a href="http://onesocialweb.org/spec/1.0/osw-inbox.html">Social Notifications</a>: Eine Notification-Inbox für XMPP</li>
</ul>

Nachdem Facebook gestern angekündigt hat, dass <a href="http://developers.facebook.com/news.php?blog=1&story=361">der eigene Chat jetzt auch über XMPP erreichbar</a> ist und <a href="http://code.google.com/intl/de-DE/apis/talk/open_communications.html">auch Google Talk das Jabber Protokoll nutzt</a>, kann man sich sicherlich über ein paar spannende Implementierungen in naher Zukunft freuen!

(via: <a href="http://ripanti.yiid.com/" rel="contact met yiid colleague co-worker">Marco Ripanti</a>)

<!--more-->Für die Audio/Visuellen unter euch, gibt es natürlich auch wieder ein kurzes Video:

https://www.youtube.com/watch?v=o7Pt0PXC_Bs