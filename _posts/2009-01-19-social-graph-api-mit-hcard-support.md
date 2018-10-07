---
ID: 1394
post_title: Social Graph API mit hCard Support?
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/01/19/social-graph-api-mit-hcard-support/
published: true
post_date: 2009-01-19 13:18:41
---
<!-- wp:paragraph -->
<p>Ich bin durch Zufall mal wieder auf der <a href="http://code.google.com/apis/socialgraph/docs/api.html"><abbr title="SocialGraph">SG</abbr>-API</a> Seite gelandet und war wirklich positiv überrascht dass die <abbr title="Application Programming Interface">API</abbr> noch stetig weiterentwickelt wird. Besonders spannend finde ich die Integration zweier <a href="http://buzzword.org.uk/profiles/hCard/1.0/">hCard-Attribute</a>: <abbr title="formatted name"><a href="http://www.w3.org/2006/03/hcard#fn">fn</a></abbr> und <a href="http://www.w3.org/2006/03/hcard#photo">photo</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>{
 "http://example-bob.livejournal.com/": {
  "attributes": {
   "atom": "http://example-bob.livejournal.com/data/atom",
   "foaf": "http://example-bob.livejournal.com/data/foaf",
   "rss": "http://example-bob.livejournal.com/data/rss",
   "fn": "Mr. Example Bob",
   "photo": "http://p-userpic.livejournal.com/example-bob", 
   "url": "http://example-bob.livejournal.com/",
   "profile": "http://example-bob.livejournal.com/profile"
  }
 }
}</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Ich denke nicht, dass Google die hCard vollständig in den <em>Sozialen Graphen</em> integrieren wird, aber es zeigt sehr schön, dass der Google-Index über alle notwendigen Informationen verfügt und die Integration von Microformats in die <a href="http://www.google.de">klassische <em>Google Suche</em></a> (à la <a href="https://notiz.blog/2008/06/19/searchmonkey-fuer-anwender/">SearchMonkey</a>) vielleicht doch nicht ganz abwegig ist.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Um richtig coole Dinge damit anstellen zu können fehlen mir persönlich jetzt noch zwei weitere hCard-Attribute und zwar <a href="http://www.w3.org/2006/03/hcard#nickname"><em>nickname</em></a> und <a href="http://www.w3.org/2006/03/hcard#email"><em>email</em></a>... aber man will ja nicht undankbar sein :)</p>
<!-- /wp:paragraph -->