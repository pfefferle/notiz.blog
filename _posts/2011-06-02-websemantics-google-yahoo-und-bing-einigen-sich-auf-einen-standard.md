---
ID: 3717
post_title: 'Websemantics: Google, Yahoo! und Bing einigen sich auf einen &#8222;Standard&#8220;'
author: Matthias Pfefferle
post_date: 2011-06-02 23:28:49
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2011/06/02/websemantics-google-yahoo-und-bing-einigen-sich-auf-einen-standard/
published: true
---
Google, Yahoo! und Bing haben heute <a href="http://insidesearch.blogspot.com/2011/06/introducing-schemaorg-search-engines.html">angekündigt</a>, dass sie beim Thema <em>Websemantics</em> zukünftig zusammen arbeiten werden und sich auf einen gemeinsamen Standard einigen wollen (wie vorher auch bei den <a href="http://www.sitemaps.org/">Sitemaps</a>, <a href="http://www.robotstxt.org/">robots.txt</a>, um.).

Auf <a href="http://schema.org/">schema.org</a> findet man eine Übersicht alle Schemas die die Suchgiganten in Zukunft unterstützen werden:

<blockquote>This site provides a collection of schemas, i.e., html tags, that webmasters can use to markup their pages in ways recognized by major search providers. Search engines including Bing, Google and Yahoo! rely on this markup to improve the display of search results, making it easier for people to find the right web pages.</blockquote>

Was mich besonders freut: Die Schemas basieren alle auf Microdata und wer meinen Blog regelmäßig verfolgt wird wissen, dass ich <a href="http://notiz.blog/tag/microdata/">das Format sehr schätze</a>! Hier ein Beispiel wie eine Person mit dem neuen Schema aussieht:

<pre><code>&lt;div itemscope itemtype="http://schema.org/Person"&gt;
  &lt;span itemprop="name"&gt;Jane Doe&lt;/span&gt;
  &lt;img src="janedoe.jpg" itemprop="image" /&gt;
&lt;/div&gt;</code></pre>

Soweit so gut, aber... es werden <strong>WIEDER</strong> einmal weder bestehende Microformats, noch RDFa Schemas auf Microdata portiert, was dazu führt dass mir spontan 5 unterschiedliche Formate einfallen um Personen zu beschreiben: <a href="http://microformats.org/wiki/hcard">hCard</a> (Microformats), <a href="http://www.data-vocabulary.org/Person/">Data-Vocabulary</a> (RDFa- und Microdata-Beschreibung genutzt von den rich-snippets), <a href="http://www.foaf-project.org/">FoaF</a> (RDFa), <a href="http://www.w3.org/Submission/vcard-rdf/">vCard</a> (RDFa), <a href="http://schema.org/Person">schema.org</a> (Microdata).

Die Microformats-Community hat von Anfang an eines richtig gemacht: Es gibt nur <a href="http://microformats.org/wiki/Main_Page">eine Stelle an der Microformats definiert werden</a> und man muss einen relativ langwierigen Prozess befolgen um ein neues Format zu definieren. Das führt zwar dazu dass es bisher nur eine handvoll Schemas veröffentlicht wurden, diese aber wohl definiert sind und in der Regel auf bisherigen Formaten aufbauen. Die <a href="http://microformats.org/wiki/hCard">hCard</a> ist beispielsweise ein 1:1 Abbild der <a href="http://www.ietf.org/rfc/rfc2426.txt">vCard</a>.

Schema.org ist zwar eine ganz nette Idee aber man hat leider versäumt sich mit der Microformats-, RDFa-, RDF- Community zusammenzusetzen und einen gemeinsamen Konsens zu finden!

Wäre folgendes Beispiel so viel komplizierter?

<pre><code>&lt;div itemscope itemtype="http://microformats.org/profile/hcard"&gt;
  &lt;span itemprop="fn"&gt;Jane Doe&lt;/span&gt;
  &lt;img src="janedoe.jpg" itemprop="photo" /&gt;
&lt;/div&gt;</code></pre>

...oder das?

<pre><code>&lt;div itemscope itemtype="http://www.w3.org/2006/vcard/ns"&gt;
  &lt;span itemprop="fn"&gt;Jane Doe&lt;/span&gt;
  &lt;img src="janedoe.jpg" itemprop="photo" /&gt;
&lt;/div&gt;</code></pre>

Das Format ist letztendlich Geschmackssache... der eine mag lieber die einfachen Microformats, der andere steht mehr auf RDFa und ich bevorzuge Microdata, man sollte sich aber endlich auf ein einheitliches Schema einigen!

Yahoo! zählt knapp zwei Milliarden hCards in ihrem Index und trotzdem diktiert man Webseitenbetreibern etwas komplett anderes auf...