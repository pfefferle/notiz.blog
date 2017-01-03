---
ID: 4678
post_title: 'Schema.org &#8211; what I&#8217;ve learned so far'
author: Matthias Pfefferle
post_date: 2012-09-21 12:00:46
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2012/09/21/schema-org-what-ive-learned-so-far/
published: true
---
<img src="http://notiz.blog/wp-content/uploads/2012/09/html5-badge-h-semantics.png" alt="HTML5 Semantics Badge" width="133" height="64" class="alignright size-full wp-image-4680" />Beim "basteln" an <a href="http://notiz.blog/2012/09/06/ive-made-a-wordpress-theme-kind-of/">SemPress</a>, meinem ersten WordPress Theme, habe ich das erste Mal praktische Erfahrungen mit <a href="http://schema.org/">Schema.org</a> gesammelt und mir sind vor allem zwei Dinge klar geworden: 1. Warum Schema.org nach einer Art "Vererbungs"-Prinzip aufgebaut ist und 2. Wie Google mit Schema.org umgeht.

<h2>The <small>http://schema.org/</small>Thing</h2>

Das "einfachste" Schema ist ein "<a href="http://www.schema.org/Thing">Thing</a>" und hat folgende Attribute:

<table>
  <tbody>
    <tr>
      <th><code>description</code></th>
      <td>TEXT</td>
      <td>A short description of the item.</td>
    </tr>
    <tr>
      <th><code>image</code></th>
      <td>URL</td>
      <td>URL of an image of the item.</td>
    </tr>
    <tr>
      <th><code>name</code></th>
      <td>TEXT</td>
      <td>The name of the item.</td>
    </tr>
    <tr>
      <th><code>url</code></th>
      <td>URL</td>
      <td>URL of the item.</td>
    </tr>
  </tbody>
</table>

Da alle anderen Objekte auf dem "Thing" aufbauen, kann man davon ausgehen dass man mind. auf diese vier Eigenschaften zugreifen kann und genau <strong>das</strong> ist der ganze Sinn hinter dieser Struktur.

Vor allem Google setzt massiv auf Schema.org, sei es beim Einsatz in der Suche (über die sogenannten <a href="http://support.google.com/webmasters/bin/answer.py?hl=en&answer=99170&topic=21997&ctx=topic">Rich-Snippets</a>)...

<img src="http://notiz.blog/wp-content/uploads/2012/09/richsnippet-schema-example.png" alt="rich snippets example" title="rich snippets example" width="600" height="170" class="aligncenter size-full wp-image-4699" />

...oder beim Anreichern der, über <a href="https://developers.google.com/+/plugins/snippet/">Google+ oder den +1 Button</a> geteilten Links.

<img src="http://notiz.blog/wp-content/uploads/2012/09/googleplus-schema-example.png" alt="Google+ Example" title="Google+ Example" width="600" height="326" class="aligncenter size-full wp-image-4700" />

Um das Parsen der Webseiten (zumindest für diese eher einfachen Ausgaben) auf ein Minimum zu reduzieren, ist die Grundstruktur immer gleich und alles darüber hinaus ist reine Kür. Wahrscheinlich werden aber 90% aller Anwendungen mit Titel (name), Beschreibung, Bild und URL auskommen.

<h2>Googles Umgang mit Schema.org</h2>

Wer seine Seite mit Schema.org auszeichnen möchte, sollte vor allem eines Beachten: <strong>Google+ (wahrscheinlich aber auch alle anderen Google Produkte) interpretiert immer das erste im Quellcode verwendete Schema!</strong>

Bei meiner ersten Implementierung von Schema.org habe ich mich etwas zu sehr an RSS bzw. Atom orientiert und folgenden Aufbau gewählt: Ein umschließendes Objekt um den Blog zu beschreiben und ein oder mehrere referenzierte Artikel.

<pre><code>&lt;body itemscope itemtype="http://schema.org/Blog"&gt;
...
  &lt;header id="branding" role="banner"&gt;
    &lt;hgroup&gt;
      &lt;h1 id="site-title" itemprop="name"&gt;&lt;?php bloginfo( 'name' ); ?&gt;&lt;/h1&gt;
      &lt;h2 id="site-description" itemprop="description"&gt;&lt;?php bloginfo( 'description' ); ?&gt;&lt;/h2&gt;
    &lt;/hgroup&gt;
  &lt;/header&gt;
...
  &lt;article itemprop="blogPost" itemscope itemtype="http://schema.org/BlogPosting"&gt;
  ...
  &lt;/article&gt;
  &lt;article itemprop="blogPost" itemscope itemtype="http://schema.org/BlogPosting"&gt;
  ...
  &lt;/article&gt;
...
&lt;/body&gt;</code></pre>

Egal ob es jetzt um mehrere Artikel (Startseite) oder nur einen Artikel (Post oder Page) gehandelt hat.

Das hat bei Google+ dazu geführt, dass die notizBlog-Links immer mit dem Titel, der Beschreibung und dem Bild des Blogs und nicht mit denen des Artikels verknüpft wurden. Es ist also gerade für Blogs wichtig, dass das <a href="http://schema.org/Blog">Blog-Schema</a> nur auf den Übersichtsseiten benutzt wird und die Einzelansichten lediglich mit "http://schema.org/BlogPosting" bzw. "http://schema.org/WebPage" ausgezeichnet werden.