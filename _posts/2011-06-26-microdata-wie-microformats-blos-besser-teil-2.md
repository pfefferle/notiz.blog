---
ID: 3693
post_title: >
  Microdata – wie Microformats bloß
  besser… (Teil 2)
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2011/06/26/microdata-wie-microformats-blos-besser-teil-2/
published: true
post_date: 2011-06-26 22:06:32
---
<!-- wp:paragraph -->
<p><strong><a href="https://notiz.blog/2009/08/10/microdata-wie-microformats-bloss-besser-teil-1/">Microdata – wie Microformats bloß besser… (Teil 1)</a>: über abbr-design-pattern, value-class-pattern und Meta-Informationen</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Knapp zwei Jahre nach dem ersten Teil, komme ich endlich mal zu Nummer 2 :) Nach den ganzen <a href="https://notiz.blog/2011/06/02/websemantics-google-yahoo-und-bing-einigen-sich-auf-einen-standard/">Diskussionen um schema.org</a> und <a href="https://notiz.blog/2011/06/21/pfefferles-openweb-microformats-v2/">Microformats V2</a> ist es mal wieder an der Zeit, am Image von Microdata zu arbeiten.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h3>Namenskollisionen und <em>Namespaces</em></h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p><code>class</code>-Attribute werden in erster Linie zum Gestalten (CSS) und für JS benutzt! Laut &quot;<em><a href="http://www.webdirections.org/sotw10">The State of Web Development 2010</a></em>&quot; setzen nur <a href="http://www.webdirections.org/sotw10/markup/#semantics">knapp 35% aller Befragten</a> Microformats ein, das heißt mehr als 65% haben keine Ahnung von Mikroformaten oder setzten sie nicht ein. Das kann zu zwei Problemen führen:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ol>
    <li>Microformats werden oft durch Re-Designs zerstört. Facebook ist wohl das prominenteste Beispiel, nach einem Re-Design verschwanden alle Microformats von den Profilseiten.</li>
    <li>Es werden fälschlicherweise <code>class</code>-Attribute interpretiert die gar nichts mit Microformats zu tun haben nur zufällig den passenden Namen tragen. Anfällige Klassen sind z.B. <code>url</code> (hCard), <code>photo</code> (hCard), <code>summary</code> (hReview), <code>description</code> (hReview) oder <code>author</code> (hAtom).</li>
</ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Um diesem Problem Herr zu werden denkt <del>die Community</del> Tantek Çelik über eine Art <a href="http://microformats.org/wiki/microformats-2#ADVANTAGES"><em>Namespace</em>-Erweiterung</a> nach.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Microformats</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>So könnten Microformtas demnächst folgendermaßen aussehen:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class=&quot;h-card&quot;&gt;
 &lt;span class=&quot;p-fn&quot;&gt;Max Mustermann&lt;/span&gt;
&lt;/div&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Dabei steht:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li>&quot;h-*&quot; für die <em>root-names</em>, z.B. &quot;h-card&quot;, &quot;h-event&quot;, &quot;h-entry&quot;</li>
    <li>und &quot;p-*&quot; für &quot;simple&quot; (Text) Properties, z.B. &quot;p-fn&quot;, &quot;p-summary&quot;</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>...und es gibt noch eine reihe weiterer <em>Prefixes</em>. Das ist zwar schön und gut und verhindert sicherlich einen Großteil der Namenskollisionen und man kann seinen Entwicklern sicherlich auch eintrichtern, alle <code>x-</code> Klassen in ruhe zu lassen... aber man mach damit jegliche Semantik kaputt. Nix mehr mit <em><a href="http://microformats.org/wiki/posh">Plain Old Semantic HTML</a></em> (POSH):</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
    <p>POSH encapsulates the best practices of using semantic HTML to author web pages. Semantic HTML is the subset of HTML 4.01 (or XHTML 1.0) elements and attributes that are semantic rather than presentational. The best way to learn and understand POSH is to do it.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>...und <em><a href="http://www.w3.org/QA/Tips/goodclassnames">semantic class names</a></em>:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
    <p>Think about why you want something to look a certain way, and not really about how it should look. Looks can always change, but the reasons for giving something a look stay the same.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Außerdem verkompliziert man das, jetzt noch so einfach zu nutzende, Format unnötig. Wann ist etwas eine id (<code>i-*</code>) oder eine Nummer (<code>n-*</code>) und was ist mit Attributen, die sowohl aus auch sein können?</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Microdata</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Der Microdata Teil ist relativ schnell abgehandelt... Durch die Trennung von <em>Semantik</em> und <em>Design</em> kommt es bei Mircodata per se zu keinen Kollisionen:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div itemtype=&quot;http://microformats.org/profile/hcard&quot; itemscope&gt;
 &lt;span itemprop=&quot;fn&quot;&gt;Max Mustermann&lt;/span&gt;
&lt;/div&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:heading -->
<h3>Informationen Referenzieren</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Informationen stehen auf Webseiten nicht immer so nahe beieinander, so dass es oftmals schwer ist, alle Daten mit einem HTML Attribut zu umschließen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Microformats</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Je komplizierter das Format oder der Anwendungsfall, desto mehr stößt man mit Microformats an die grenzen des machbaren. HTML 4 bietet keinerlei Mechanismen, den oben angesprochenen Problem zu lösen, deshalb greift die Microformtas-Community zu einer recht Kreativen Lösung: dem <em><a href="http://microformats.org/wiki/include-pattern">include-pattern</a></em>.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class=&quot;vcard&quot;&gt;
 &lt;a class=&quot;include&quot; href=&quot;#author-name&quot;&gt;&lt;/a&gt;
&lt;/div&gt;

&lt;span class=&quot;fn n&quot; id=&quot;author-name&quot;&gt;Max Mustermann&lt;/span&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>oder:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div class=&quot;vcard&quot;&gt;
 &lt;object class=&quot;include&quot; data=&quot;#author-name&quot;&gt;&lt;/object&gt;
&lt;/div&gt;

&lt;span class=&quot;fn n&quot; id=&quot;author-name&quot;&gt;Max Mustermann&lt;/span&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Nette Idee mit etlichen Unschönheiten:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li>Leere HTML-Elemente</li>
    <li>Zweckentfremdung von Object- bzw. Link-Element</li>
    <li>Die Nutzung von <code>&lt;object /&gt;</code> führt zu einigen Problem bei einigen Versionen von Internet Explorer, Safari und Firefox</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p><strong>Microdata</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Microdata löst das Problem mit dem <code>itemref</code>-Attribut:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;div itemscope
     itemtype=&quot;http://microformats.org/profile/hcard&quot;
     itemref=&quot;author-name&quot;&gt;
 ...
&lt;/div&gt;

&lt;span itemprop=&quot;fn n&quot; id=&quot;author-name&quot;&gt;Max Mustermann&lt;/span&gt;</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Viel mehr gibt es dazu eigentlich nicht zu sagen :)</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h3>Fazit</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Als Fazit, passt hier sehr gut ein Satz den ich auch als Fazit im aktuellen <a href="https://notiz.blog/2011/06/21/pfefferles-openweb-microformats-v2/">Webstandards-Magazin</a> verwende:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
    <p>Microformats sind und bleiben Plain Old Semantic HTML und man sollte auch in Zukunft keinesfalls darauf verzichten sie einzusetzen, selbst mit dem Risiko einer fehlerhaften Implementierungen oder Namenskollisionen, „erzieht“ die Nutzung von Microformats einen jeden Webentwickler dazu „schönen“ und „sprechenden“ HTML-Code zu schreiben.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>...um HTML-Code aber wirklich maschinenlesbar zu machen, wird es Zeit auf Microdata und RDFa zu setzen. Microformats haben den Weg für bessere und native Lösungen geebnet und haben weiterhin ihre Daseinsberechtigung aber man sollte nicht mehr als dem Format machen, als es leisten kann.</p>
<!-- /wp:paragraph -->