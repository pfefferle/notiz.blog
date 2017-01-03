---
ID: 3693
post_title: >
  Microdata – wie Microformats bloß
  besser… (Teil 2)
author: Matthias Pfefferle
post_date: 2011-06-26 22:06:32
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2011/06/26/microdata-wie-microformats-blos-besser-teil-2/
published: true
---
<div class="alert alert-info"><a href="http://notiz.blog/2009/08/10/microdata-wie-microformats-bloss-besser-teil-1/">Microdata – wie Microformats bloß besser… (Teil 1)</a>: über abbr-design-pattern, value-class-pattern und Meta-Informationen</div>

Knapp zwei Jahre nach dem ersten Teil, komme ich endlich mal zu Nummer 2 :) Nach den ganzen <a href="http://notiz.blog/2011/06/02/websemantics-google-yahoo-und-bing-einigen-sich-auf-einen-standard/">Diskussionen um schema.org</a> und <a href="http://notiz.blog/2011/06/21/pfefferles-openweb-microformats-v2/">Microformats V2</a> ist es mal wieder an der Zeit, am Image von Microdata zu arbeiten.

<h3>Namenskollisionen und <em>Namespaces</em></h3>

<code>class</code>-Attribute werden in erster Linie zum Gestalten (CSS) und für JS benutzt! Laut "<em><a href="http://www.webdirections.org/sotw10">The State of Web Development 2010</a></em>" setzen nur <a href="http://www.webdirections.org/sotw10/markup/#semantics">knapp 35% aller Befragten</a> Microformats ein, das heißt mehr als 65% haben keine Ahnung von Mikroformaten oder setzten sie nicht ein. Das kann zu zwei Problemen führen:

<ol><li>Microformats werden oft durch Re-Designs zerstört. Facebook ist wohl das prominenteste Beispiel, nach einem Re-Design verschwanden alle Microformats von den Profilseiten.</li>
<li>Es werden fälschlicherweise <code>class</code>-Attribute interpretiert die gar nichts mit Microformats zu tun haben nur zufällig den passenden Namen tragen. Anfällige Klassen sind z.B. <code>url</code> (hCard), <code>photo</code> (hCard), <code>summary</code> (hReview), <code>description</code> (hReview) oder <code>author</code> (hAtom).</li></ol>

Um diesem Problem Herr zu werden denkt <del datetime="2011-06-26T16:57:14+00:00">die Community</del> Tantek Çelik über eine Art <a href="http://microformats.org/wiki/microformats-2#ADVANTAGES"><em>Namespace</em>-Erweiterung</a> nach.

<strong>Microformats</strong>

So könnten Microformtas demnächst folgendermaßen aussehen:

<pre><code>&lt;div class="h-card"&gt;
 &lt;span class="p-fn"&gt;Max Mustermann&lt;/span&gt;
&lt;/div&gt;</code></pre>

Dabei steht:

<ul><li>"h-*" für die <em>root-names</em>, z.B. "h-card", "h-event", "h-entry"</li>
<li>und "p-*" für "simple" (Text) Properties, z.B. "p-fn", "p-summary"</li></ul>

...und es gibt noch eine reihe weiterer <em>Prefixes</em>. Das ist zwar schön und gut und verhindert sicherlich einen Großteil der Namenskollisionen und man kann seinen Entwicklern sicherlich auch eintrichtern, alle <code>x-</code> Klassen in ruhe zu lassen... aber man mach damit jegliche Semantik kaputt. Nix mehr mit <em><a href="http://microformats.org/wiki/posh">Plain Old Semantic HTML</a></em> (POSH):

<blockquote>POSH encapsulates the best practices of using semantic HTML to author web pages. Semantic HTML is the subset of HTML 4.01 (or XHTML 1.0) elements and attributes that are semantic rather than presentational. The best way to learn and understand POSH is to do it.</blockquote>

...und <em><a href="http://www.w3.org/QA/Tips/goodclassnames">semantic class names</a></em>:

<blockquote>Think about why you want something to look a certain way, and not really about how it should look. Looks can always change, but the reasons for giving something a look stay the same. </blockquote>

Außerdem verkompliziert man das, jetzt noch so einfach zu nutzende, Format unnötig. Wann ist etwas eine id (<code>i-*</code>) oder eine Nummer (<code>n-*</code>) und was ist mit Attributen, die sowohl aus auch sein können?

<strong>Microdata</strong>

Der Microdata Teil ist relativ schnell abgehandelt... Durch die Trennung von <em>Semantik</em> und <em>Design</em> kommt es bei Mircodata per se zu keinen Kollisionen:

<pre><code>&lt;div itemtype="http://microformats.org/profile/hcard" itemscope&gt;
 &lt;span itemprop="fn"&gt;Max Mustermann&lt;/span&gt;
&lt;/div&gt;</code></pre>

<h3>Informationen Referenzieren</h3>

Informationen stehen auf Webseiten nicht immer so nahe beieinander, so dass es oftmals schwer ist, alle  Daten mit einem HTML Attribut zu umschließen.

<strong>Microformats</strong>

Je komplizierter das Format oder der Anwendungsfall, desto mehr stößt man mit Microformats an die grenzen des machbaren. HTML 4 bietet keinerlei Mechanismen, den oben angesprochenen Problem zu lösen, deshalb greift die Microformtas-Community zu einer recht Kreativen Lösung: dem <em><a href="http://microformats.org/wiki/include-pattern">include-pattern</a></em>.

<pre><code>&lt;div class="vcard"&gt;
 &lt;a class="include" href="#author-name"&gt;&lt;/a&gt;
&lt;/div&gt;

&lt;span class="fn n" id="author-name"&gt;Max Mustermann&lt;/span&gt;</code></pre>

oder:

<pre><code>&lt;div class="vcard"&gt;
 &lt;object class="include" data="#author-name"&gt;&lt;/object&gt;
&lt;/div&gt;

&lt;span class="fn n" id="author-name"&gt;Max Mustermann&lt;/span&gt;</code></pre>

Nette Idee mit etlichen Unschönheiten:

<ul><li>Leere HTML-Elemente</li>
<li>Zweckentfremdung von Object- bzw. Link-Element</li>
<li>Die Nutzung von <code>&lt;object /&gt;</code> führt zu einigen Problem bei einigen Versionen von Internet Explorer, Safari und Firefox</li></ul>

<strong>Microdata</strong>

Microdata löst das Problem mit dem <code>itemref</code>-Attribut:

<pre><code>&lt;div itemscope
     itemtype="http://microformats.org/profile/hcard"
     itemref="author-name"&gt;
 ...
&lt;/div&gt;

&lt;span itemprop="fn n" id="author-name"&gt;Max Mustermann&lt;/span&gt;</code></pre>

Viel mehr gibt es dazu eigentlich nicht zu sagen :)

<h3>Fazit</h3>

Als Fazit, passt hier sehr gut ein Satz den ich auch als Fazit im aktuellen <a href="http://notiz.blog/2011/06/21/pfefferles-openweb-microformats-v2/">Webstandards-Magazin</a> verwende:

<blockquote>Microformats sind und bleiben Plain Old Semantic HTML und man sollte auch in Zukunft keinesfalls darauf verzichten sie einzusetzen, selbst mit dem Risiko einer fehlerhaften Implementierungen oder Namenskollisionen, „erzieht“ die Nutzung von Microformats einen jeden Webentwickler dazu „schönen“ und „sprechenden“ HTML-Code zu schreiben.</blockquote>

...um HTML-Code aber wirklich maschinenlesbar zu machen, wird es Zeit auf Microdata und RDFa zu setzen. Microformats haben den Weg für bessere und native Lösungen geebnet und haben weiterhin ihre Daseinsberechtigung aber man sollte nicht mehr als dem Format machen, als es leisten kann.