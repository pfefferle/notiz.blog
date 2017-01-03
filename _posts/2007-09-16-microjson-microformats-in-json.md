---
ID: 573
post_title: 'microJSON &#8211; Microformats in JSON'
author: Matthias Pfefferle
post_date: 2007-09-16 12:08:10
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/09/16/microjson-microformats-in-json/
published: true
aktt_tweeted:
  - "1"
---
<a href="http://microjson.org/">microJSON</a> ist ein Projekt von <a href="http://jpsykes.com/">Jon Sykes</a> und <a href="http://jimbarraud.com/">Jim Barraud</a>. Es geht darum, <a href="http://microformats.org">Microformats</a> in Form der <a href="http://www.json.org"><abbr title="JavaScript Object Notation">JSON</abbr></a> Schreibweise darzustellen. Die Idee von JSON ist, einen einfachen Datenaustausch von Objekten oder auch anderen Datenstrukturen wie z.B. Arrays zwischen Client Systemen (z.B. dem WebBrowser) und Server Systemen zu realisieren. Der Vorteil von JSON ist, dass sie kaum Overhead produziert und in JavaScript über die eval() Funktion wieder ganz einfach in ein Objekt gewandelt werden kann.

Beipiel einer hCard:
<pre class="code">&lt;div id=&quot;hcard-given-middle-family&quot; class=&quot;vcard&quot;&gt;
  &lt;span class=&quot;fn n&quot;&gt;
    &lt;span class=&quot;given-name&quot;&gt;given&lt;/span&gt;

    &lt;span class=&quot;additional-name&quot;&gt;middle&lt;/span&gt;
    &lt;span class=&quot;family-name&quot;&gt;family&lt;/span&gt;
  &lt;/span&gt;
  &lt;div class=&quot;org&quot;&gt;org&lt;/div&gt;

  &lt;a class=&quot;email&quot; href=&quot;mailto:email&quot;&gt;email&lt;/a&gt;
  &lt;div class=&quot;adr&quot;&gt;
    &lt;div class=&quot;street-address&quot;&gt;street&lt;/div&gt;

    &lt;span class=&quot;locality&quot;&gt;city&lt;/span&gt;,&lt;span class=&quot;region&quot;&gt;state/province&lt;/span&gt;,&lt;span class=&quot;postal-code&quot;&gt;postal&lt;/span&gt;
    &lt;span class=&quot;country-name&quot;&gt;country&lt;/span&gt;

  &lt;/div&gt;
  &lt;div class=&quot;tel&quot;&gt;phone&lt;/div&gt;
  &lt;a class=&quot;url&quot; href=&quot;aim:goim?screenname=AIM&quot;&gt;AIM&lt;/a&gt;

  &lt;a class=&quot;url&quot; href=&quot;ymsgr:sendIM?YIM&quot;&gt;YIM&lt;/a&gt;
&lt;/div&gt;</pre>

Die gleiche hCard als jCard:
<pre class="code">{
&quot;vcard&quot;:{
  &quot;name&quot;:{
    &quot;given&quot;:&quot;John&quot;,
    &quot;additional&quot;:&quot;Paul&quot;,
    &quot;family&quot;:&quot;Smith&quot;

  },
  &quot;org&quot;:&quot;Company Corp&quot;,
  &quot;email&quot;:&quot;john@companycorp.com&quot;,
  &quot;address&quot;:{
    &quot;street&quot;:&quot;50 Main Street&quot;,
    &quot;locality&quot;:&quot;Cityville&quot;,
    &quot;region&quot;:&quot;Stateshire&quot;,
    &quot;postalCode&quot;:&quot;1234abc&quot;,
    &quot;country&quot;:&quot;Someplace&quot;

  },
  &quot;tel&quot;:&quot;111-222-333&quot;,
  &quot;aim&quot;:&quot;johnsmith&quot;,
  &quot;yim&quot;:&quot;smithjohn&quot;
}</pre>

Neben den Abbildungen der Microformats hCard (<a href="http://microjson.org/wiki/JCard">jCard</a>) und hCalendar (<a href="http://microjson.org/wiki/JCalendar">jCalendar</a>) sind auch die Format jAtom, jResume, jReview, jAtom und jResume geplant. Weitere abbildung gibt es für normale Formulare (<a href="http://microjson.org/wiki/JForm">jForm</a>), sowie auch für RSS Feeds (<a href="http://microjson.org/wiki/JRss">jRSS</a>).

MicroJSON sind meiner Meinung nach eine sehr gute Idee, wenn man Bedenkt dass viele gute Microformats Parser, wie z.B. der vom Firefox Addon <em><a href="http://www.kaply.com/weblog/operator/">Operator</a></em> verwendete <em><a href="http://www.kaply.com/weblog/2007/01/31/parsing-microformats/">ufParser</a></em>, auf JavaScript basiert.