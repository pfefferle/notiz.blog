---
ID: 611
post_title: hCard Links
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/10/15/hcard-links/
published: true
post_date: 2007-10-15 17:06:43
---
<!-- wp:paragraph -->
<p><a href="http://adactio.com"><abbr title="Jeremy Keith">Jeremy</abbr></a> beschreibt in seinem <a href="http://adactio.com/journal/1358">Weblog</a> wie man mit Hilfe des <code>abbr</code> Tags eine vollständige hCard für Links erstellen kann.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Sein Problem:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>I would still make his name a hyperlink but what can I do about making this text into an hCard? Should I change my writing style and refer to everyone by their full formated name even if the context and writing style would favour just using their first name?</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Will man eine hCard erstellen bei der nur der Vorname angezeigt wird, wird natürlich auch nur der Vorname ins Adressbuch übernommen:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;span class="vcard">
  &lt;a class="fn url" href="http://example.com/">
    Max
  &lt;/a>
&lt;/span>
</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Die Lösung des Problems ist die Nutzung des <code>abbr</code> Tags:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;span class="vcard">
  &lt;a class="url" rel="friend met" href="http://example.com/">
    &lt;abbr class="fn" title="Max Mustermann">
      Max
    &lt;/abbr>
  &lt;/a>
&lt;/span>
</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Schicke Idee, fragt sich nur ob der Vorname als <em>Abbreviate</em> (Abkürzung) durch geht und die Nutzung von <code>&lt;abbr></code> <a href="http://www.webstandards.org/2007/04/27/haccessibility/">gerechtfertigt</a> ist.</p>
<!-- /wp:paragraph -->