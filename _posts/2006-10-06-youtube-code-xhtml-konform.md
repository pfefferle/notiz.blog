---
ID: 167
post_title: YouTube Code XHTML konform
author: Matthias Pfefferle
post_date: 2006-10-06 11:10:54
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2006/10/06/youtube-code-xhtml-konform/
published: true
---
Irgendwie ist der original Code von YouTube zum Einbinden von Videos nicht XHTML konform, aber mit dem folgenden Code den ich bei <a href="http://www.wildbits.de/2006/04/02/youtube-xhtml/">wildbits.de</a> gefunden habe sollte es funktionieren.
<pre class="code">&lt;object type="application/x-shockwave-flash" 
  style="width:425px; height:350px" 
  data="http://www.youtube.com/v/DEINE_VIDEO_ID"&gt;
    &lt;param name="movie" 
    value="http://www.youtube.com/v/DEINE_VIDEO_ID"&gt;
    &lt;/param&gt;
&lt;/object&gt;</pre>
Als <a href="http://www.dm.hs-furtwangen.de/dm.php?template=_studiengang&sg=om&action=click&handler=menu&menuid=9">OnlineMedien</a> Student muß man einfach valide Seiten erstellen :)