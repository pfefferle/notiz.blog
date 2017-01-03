---
ID: 791
post_title: hCardMapper für WordPress
author: Matthias Pfefferle
post_date: 2008-04-02 20:21:51
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/04/02/hcardmapper-fuer-wordpress/
published: true
aktt_tweeted:
  - "1"
---
Wie in meinem letzten <a href="http://notiz.blog/2008/03/28/hcard-mapper/">Post über den hCardMapper</a> beschrieben, war es in der Tat nicht möglich den Microformats-Parser/Proxy ohne weitere Probleme auszutauschen. Die generierten <a href="http://microformats.org/wiki/json">JSON Formate</a> der einzelnen Parser (<a href="http://lab.backnetwork.com/ufXtract/">ufXtract</a>, <a href="http://microformats.org/wiki/hKit">hKit</a>, <a href="http://mofo.rubyforge.org/">mofo</a>) unterscheiden sich an einigen Stellen zu sehr um sie alle gleich behandeln zu können. Soweit zur schlechten Nachricht...

Die gute Nachricht ist, dass sich <a href="http://www.omnia-computing.de">Gordon Oheim</a> (der Macher des <a href="http://lib.omnia-computing.de/hcardmapper">hCardMappers</a>) nochmal alle JSON Formate vorgenommen und eine neue Version gebastelt hat:

<blockquote>v0.94 - Added better support for JSON returned by Optimus, ufXtract and hKit.</blockquote>

Der Mapper sollte also mit mofo, Optimus, ufXtract and hKit problemlos funktionieren.

Die nächste tolle Nachricht ist, dass Gordon auch auf einen kleinen Änderungswunsch von mir sofort eingegangen ist, so dass wir euch jetzt eine <em>hCardMapper Edition</em> von dem <a href="http://notiz.blog/projects/wp-hcard-commenting/">WordPress hCard-Commenting Plugin</a> anbieten können :).

<p class="download">Download: <del datetime="2008-04-07T09:23:09+00:00"><a href='http://notiz.blog/wp-content/uploads/2008/04/wp-hcard-mapper.zip' rel='enclosure'>hCardMapper for WordPress v0.1</a></del> <ins datetime="2008-04-07T09:23:09+00:00"><a href="http://wordpress.org/extend/plugins/hcardmapper/">hCardMapper bei WordPress.org</a></ins></p>

Wenn ihr immer die aktuelle Version haben wollt, hier ist der <a href="http://svn.wp-plugins.org/hcard-commenting/branches/">Link zum SVN</a>.

Ich hab das Plugin auch mal auf notizBlog aktiviert und würde mich über euer Feedback freuen. Macht es Sinn über das Admin-Menü zwischen beiden Versionen (hCard-Commenting und hCardMapper-Commenting) zu wechseln?

Ein dickes Danke nochmal an Gordon für seine tolle und schnelle Arbeit... tolles Script.