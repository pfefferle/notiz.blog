---
ID: 1958
post_title: ActivityStrea.ms Extension for WordPress
author: Matthias Pfefferle
post_date: 2009-09-18 19:01:06
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/09/18/activitystrea-ms-extension-for-wordpress/
published: true
---
Ich habe mal ein kleines <a href="http://wordpress.org/extend/plugins/activitystream-extension/">Plugin</a> geschrieben welches den WordPress-Atom-Feed mit der <a href="http://martin.atkins.me.uk/specs/activitystreams/atomactivity">ActivityStream-Syntax</a> erweitert.

<pre> &lt;entry&gt;
  &lt;id&gt;http://notiz.blog/?p=1775&lt;/id&gt;
  &lt;author&gt;
    &lt;name&gt;Matthias Pfefferle&lt;/name&gt;
    &lt;uri&gt;http://notiz.blog&lt;/uri&gt;
  &lt;/author&gt;
  &lt;...&gt;
  &lt;activity:verb&gt;http://activitystrea.ms/schema/1.0/post&lt;/activity:verb&gt;
  &lt;activity:object&gt;
    &lt;activity:object-type&gt;http://activitystrea.ms/schema/1.0/blog-entry&lt;/activity:object-type&gt;
    &lt;activity:object-type&gt;http://activitystrea.ms/schema/1.0/article&lt;/activity:object-type&gt;
    &lt;id&gt;tag:notiz.blog,2009-07-13:/post/1775&lt;/id&gt;
    &lt;title type="html"&gt;&lt;![CDATA[Matthias Pfefferle posted a new blog-entry]]&gt;&lt;/title&gt;
    &lt;link rel="alternate" type="text/html" href="http://notiz.blog/2009/07/14/webstandards-kolumne/" /&gt;
  &lt;/activity:object&gt;
&lt;/entry&gt;</pre>

Die Syntax ist dazu gedacht, dem Feed-Parser/Feed-Reader zu erklären um was für einen Eintrag es sich handelt. Bei WordPress sind die <code>&lt;entry /&gt;</code>s ausschließlich Blogposts/Artikel...

<pre>&lt;activity:object-type&gt;http://activitystrea.ms/schema/1.0/blog-entry&lt;/activity:object-type&gt;
&lt;activity:object-type&gt;http://activitystrea.ms/schema/1.0/article&lt;/activity:object-type&gt;</pre>

...die gepostet wurden.

<pre>&lt;activity:verb&gt;http://activitystrea.ms/schema/1.0/post&lt;/activity:verb&gt;</pre>

Und für die Dienste wie <a href="http://pfefferle.org/">NoseRub</a>, die die Aktivität gerne in einen Satz packen, gibt's das ganze auch noch in Prosa.

<pre>&lt;title type="html"&gt;&lt;![CDATA[Matthias Pfefferle posted a new blog-entry]]&gt;&lt;/title&gt;</pre>

Das <a href="http://martin.atkins.me.uk/specs/activitystreams/activityschema">ActivityStream Schema</a> definiert übrigens noch 'ne ganze Reihe an weiteren Objekten und Verben, die auf alle möglichen Aktionen im Netz passen. Falls ihr also noch welche findet, die zu WordPress passen könnten... lasst es mich wissen ;)

Es gibt leider aber auch ein paar <a href="http://blog.openwebpodcast.de/107/episode-14-was-bringt-eigentlich-data-portability/comment-page-1/#comment-33">Probleme mit der Syntax und diversen Feed-Readern</a>, die das zweite <code>&lt;title /&gt;</code> im <code>&lt;activity-object /&gt;</code> mit interpretieren und dann beide Titel ausgeben... aber da ja auch <a href="http://wiki.developer.myspace.com/index.php?title=Standards_for_Activity_Streams">MySpace</a> und <a href="http://wiki.developers.facebook.com/index.php/Using_Activity_Streams">Facebook</a> die ActivityStream-Syntax einsetzen ist dieser Fehler sicherlich bald bei jedem Feed-Reader behoben ;)

Viel Spaß beim ausprobieren!