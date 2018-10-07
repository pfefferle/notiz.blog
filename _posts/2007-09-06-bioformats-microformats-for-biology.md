---
ID: 562
post_title: 'bioformats: microformats for biology'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/09/06/bioformats-microformats-for-biology/
published: true
post_date: 2007-09-06 14:49:56
---
<!-- wp:image {"align":"center"} -->
<div class="wp-block-image"><figure class="aligncenter"><img src="https://notiz.blog/wp-content/uploads/2007/09/bioformats.png" alt="bioformats"/></figure></div>
<!-- /wp:image -->

<!-- wp:quote -->
<blockquote class="wp-block-quote"><p>Modern biological research is reliant on the data and tools made available on the web. However, even as the volume of biological data grows, and as new tools arrive to accommodate this growth, putting them to work is not straightforward. Cut and paste, screen scrapers and custom parsers are all common place. Microformats offer an alternative. <a href="http://www.bioformats.org/">﻿</a></p><cite><a href="http://www.bioformats.org/">#</a></cite></blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Bioformats sind Mikroformate um biologische Daten abzubilden. Es gibt schon ein paar <em>Working Drafts</em> für <a href="http://www.bioformats.org/hProtein/">Proteine</a>, <a href="http://www.bioformats.org/hGene/">Gene</a> und <a href="http://www.bioformats.org/hSequence/">Abläufe</a>, wobei bisher nur die <a href="http://www.bioformats.org/hGene/">hGenes</a> ausformuliert wurden.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ein hGene könnte wie folgt aussehen:
</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class='hgene'>
  &lt;span class='name'>BRCA2&lt;/span>
  &lt;p class='description'>
    Breast cancer type 2 susceptibility protein 
    (Fanconi anemia group D1 protein)	
  &lt;/p>
  &lt;ul>
    &lt;li>Genbank: &lt;a href='genbank.pl?U43746' class='ident' rel='genbank'>U43746&lt;/a>&lt;/li>
    &lt;li>Entrez: &lt;a href='entrez.pl?675' class='ident' rel='entrez'>675&lt;/a>&lt;/li>
    &lt;li>Location: &lt;a href='lookup.pl?675' class='location' rel='homo_sapiens'>13:31787611-31871347&lt;/a>&lt;/li>	  
  &lt;/ul>
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Witzige Idee... vor allem das Logo!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Mal schauen was neben <a href="http://microformats.org">Microformats</a>, <a href="http://twitternanoformats.wikispaces.com/">Nanoformats</a>, <a href="http://microformats.org/wiki/picoformats">Picoformats</a> und jetzt auch <a href="http://www.bioformats.org">Bioformats</a> noch so alles entsteht.</p>
<!-- /wp:paragraph -->