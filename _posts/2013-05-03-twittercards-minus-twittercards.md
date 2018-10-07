---
ID: 5105
post_title: TwitterCards minus TwitterCards
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2013/05/03/twittercards-minus-twittercards/
published: true
post_date: 2013-05-03 08:21:14
---
<!-- wp:image {"id":5107,"align":"center","className":"size-full wp-image-5107"} -->
<figure class="wp-block-image aligncenter size-full wp-image-5107"><a href="http://garfieldminusgarfield.net/post/26271055"><img src="https://notiz.blog/wp-content/uploads/2013/04/garfield-minus-garfield.png" alt="Garfield minus Garfield comic" class="wp-image-5107"/></a>
	<figcaption> Image from Garfield minus Garfield</figcaption>
</figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Ich war nie ein <a href="https://notiz.blog/2012/06/22/twitter-cards/">großer Fan der <em>Twitter Cards</em></a>, was aber nicht wirklich schlimm ist, da Twitter das <em>Open Graph Protocol</em> als vollwertiges Fallback unterstützt... unterstützt hat...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Seit ein paar Wochen scheint den feinen Herren das <em>Open Graph Protocol</em> aber nicht mehr auszureichen und meinen Links fehlt der schöne, kleine Teaser :(</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Zum Glück reicht aber ein Meta-Tag um das ganze wieder zum laufen zu bekommen. Twitter unterstützt verschiedene Arten von Previews, welche über <code>&lt;meta name="twitter:card" content="summary" /></code> festgelegt werden. Neben <code>summary</code> (für Texte) gibt es auch noch <code>photo</code> für Bilder und <code>player</code> für Audio/Video (die komplette Liste findet ihr <a href="https://dev.twitter.com/docs/cards">hier</a>). Ich würde euch außerdem noch den <code>twitter:creator</code> empfehlen, mit dem ihr auf den Twitter-Account des Autors hinweisen könnt. Für meinen Blog sieht das wie folgt aus:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;meta name="twitter:creator" content="@pfefferle" />
&lt;meta name="twitter:card" content="summary" /></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Wenn ihr sicher gehen wollt ob ihr alles richtig gemacht habt, könnt ihr eure Seite mit dem <em><a href="https://dev.twitter.com/docs/cards/validation/validator">Twitter Card Validator</a></em> testen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Den WordPresslern unter euch kann ich außerdem folgende Plugins empfehlen:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><a href="http://wordpress.org/extend/plugins/opengraph/">Open Graph</a> - Keine Settings, kein Know-How, alles vollkommen Idiotensicher.</li>
	<li><a href="https://github.com/pfefferle/twitter-creator">twitter:creator</a> - Setzt zusätzlich die angesprochenen <code>twitter:creator</code> und <code>twitter:card</code>.</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>...also viel Spaß beim <em>Twitter Cards</em> Boykott ;).</p>
<!-- /wp:paragraph -->