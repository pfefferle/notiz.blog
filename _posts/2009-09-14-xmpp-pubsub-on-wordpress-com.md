---
ID: 1878
post_title: XMPP PubSub on WordPress.com
author: Matthias Pfefferle
post_date: 2009-09-14 22:57:06
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/09/14/xmpp-pubsub-on-wordpress-com/
published: true
---
<a href="http://joss.blogs.lincoln.ac.uk">Joss Winn</a> hatte schon im Mai darüber berichtet, dass <a href="http://joss.blogs.lincoln.ac.uk/2009/05/05/xmpp-pubsub-on-wordpresscom/">WordPress.com jetzt auch XMPP unterstützt</a>:

<blockquote>Just some notes on how to get XMPP notifications from any wordpress.com blog. It’s an experimental service so might not work tomorrow ;)</blockquote>

...und es hat in der Tat am nächsten Tag nicht mehr funktioniert. Durch den ganzen <a href="http://en.blog.wordpress.com/2009/09/07/rss-in-the-clouds/">Trubel um WordPress, <em>RSS cloud</em> und dem Echtzeitweb</a> in den letzten Tagen, bin ich auch wieder auf den WordPress <abbr title="Extensible Messaging and Presence Protocol">XMPP</abbr>-Service aufmerksam geworden und er scheint mittlerweile relativ stabil zu laufen.

Es sollte eigentlich mit jedem Jabber-Client funktionieren der <abbr title="Publish/Subscribe">PubSub</abbr> (<a href="http://xmpp.org/extensions/xep-0060.html"><abbr title="XMPP Extension Protocol">XEP</abbr>-0060</a>) unterstützt:

<ol>
<li>Zuerst einen neuen Jabber/XMPP-Account hinzufügen:
<ul>
<li><strong>Jabber ID</strong><br />
<em>name@im.wordpress.com</em><br />
Der <em>name</em> ist der WordPress.com Benutzer-Name gefolgt von “@im.wordpress.com”.</li>
<li><strong>Password</strong><br />
Das WordPress.com Passwort.</li>
<li><strong>Jabber Server/Host</strong><br>
<em>im.wordpress.com</em></li>
<li><strong>Port</strong><br />
<em>5222</em> (Standard-Port)</li>
</ul>
</li>
<li>Dann den <em>WordPress-Bot</em> als Kontakt hinzufügen: "<strong>bot@im.wordpress.com</strong>"</li>
<li>Für alle weiteren Anweisungen einfach dem <em>WordPress-Bot</em> eine Nachricht mit "<strong>help</strong>" schicken.</li>
<li>Fertsch :)</li>
</ol>

<img src="http://notiz.blog/wp-content/uploads/2009/09/im-wordpress-com.png" alt="XMPP on WordPress.com" title="XMPP on WordPress.com" width="480" height="300" class="aligncenter size-full wp-image-1898" />

Nachdem man mit dem Befehl "<strong>sub &lt;wordpress-url&gt;</strong>" einen Blog abonniert hat bekommt man alle neuen Posts auf den Jabber-Client und wenn es der eigene Blog ist, kann man sogar über z.B. Adium neue Blog-Posts verfassen.

Großartig!

...wer braucht da noch <a href="http://code.google.com/p/pubsubhubbub/">PubSubHubBub</a> und <a href="http://rsscloud.org/">RSS cloud</a> :)

Weiterführende Links:
<ul><li><a href="http://im.wordpress.com/" rel="bookmark">im.wordpress.org</a></li>
<li><a href="http://support.wordpress.com/jabber/">WordPress.com Jabber Support</a></li></ul>