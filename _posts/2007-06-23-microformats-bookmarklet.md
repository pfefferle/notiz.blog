---
ID: 496
post_title: Microformats Bookmarklet
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/06/23/microformats-bookmarklet/
published: true
post_date: 2007-06-23 17:59:07
---
<!-- wp:paragraph -->
<p>Auf <a href="http://leftlogic.com/lounge/articles/microformats_bookmarklet">leftlogic.com</a> hab ich ein kleines <a href="http://de.wikipedia.org/wiki/Bookmarklet">Bookmarklet</a> zum Anzeigen und Speichern von Microformats gefunden.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2007/06/mac_microformat.jpg" alt="Microformats Bookmarklet" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Die Idee kommt von <a href="http://www.hicksdesign.co.uk">hicksdesigns</a> "<a href="http://www.hicksdesign.co.uk/journal/a-proposal-for-a-safari-microformats-plugin">A Proposal for a Safari Microformats plugin</a>" und aus der Not heraus, dass es (im gegensatz zum <a href="https://notiz.blog/2007/01/03/tails-vs-operator/">Firefox</a>) für den Safari kein Microformats Plugin gibt.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Bookmarklet</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Einfach den unten aufgeführten Link in die Bookmarkleiste ziehen, fertig.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Bookmarklet: <strong><a href="javascript:if%20(!document.getElementById('MF_jq'))%20{var%20q=document.createElement('script');q.setAttribute('id',%20'MF_jq');q.setAttribute('src',%20'http://code.jquery.com/jquery-latest.pack.js');document.getElementsByTagName('body')[0].appendChild(q);}%20var%20s=document.createElement('script');s.setAttribute('id','MF_loader');%20s.setAttribute('src',%20'http://leftlogic.com/js/microformats.js');document.getElementsByTagName('head')[0].appendChild(s);void(s);">Microformats</a></strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Unterstützte Mikroformate sind <a href="http://microformats.org/wiki/hCard">hCard</a> und <a href="http://microformats.org/wiki/hCalendar">hCalendar</a>.</p>
<!-- /wp:paragraph -->