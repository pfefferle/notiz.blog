---
ID: 1958
post_title: ActivityStrea.ms Extension for WordPress
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/09/18/activitystrea-ms-extension-for-wordpress/
published: true
post_date: 2009-09-18 19:01:06
---
<!-- wp:paragraph -->
<p>Ich habe mal ein kleines <a href="http://wordpress.org/extend/plugins/activitystream-extension/">Plugin</a> geschrieben welches den WordPress-Atom-Feed mit der <a href="http://martin.atkins.me.uk/specs/activitystreams/atomactivity">ActivityStream-Syntax</a> erweitert.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code> &lt;entry>
  &lt;id>https://notiz.blog/?p=1775&lt;/id>
  &lt;author>
    &lt;name>Matthias Pfefferle&lt;/name>
    &lt;uri>https://notiz.blog&lt;/uri>
  &lt;/author>
  &lt;...>
  &lt;activity:verb>http://activitystrea.ms/schema/1.0/post&lt;/activity:verb>
  &lt;activity:object>
    &lt;activity:object-type>http://activitystrea.ms/schema/1.0/blog-entry&lt;/activity:object-type>
    &lt;activity:object-type>http://activitystrea.ms/schema/1.0/article&lt;/activity:object-type>
    &lt;id>tag:notiz.blog,2009-07-13:/post/1775&lt;/id>
    &lt;title type="html">&lt;![CDATA[Matthias Pfefferle posted a new blog-entry]]>&lt;/title>
    &lt;link rel="alternate" type="text/html" href="https://notiz.blog/2009/07/14/webstandards-kolumne/" />
  &lt;/activity:object>
&lt;/entry></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Die Syntax ist dazu gedacht, dem Feed-Parser/Feed-Reader zu erklären um was für einen Eintrag es sich handelt. Bei WordPress sind die <code>&lt;entry /></code>s ausschließlich Blogposts/Artikel...</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;activity:object-type>http://activitystrea.ms/schema/1.0/blog-entry&lt;/activity:object-type>
&lt;activity:object-type>http://activitystrea.ms/schema/1.0/article&lt;/activity:object-type></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...die gepostet wurden.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;activity:verb>http://activitystrea.ms/schema/1.0/post&lt;/activity:verb></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Und für die Dienste wie <a href="http://pfefferle.org/">NoseRub</a>, die die Aktivität gerne in einen Satz packen, gibt's das ganze auch noch in Prosa.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;title type="html">&lt;![CDATA[Matthias Pfefferle posted a new blog-entry]]>&lt;/title></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Das <a href="http://martin.atkins.me.uk/specs/activitystreams/activityschema">ActivityStream Schema</a> definiert übrigens noch 'ne ganze Reihe an weiteren Objekten und Verben, die auf alle möglichen Aktionen im Netz passen. Falls ihr also noch welche findet, die zu WordPress passen könnten... lasst es mich wissen ;)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Es gibt leider aber auch ein paar <a href="http://blog.openwebpodcast.de/107/episode-14-was-bringt-eigentlich-data-portability/comment-page-1/#comment-33">Probleme mit der Syntax und diversen Feed-Readern</a>, die das zweite <code>&lt;title /></code> im <code>&lt;activity-object /></code> mit interpretieren und dann beide Titel ausgeben... aber da ja auch <a href="http://wiki.developer.myspace.com/index.php?title=Standards_for_Activity_Streams">MySpace</a> und <a href="http://wiki.developers.facebook.com/index.php/Using_Activity_Streams">Facebook</a> die ActivityStream-Syntax einsetzen ist dieser Fehler sicherlich bald bei jedem Feed-Reader behoben ;)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Viel Spaß beim ausprobieren!</p>
<!-- /wp:paragraph -->