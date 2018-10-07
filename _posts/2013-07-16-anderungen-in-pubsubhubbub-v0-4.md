---
ID: 5420
post_title: Änderungen in PubSubHubbub v0.4
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2013/07/16/anderungen-in-pubsubhubbub-v0-4/
published: true
post_date: 2013-07-16 12:52:16
---
<img src="//notiz.blog/wp-content/uploads/2013/07/pubsubhubbub-logo.png" alt="pubsubhubbub-logo" width="113" height="38" class="alignright size-full wp-image-5423" />Seit ein paar Wochen scheint die <a href="https://superfeedr-misc.s3.amazonaws.com/pubsubhubbub-core-0.4.html#publishing">Version 0.4</a> von <a href="https://code.google.com/p/pubsubhubbub/">PubSubHubbub</a> relativ stabil zu sein... immerhin so stabil, dass <a href="http://googledevelopers.blogspot.de/2013/07/pubsubhubbub-feeds-and-feed-api.html">Google</a> und <a href="http://blog.superfeedr.com/pubsubhubbub-04/">Superfeedr</a> ihre Hubs an die neue Spec angepasst haben.

Die wesentlichen Unterschiede zu der Vorgängerversion sind:

<ul>
<li>Alle Datentypen werden unterstützt: Neben RSS/Atom können jetzt auch vCards, beliebige XML oder JSON Datein oder auch Bilder ge-push-t werden</li>
<li>Statt HTML/Atom-Links werden <a href="http://tools.ietf.org/html/rfc5988">HTTP-Link-Header</a> benutzt</li>
<li>Der Pubslisher-Prozess ist nicht mehr über die Spezifikation definiert</li>
</ul>

Für die zwei großen Hubs sollte es reichen wenn ihr eure Feed-&lt;link /&gt;s ("hub" und "self"):

<pre><code>&lt;?xml version="1.0"?&gt;
&lt;atom:feed&gt;

  &lt;link rel="hub" href="http://myhub.example.com/endpoint" /&gt;
  &lt;link rel="self" href="http://publisher.example.com/happycats.xml" /&gt;

&lt;/atom:feed&gt;</code></pre>

...zusätzlich über die HTTP-Header ausliefert:

<pre><code>HTTP/1.1 200 OK
Date: Tue, 03 Apr 2012 08:02:19 GMT
Content-Type: text/html
Content-Length: 11261
Link: &lt;http://http://myhub.example.com/endpoint&gt;; rel="hub"
Link: &lt;http://publisher.example.com/happycats.xml&gt;; rel="self"</code></pre>

Leider ist die Version 0.4 aber nicht 100% abwärts-kompatibel... Die wahrscheinlich größte (und für mich enttäuschendste) Änderung ist das bewusste Weglassen des <a href="https://superfeedr-misc.s3.amazonaws.com/pubsubhubbub-core-0.4.html#publishing">Publisher-Prozesses</a>:

<blockquote>The publisher MUST inform the hubs it previously designated when a topic has been updated. The hub and the publisher can agree on any mechanism, as long as the hub is eventually able send the updated payload to the subscribers.</blockquote>

Auf der einen Seite kann das ein enormer Vorteil für Publisher sein, da Hubs in Zukunft auch per E-Mail, SMS, Pingbacks/Trackbacks oder XMPP über Updates informieren werden könnten. Auf der anderen Seite ist es aber auch sehr Wahrscheinlich, dass man für jedes v0.4 Hub eine individuelle Implementierung benötigt. Bisher unterstützen beide großen Hubs (Google und Superfeedr) aber weiterhin das alte <a href="http://pubsubhubbub.googlecode.com/svn/trunk/pubsubhubbub-core-0.3.html#publishing">Verfahren</a>, also kein Grund sich jetzt schon Sorgen zu machen...

Alles in allem finde ich die Änderungen aber ganz nett und hoffe dass "<a href="http://en.wikipedia.org/wiki/Polling_(computer_science)">Polling</a>" bald der Vergangenheit angehört...