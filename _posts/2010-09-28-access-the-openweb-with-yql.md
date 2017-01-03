---
ID: 3233
post_title: Accessing the OpenWeb with YQL
author: Matthias Pfefferle
post_date: 2010-09-28 00:02:51
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2010/09/28/access-the-openweb-with-yql/
published: true
---
<img src="http://notiz.blog/wp-content/uploads/2010/09/YQL.png" alt="" title="YQL" width="137" height="123" class="alignright size-full wp-image-3282" />Durch einen Artikel auf ReadWriteWeb (<a href="http://www.readwriteweb.com/hack/2010/09/10-great-yql-one-liners.php" title="Permanent link to 5 Great YQL One-Liners">5 Great YQL One-Liners</a>) bin ich nach langer Zeit mal wieder auf <a href="https://developer.yahoo.com/yql/">Yahoos YQL-Plattform</a> gelandet und habe nicht schlecht gestaunt, was die <em>Yahoo Query Language</em> mittlerweile alles leistet (mehr über YQL <a href="http://notiz.blog/2009/01/14/select-from-microformats/">hier</a>). Ich hatte z.B. keine Ahnung, dass man auch eigene <em><a href="http://datatables.org/">table definition</a></em> schreiben kann und dass es auch schon eine ziemlich fleißige Community um diese Definitionen gibt.

Meine Favoriten sind:

<strong>Microformats</strong>
<pre>select * from microformats where
url='http://wait-till-i.com'</pre>
...findet diverse Microformats. &raquo; <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20microformats%20where%20url%3D%27http%3A//wait-till-i.com%27">Direct Link</a>

Mehr dazu hier: <a href="http://notiz.blog/2009/01/14/select-from-microformats/">SELECT * FROM microformats</a>

<strong>OpenID</strong>
<pre>select * from openid.discover where
normalizedId="http://www.yahoo.com/"</pre>
...klassische OpenID-Discovery.  &raquo; <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20openid.discover%20where%20normalizedId%3D%22http%3A//www.yahoo.com/%22">Direct Link</a>

<pre>select * from openid.yadis where
uri="http://www.yahoo.com/"</pre>
...YADIS-Discovery. &raquo; <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20openid.yadis%20where%20uri%3D%22http%3A//www.yahoo.com/%22">Direct Link</a>

...und es gibt noch 'ne Reihe anderer <em>OpenID Queries</em>... es sollte sogar möglich sein einen kompletten OpenID-Client mit YQL zu bauen.

<strong>OAuth</strong>
<pre>select * from oauth where uri='http://example.com'
and consumerKey='asd123' and consumerSecret='zxc456'
and callbackUri='http://example.com';</pre>
...sendet einen OAuth-Request. &raquo; <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20oauth%20where%20uri%3D%27http%3A//example.com%27%20and%20consumerKey%3D%27asd123%27%20and%20consumerSecret%3D%27zxc456%27%20and%20callbackUri%3D%27http%3A//example.com%27%3B">Direct Link</a>

<strong>pubsubhubbub</strong>
<pre>insert into pubsubhubbub.publisher
(hub_url, topic_url) values
('http://pubsubhubbub.appspot.com/publish',
'http://developer.yahoo.com')</pre>

...sendet ein Update an das angegebene Hub. &raquo; <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&env=store://datatables.org/alltableswithkeys#h=insert%20into%20pubsubhubbub.publisher%20%28hub_url%2C%20topic_url%29%20values%20%28%27http%3A//pubsubhubbub.appspot.com/publish%27%2C%20%27http%3A//developer.yahoo.com%27%29">Direct Link</a>

<strong>Webfinger</strong>
<pre>select * from webfinger where
account='pfefferle@gmail.com'</pre>
...Webfinger-Discovery. &raquo; <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20webfinger%20where%20account%3D%27pfefferle@gmail.com%27">Direct Link</a>

<strong>OpenSocial</strong>
<pre>select * from opensocial.people</pre>
...sendet eine OpenSocial <em>People</em>-Anfrage. &raquo; <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20opensocial.people%20where%20ck%20%3D%20%22orkut.com%3A623061448914%22%20and%20cks%20%3D%20%22uynAeXiWTisflWX99KU1D2q5%22%20and%20count%20%3D%20%224%22%20and%20container%20%3D%20%22orkut%22%20and%20guid%20%3D%20%2203067092798963641994%22%20and%20selector%20%3D%20%22friends%22">Direct Link</a>

<strong>Social Graph API</strong>
<pre>select * from socialgraph.lookup where
q = "notiz.blog" AND edo = "1"</pre>
...ermöglicht Zugriff auf Googles <a href="http://code.google.com/intl/de-DE/apis/socialgraph/"><em>Social Graph API</em></a>. &raquo; <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20socialgraph.lookup%20where%20q%20%3D%20%22notiz.blog%22%20AND%20edo%20%3D%20%221%22">Direct Link</a>

<strong>Atom</strong>
<pre>select * from atom where
url='http://notiz.blog/feed/atom'</pre>
...interpretiert Atom-Feeds mit allen möglichen Erweiterungen, beispielsweise der <a href="http://activitystrea.ms/spec/1.0/atom-activity-01.html">ActivityStreams-Extension</a>. &raquo; <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20atom%20where%20url%3D%27http%3A//notiz.blog/feed/atom%27">Direct Link</a>

Vielleicht bekomm' ich die Tage ja auch mal eine <em>Query</em> zusammen :)