---
ID: 3233
post_title: Accessing the OpenWeb with YQL
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2010/09/28/access-the-openweb-with-yql/
published: true
post_date: 2010-09-28 00:02:51
---
<!-- wp:image {"id":3282,"align":"right"} -->
<div class="wp-block-image"><figure class="alignright"><img src="https://notiz.blog/wp-content/uploads/2010/09/YQL.png" alt="" class="wp-image-3282"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Durch einen Artikel auf ReadWriteWeb (<a href="http://www.readwriteweb.com/hack/2010/09/10-great-yql-one-liners.php">5 Great YQL One-Liners</a>) bin ich nach langer Zeit mal wieder auf <a href="https://developer.yahoo.com/yql/">Yahoos YQL-Plattform</a> gelandet und habe nicht schlecht gestaunt, was die <em>Yahoo Query Language</em> mittlerweile alles leistet (mehr über YQL <a href="https://notiz.blog/2009/01/14/select-from-microformats/">hier</a>). Ich hatte z.B. keine Ahnung, dass man auch eigene <em><a href="http://datatables.org/">table definition</a></em> schreiben kann und dass es auch schon eine ziemlich fleißige Community um diese Definitionen gibt.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Meine Favoriten sind:</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>Microformats</h3>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>select * from microformats where url='http://wait-till-i.com'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...findet diverse Microformats. » <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&amp;env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20microformats%20where%20url%3D%27http%3A//wait-till-i.com%27">Direct Link</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Mehr dazu hier: <a href="https://notiz.blog/2009/01/14/select-from-microformats/">SELECT * FROM microformats</a></p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>OpenID</h3>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>select * from openid.discover where normalizedId="http://www.yahoo.com/"</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...klassische OpenID-Discovery. » <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&amp;env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20openid.discover%20where%20normalizedId%3D%22http%3A//www.yahoo.com/%22">Direct Link</a></p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>select * from openid.yadis where uri="http://www.yahoo.com/"</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...YADIS-Discovery. » <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&amp;env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20openid.yadis%20where%20uri%3D%22http%3A//www.yahoo.com/%22">Direct Link</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>...und es gibt noch 'ne Reihe anderer <em>OpenID Queries</em>... es sollte sogar möglich sein einen kompletten OpenID-Client mit YQL zu bauen.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3><strong>OAuth</strong>
</h3>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>select * from oauth where uri='http://example.com' and consumerKey='asd123' and consumerSecret='zxc456' and callbackUri='http://example.com';</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...sendet einen OAuth-Request. » <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&amp;env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20oauth%20where%20uri%3D%27http%3A//example.com%27%20and%20consumerKey%3D%27asd123%27%20and%20consumerSecret%3D%27zxc456%27%20and%20callbackUri%3D%27http%3A//example.com%27%3B">Direct Link</a></p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>pubsubhubbub</h3>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>insert into pubsubhubbub.publisher (hub_url, topic_url) values ('http://pubsubhubbub.appspot.com/publish', 'http://developer.yahoo.com')</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...sendet ein Update an das angegebene Hub. » <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&amp;env=store://datatables.org/alltableswithkeys#h=insert%20into%20pubsubhubbub.publisher%20%28hub_url%2C%20topic_url%29%20values%20%28%27http%3A//pubsubhubbub.appspot.com/publish%27%2C%20%27http%3A//developer.yahoo.com%27%29">Direct Link</a></p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>Webfinger</h3>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>select * from webfinger where account='pfefferle@gmail.com'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...Webfinger-Discovery. » <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&amp;env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20webfinger%20where%20account%3D%27pfefferle@gmail.com%27">Direct Link</a></p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3>OpenSocial</h3>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>select * from opensocial.people</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...sendet eine OpenSocial <em>People</em>-Anfrage. » <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&amp;env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20opensocial.people%20where%20ck%20%3D%20%22orkut.com%3A623061448914%22%20and%20cks%20%3D%20%22uynAeXiWTisflWX99KU1D2q5%22%20and%20count%20%3D%20%224%22%20and%20container%20%3D%20%22orkut%22%20and%20guid%20%3D%20%2203067092798963641994%22%20and%20selector%20%3D%20%22friends%22">Direct Link</a></p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3><strong>Social Graph</strong> API</h3>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>select * from socialgraph.lookup where q = "notiz.blog" AND edo = "1"</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...ermöglicht Zugriff auf Googles <a href="http://code.google.com/intl/de-DE/apis/socialgraph/"><em>Social Graph API</em></a>. » <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&amp;env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20socialgraph.lookup%20where%20q%20%3D%20%22notiz.blog%22%20AND%20edo%20%3D%20%221%22">Direct Link</a></p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":3} -->
<h3><strong>Atom</strong></h3>
<!-- /wp:heading -->

<!-- wp:code -->
<pre class="wp-block-code"><code>select * from atom where url='https://notiz.blog/feed/atom'</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...interpretiert Atom-Feeds mit allen möglichen Erweiterungen, beispielsweise der <a href="http://activitystrea.ms/spec/1.0/atom-activity-01.html">ActivityStreams-Extension</a>. » <a href="https://developer.yahoo.com/yql/console/?q=show%20tables&amp;env=store://datatables.org/alltableswithkeys#h=select%20*%20from%20atom%20where%20url%3D%27http%3A//notiz.blog/feed/atom%27">Direct Link</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Vielleicht bekomm' ich die Tage ja auch mal eine <em>Query</em> zusammen :)</p>
<!-- /wp:paragraph -->