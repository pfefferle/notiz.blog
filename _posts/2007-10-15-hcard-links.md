---
ID: 611
post_title: hCard Links
author: Matthias Pfefferle
post_date: 2007-10-15 17:06:43
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/10/15/hcard-links/
published: true
---
<span class="vcard"><a class="url" href="http://adactio.com"><abbr class="fn" title="Jeremy Keith">Jeremy</abbr></a></span> beschreibt in seinem <a href="http://adactio.com/journal/1358">Weblog</a> wie man mit Hilfe des <code>abbr</code> Tags eine vollständige hCard für Links erstellen kann.

Sein Problem:
<blockquote>I would still make his name a hyperlink but what can I do about making this text into an hCard? Should I change my writing style and refer to everyone by their full formated name even if the context and writing style would favour just using their first name?</blockquote>

Will man eine hCard erstellen bei der nur der Vorname angezeigt wird, wird natürlich auch nur der Vorname ins Adressbuch übernommen:

<pre><code>&lt;span class="vcard"&gt;
  &lt;a class="fn url" href="http://example.com/"&gt;
    Max
  &lt;/a&gt;
&lt;/span&gt;
</code></pre>

Die Lösung des Problems ist die Nutzung des <code>abbr</code> Tags:

<pre><code>&lt;span class="vcard"&gt;
  &lt;a class="url" rel="friend met" href="http://example.com/"&gt;
    &lt;abbr class="fn" title="Max Mustermann"&gt;
      Max
    &lt;/abbr&gt;
  &lt;/a&gt;
&lt;/span&gt;
</code></pre>

Schicke Idee, fragt sich nur ob der Vorname als <em>Abbreviate</em> (Abkürzung) durch geht und die Nutzung von <code>&lt;abbr&gt;</code> <a href="http://www.webstandards.org/2007/04/27/haccessibility/">gerechtfertigt</a> ist.