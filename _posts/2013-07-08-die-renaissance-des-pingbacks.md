---
ID: 5307
post_title: Die Renaissance des Pingbacks
author: Matthias Pfefferle
post_date: 2013-07-08 13:04:38
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2013/07/08/die-renaissance-des-pingbacks/
published: true
---
<a href="http://www.hixie.ch/specs/pingback/pingback">Pingbacks</a> (und Trackbacks) werden zwar immer noch von allen WordPress Blogs unterstützt aber mal ehrlich... wen interessieren sie denn noch wirklich? Das hängt hauptsächlich mit der etwas veralteten Spezifikation zusammen, in der folgendes vorgeschlagen wird:

<blockquote>Bob's blog also retrieves other data required from the content of Alice's new post, such as the page title, an extract of the page content surrounding the link to Bob's post, any attributes indicating which language the page is in, and so forth.</blockquote>

Das führt bei WordPress zu Einträgen die ungefähr so aussehen:

<blockquote>[...] und Wertvorstellungen entspricht und nicht von der Mehrheit meiner Freunde abhängig sein.» Dezentrale Walled Gardens Hier erscheinen von Montag bis Freitag ausgewählte Links zu lesenswerten Texten und aktuellen [...]</blockquote>

Der automatische generierte Ausschnitt lässt nicht wirklich erahnen was Markus Spath <a href="http://netzwertig.com/2012/11/22/linkwertig-wi-apps-privacy-aufklaerung/">wirklich geschrieben hat</a> und deshalb verüble ich es niemandem, wenn er die Pingbacks/Trackbacks auf seiner Seite auf eine simple Liste von Links beschränkt hat. Als die Spezifikation 2002 geschrieben wurde, war das mit dem "Ausschnitt um den Link" sicherlich eine gute Lösung. Es gab keine andere Möglichkeit automatisch zu erkennen welcher Text genau zu dem Link gehört oder wann ein neuer Artikel, die Navigation oder sogar Werbung beginnt. Mittlerweile lassen sich Inhalte dank Websemantiken wie <a href="http://notiz.blog/tag/microformats">Microformats</a>, <a href="http://notiz.blog/tag/rdfa">RDFa</a> oder <a href="http://notiz.blog/tag/microdata">Microdata</a> sehr gut erkennen. Aber auch mit purem HTML5 Markup lässt sich problemlos ein &lt;article /&gt; und dessen Überschrift erkennen.

Pingbacks sind aktuell die einfachste und wahrscheinlich sogar die einzige Möglichkeit, Kommentare dezentral und vor allem Plattform unabhängig zu "verschicken", deshalb verstehe ich nicht wieso es so lange gedauert hat, bis jemand (im Rahmen eines <a href="http://indiewebcamp.com/pingback">IndieWebCamps</a>) auf die Idee kam sie den aktuellen Bedürfnissen und Möglichkeiten anzupassen anstatt sich weiter den Kopf über komplizierte dezentrale Protokolle zu zermartern. Wer sich das <a href="http://www.salmon-protocol.org/">Salmon Protocol</a> schon einmal angeschaut hat, weiß was ich meine...

Pingbacks haben diverse Vorzüge:

<ul>
<li>Sie sind leicht zu implementieren (einfacher XML-RPC Request an jedem, im Text erwähnte URL)</li>
<li>Sie bieten einen simplen Schutz (wenn auch keinen 100%igen) gegen Spam, da der Pingende zumindest für eine gewisse Zeit auf die ge-pingte Seite verlinken muss</li>
<li><abbr title="don't repeat yourself">DRY</abbr>... Die Webseite dient als API und man muss seine Texte nicht zusätzlich in diversen XML oder JSON Formaten anbieten</li>
</ul>

Auf der IndieWebCamp Seite gibt es eine Reihe an <a href="http://indiewebcamp.com/comments">interessanten Diskussionen</a> wie sich mit Hilfe von Microformats und ein paar <a href="http://indiewebcamp.com/responses"><code>rel</code>-Attributen</a> auch "Likes" oder "RSVPs" über Pingbacks realisieren ließen.

Ein Like könnte beispielsweise folgendermaßen aussehen:

<pre><code>&lt;div class="h-entry"&gt;&lt;span class="p-autor h-card"&gt;Matthias Pfefferle&lt;/span&gt; likes &lt;a rel="<strong>object-of-like</strong>" href="http://hackr.de"&gt;hackr.de&lt;/a&gt;&lt;/div&gt;
</code></pre>

Sandeep Shetty hat das auf <a href="http://www.sandeep.io/">sandeep.io</a> sehr schön <a href="http://www.sandeep.io/39" class="u-mention">erklärt</a> und <a href="http://www.sandeep.io/39#likes">implementiert</a>!

<a href="http://werd.io/view/51cce999bed7de1e06ae3840" class="u-like u-object-of-like">Ben Werdmuller</a> hat außerdem nochmal alles (Comments/Likes/RSVPs) als Video zusammengefasst:

http://www.youtube.com/watch?v=zgvQq8o8RxU

Im nächsten Blogpost geht es dann um <a href="http://webmention.org/">Webmentions</a>, einer etwas moderneren Variante von Pingbacks.