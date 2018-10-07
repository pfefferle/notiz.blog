---
ID: 573
post_title: 'microJSON &#8211; Microformats in JSON'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/09/16/microjson-microformats-in-json/
published: true
post_date: 2007-09-16 12:08:10
---
<!-- wp:paragraph -->
<p><a href="http://microjson.org/">microJSON</a> ist ein Projekt von <a href="http://jpsykes.com/">Jon Sykes</a> und <a href="http://jimbarraud.com/">Jim Barraud</a>. Es geht darum, <a href="http://microformats.org">Microformats</a> in Form der <a href="http://www.json.org"><abbr title="JavaScript Object Notation">JSON</abbr></a> Schreibweise darzustellen. Die Idee von JSON ist, einen einfachen Datenaustausch von Objekten oder auch anderen Datenstrukturen wie z.B. Arrays zwischen Client Systemen (z.B. dem WebBrowser) und Server Systemen zu realisieren. Der Vorteil von JSON ist, dass sie kaum Overhead produziert und in JavaScript über die eval() Funktion wieder ganz einfach in ein Objekt gewandelt werden kann.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Beipiel einer hCard:
</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div id="hcard-given-middle-family" class="vcard">
  &lt;span class="fn n">
    &lt;span class="given-name">given&lt;/span>
    &lt;span class="additional-name">middle&lt;/span>
    &lt;span class="family-name">family&lt;/span>
  &lt;/span>
  &lt;div class="org">org&lt;/div>
  &lt;a class="email" href="mailto:email">email&lt;/a>
  &lt;div class="adr">
    &lt;div class="street-address">street&lt;/div>
    &lt;span class="locality">city&lt;/span>,&lt;span class="region">state/province&lt;/span>,&lt;span class="postal-code">postal&lt;/span>
    &lt;span class="country-name">country&lt;/span>
  &lt;/div>
  &lt;div class="tel">phone&lt;/div>
  &lt;a class="url" href="aim:goim?screenname=AIM">AIM&lt;/a>
  &lt;a class="url" href="ymsgr:sendIM?YIM">YIM&lt;/a>
&lt;/div></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Die gleiche hCard als jCard:
</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>{
"vcard":{
  "name":{
    "given":"John",
    "additional":"Paul",
    "family":"Smith"
  },
  "org":"Company Corp",
  "email":"john@companycorp.com",
  "address":{
    "street":"50 Main Street",
    "locality":"Cityville",
    "region":"Stateshire",
    "postalCode":"1234abc",
    "country":"Someplace"
  },
  "tel":"111-222-333",
  "aim":"johnsmith",
  "yim":"smithjohn"
}</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Neben den Abbildungen der Microformats hCard (<a href="http://microjson.org/wiki/JCard">jCard</a>) und hCalendar (<a href="http://microjson.org/wiki/JCalendar">jCalendar</a>) sind auch die Format jAtom, jResume, jReview, jAtom und jResume geplant. Weitere abbildung gibt es für normale Formulare (<a href="http://microjson.org/wiki/JForm">jForm</a>), sowie auch für RSS Feeds (<a href="http://microjson.org/wiki/JRss">jRSS</a>).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>MicroJSON sind meiner Meinung nach eine sehr gute Idee, wenn man Bedenkt dass viele gute Microformats Parser, wie z.B. der vom Firefox Addon <em><a href="http://www.kaply.com/weblog/operator/">Operator</a></em> verwendete <em><a href="http://www.kaply.com/weblog/2007/01/31/parsing-microformats/">ufParser</a></em>, auf JavaScript basiert.</p>
<!-- /wp:paragraph -->