---
ID: 4678
post_title: 'Schema.org &#8211; what I&#8217;ve learned so far'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2012/09/21/schema-org-what-ive-learned-so-far/
published: true
post_date: 2012-09-21 12:00:46
---
<!-- wp:image {"align":"right"} -->
<figure class="wp-block-image alignright" style="max-width:50%"><img src="https://notiz.blog/wp-content/uploads/2012/09/html5-badge-h-semantics.png" alt="HTML5 Semantics Badge" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Beim &quot;basteln&quot; an <a href="https://notiz.blog/2012/09/06/ive-made-a-wordpress-theme-kind-of/">SemPress</a>, meinem ersten WordPress Theme, habe ich das erste Mal praktische Erfahrungen mit <a href="http://schema.org/">Schema.org</a> gesammelt und mir sind vor allem zwei Dinge klar geworden: 1. Warum Schema.org nach einer Art &quot;Vererbungs&quot;-Prinzip aufgebaut ist und 2. Wie Google mit Schema.org umgeht.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>The http://schema.org/Thing</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Das &quot;einfachste&quot; Schema ist ein &quot;<a href="http://www.schema.org/Thing">Thing</a>&quot; und hat folgende Attribute:</p>
<!-- /wp:paragraph -->

<!-- wp:table {"align":"center"} -->
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
<!-- /wp:table -->

<!-- wp:paragraph -->
<p>Da alle anderen Objekte auf dem &quot;Thing&quot; aufbauen, kann man davon ausgehen dass man mind. auf diese vier Eigenschaften zugreifen kann und genau <strong>das</strong> ist der ganze Sinn hinter dieser Struktur.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Vor allem Google setzt massiv auf Schema.org, sei es beim Einsatz in der Suche (über die sogenannten <a href="http://support.google.com/webmasters/bin/answer.py?hl=en&amp;answer=99170&amp;topic=21997&amp;ctx=topic">Rich-Snippets</a>)...</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2012/09/richsnippet-schema-example.png" alt="rich snippets example" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>...oder beim Anreichern der, über <a href="https://developers.google.com/+/plugins/snippet/">Google+ oder den +1 Button</a> geteilten Links.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2012/09/googleplus-schema-example.png" alt="Google+ Example" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Um das Parsen der Webseiten (zumindest für diese eher einfachen Ausgaben) auf ein Minimum zu reduzieren, ist die Grundstruktur immer gleich und alles darüber hinaus ist reine Kür. Wahrscheinlich werden aber 90% aller Anwendungen mit Titel (name), Beschreibung, Bild und URL auskommen.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Googles Umgang mit Schema.org</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Wer seine Seite mit Schema.org auszeichnen möchte, sollte vor allem eines Beachten: <strong>Google+ (wahrscheinlich aber auch alle anderen Google Produkte) interpretiert immer das erste im Quellcode verwendete Schema!</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Bei meiner ersten Implementierung von Schema.org habe ich mich etwas zu sehr an RSS bzw. Atom orientiert und folgenden Aufbau gewählt: Ein umschließendes Objekt um den Blog zu beschreiben und ein oder mehrere referenzierte Artikel.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;body itemscope itemtype=&quot;http://schema.org/Blog&quot;&gt;
...
  &lt;header id=&quot;branding&quot; role=&quot;banner&quot;&gt;
    &lt;hgroup&gt;
      &lt;h1 id=&quot;site-title&quot; itemprop=&quot;name&quot;&gt;&lt;?php bloginfo( &#x27;name&#x27; ); ?&gt;&lt;/h1&gt;
      &lt;h2 id=&quot;site-description&quot; itemprop=&quot;description&quot;&gt;&lt;?php bloginfo( &#x27;description&#x27; ); ?&gt;&lt;/h2&gt;
    &lt;/hgroup&gt;
  &lt;/header&gt;
...
  &lt;article itemprop=&quot;blogPost&quot; itemscope itemtype=&quot;http://schema.org/BlogPosting&quot;&gt;
  ...
  &lt;/article&gt;
  &lt;article itemprop=&quot;blogPost&quot; itemscope itemtype=&quot;http://schema.org/BlogPosting&quot;&gt;
  ...
  &lt;/article&gt;
...
&lt;/body&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Egal ob es jetzt um mehrere Artikel (Startseite) oder nur einen Artikel (Post oder Page) gehandelt hat.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Das hat bei Google+ dazu geführt, dass die notizBlog-Links immer mit dem Titel, der Beschreibung und dem Bild des Blogs und nicht mit denen des Artikels verknüpft wurden. Es ist also gerade für Blogs wichtig, dass das <a href="http://schema.org/Blog">Blog-Schema</a> nur auf den Übersichtsseiten benutzt wird und die Einzelansichten lediglich mit &quot;http://schema.org/BlogPosting&quot; bzw. &quot;http://schema.org/WebPage&quot; ausgezeichnet werden.</p>
<!-- /wp:paragraph -->