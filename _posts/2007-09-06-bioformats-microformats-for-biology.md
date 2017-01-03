---
ID: 562
post_title: 'bioformats: microformats for biology'
author: Matthias Pfefferle
post_date: 2007-09-06 14:49:56
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/09/06/bioformats-microformats-for-biology/
published: true
---
<img class="aligncenter" src='http://notiz.blog/wp-content/uploads/2007/09/bioformats.png' alt='bioformats' />

<blockquote>Modern biological research is reliant on the data and tools made available on the web. However, even as the volume of biological data grows, and as new tools arrive to accommodate this growth, putting them to work is not straightforward. Cut and paste, screen scrapers and custom parsers are all common place. Microformats offer an alternative. <a href="http://www.bioformats.org/">#</a></blockquote>

Bioformats sind Mikroformate um biologische Daten abzubilden. Es gibt schon ein paar <em>Working Drafts</em> für <a href="http://www.bioformats.org/hProtein/">Proteine</a>, <a href="http://www.bioformats.org/hGene/">Gene</a> und <a href="http://www.bioformats.org/hSequence/">Abläufe</a>, wobei bisher nur die <a href="http://www.bioformats.org/hGene/">hGenes</a> ausformuliert wurden.

Ein hGene könnte wie folgt aussehen:
<pre class="code">&lt;div class='hgene'&gt;
  &lt;span class='name'&gt;BRCA2&lt;/span&gt;
  &lt;p class='description'&gt;
    Breast cancer type 2 susceptibility protein 
    (Fanconi anemia group D1 protein)	
  &lt;/p&gt;
  &lt;ul&gt;

    &lt;li&gt;Genbank: &lt;a href='genbank.pl?U43746' class='ident' rel='genbank'&gt;U43746&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;Entrez: &lt;a href='entrez.pl?675' class='ident' rel='entrez'&gt;675&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;Location: &lt;a href='lookup.pl?675' class='location' rel='homo_sapiens'&gt;13:31787611-31871347&lt;/a&gt;&lt;/li&gt;	  
  &lt;/ul&gt;

&lt;/div&gt;</pre>


Witzige Idee... vor allem das Logo!

Mal schauen was neben <a href="http://microformats.org">Microformats</a>, <a href="http://twitternanoformats.wikispaces.com/">Nanoformats</a>, <a href="http://microformats.org/wiki/picoformats">Picoformats</a> und jetzt auch <a href="http://www.bioformats.org">Bioformats</a> noch so alles entsteht.