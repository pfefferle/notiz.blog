---
ID: 4459
post_title: >
  I’ve made a WordPress Theme… kind
  of…
author: Matthias Pfefferle
post_date: 2012-09-06 22:54:53
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2012/09/06/ive-made-a-wordpress-theme-kind-of/
published: true
---
Eigentlich wollte ich ja nur einen <a href="http://wordpress.org/extend/themes/toolbox">Toolbox</a> Fork erstellen und das Theme um Microdata/Schema.org erweitern und dann hat es doch so viel Spaß gemacht, dass ein eigenes Theme daraus wurde... Ich präsentiere euch <a href="https://github.com/pfefferle/SemPress">SemPress</a>, das hoch semantische HTML5 Theme mit ner Prise Responsiveness und <abbr title="Search Engine Optimization">SEO</abbr> :)

Das Theme verschönert übrigens das <a href="http://notiz.blog/">notizBlog</a> und ist aus folgenden Gründen großartig:

<h2 id="websemantics">POSH - Plain Old Semantic HTML5</h2>

<img src="http://notiz.blog/wp-content/uploads/2011/07/HTML5_Logo_256.png" alt="HTML5 Logo" title="HTML5 Logo" width="256" height="256" class="alignright size-full wp-image-3841" />SemPress basiert, wie schon erwähnt, auf Toolbox und die HTML5 Struktur wurde auch weitestgehend beibehalten. Ich habe lediglich einige Tags in (meiner Meinung nach) semantisch passendere getauscht. Im Detail:

<ul>
<li><strong><a href="http://diveintohtml5.info/semantics.html#new-elements">Semantische Tags</a></strong> - Ich habe einfach mal geschaut welche Tags Toolbox noch nicht unterstützt und sie dann, hoffentlich richtig eingebaut :).</li>
<li><strong><a href="http://diveintohtml5.info/forms.html">HTML5 Input-Types</a></strong> - SemPress unterstützt einige der neuen Input-Types wie z.B. "search", "email" und "url". Mehr dazu in einem älteren <a href="http://notiz.blog/2011/07/11/html5-input-types-form-validierung-und-wordpress/">Artikel</a>.</li>
</ul>

<h2>Websemantics</h2>

Eigentlich hab ich das ganze Projekt (wie schon erwähnt) ja nur gestartet, damit ich mal wieder was produktives mit Microformats machen und Schema.org lernen kann. Hier also der <em>Semantic Overload</em>:

<ul>
<li><strong>Microformats</strong> - Toolbox selbst unterstütz Microformats ja schon von Haus aus und ich musste nur kleine hAtom fixes und die richtigen <em><a href="http://microformats.org/wiki/rel-profile">Profile Header</a></em> setzen.</li>
<li><strong>Microformats v2</strong> - Ich bin zwar <a href="http://notiz.blog/2012/07/03/microformats-the-next-generation/">kein großer Fan</a> von <a href="http://microformats.org/wiki/microformats_2">Microformats 2</a>, aber ich wollte testen wie leicht sich das Theme um neues HTML-Classes erweitern lässt und wie viel Arbeit es bedeutet. SemPress unterstützt hCard 2 und hAtom 2.</li>
<li><strong>Microdata/Schema.org</strong> - Ähnlich wie bei Microformats v2 wollte ich testen wie schwer es ist, <a href="http://schema.org/">Schema.org</a> einzubauen. Das Theme unterstützt http://schema.org/Blog, http://schema.org/BlogPosting and http://schema.org/Person.</li>
</ul>

Was ich noch gerne einbauen will ist hMedia für alle möglichen Medieninhalte wie z.B. auch WordPress "Images" und "Galleries" und natürlich auch das Schema.org Pendant.

<h2>WordPress Features</h2>

<img src="http://notiz.blog/wp-content/uploads/2007/03/wordpress-logo.png" alt="" title="WordPress Logo" width="150" height="150" class="alignright size-full wp-image-1748" />Neben dem ganzen semantik Gedöns, hab ich natürlich auch ne Menge WordPress-Features eingebaut.

<ul>
<li><strong>Post Thumbnails</strong> - SemPress unterstützt diverse <em><a href="http://codex.wordpress.org/Post_Thumbnails">Post-Thumbnail</a></em> Größen (maximal 600px) und versucht sie bestmöglich darzustellen. Alle Bilder kleiner als 480px werden z.B. mit <em>float right</em> in den Text integriert.</li>
<li><strong>Post Types</strong> - Im Gegensatz zu Toolbox unterstützt SemPress folgende <em><a href="https://codex.wordpress.org/Post_Types">Post-Types</a></em>: "aside, status, gallery, video, audio, link, image" und fast alle haben auch ein individuelles Layout spendiert bekommen.</li>
<li>...außerdem: <a href="http://codex.wordpress.org/Translating_WordPress">Localization</a>, Sidebar-Widgets und die WordPress' Navigation Menu.</li>
</ul>

Mal schauen ob ich noch ein <a href="http://en.support.wordpress.com/themes/custom-header-image/">Custom-Header-Image</a> mit rein nehmen werde...

<h2>CSS und Design</h2>

Zuerst sollte SemPress gar kein Design bekommen, aber man muss ja auch bei CSS und Fonts auf dem Laufenden bleiben! Ich mach das ja schließlich nicht zum Spaß sondern zur Fortbildung :). Da ich aber kein wirklich großer Designer bin, hab ich mir ne Menge Ideen und CSS bei folgenden großartigen Projekten ausgeliehen:

<ul>
<li>Das Basis-CSS hab' ich von <a href="http://wordpress.org/extend/themes/toolbox">Toolbox</a> übernommen.</li>
<li>Die Tabellen, Buttons, Input-Felder, Code-Boxen habe ich mir bei <em><a href="http://twitter.github.com/bootstrap/">Twitters Bootstrap</a></em> gemopst.</li>
<li>Die Icons, die vor einigen Artikeln erscheinen (z.B. die vom Typ Video oder Audio) sind von von <a href="http://fortawesome.github.com/Font-Awesome/">Font Awesome</a>.</li>
<li>Danke auch an <a href="http://html5boilerplate.com/">HTML5 Boilerplate</a> für einige Ideen!</li>
</ul>

Ein paar weitere Kleinigkeiten (auf die ich auch bissle Stolz bin):

<ul>
<li>Man kann den bei dem &lt;code /&gt;-Tag die Programmiersprache mir <code>data-programming-language="PHP"</code> setzen und es wird wie folgend angezeigt:
<pre><code data-programming-language="PHP">&lt;?php echo "Hallo Welt"; ?&gt;</code></pre></li>
<li>Das Theme kommt komplett ohne Bilder aus.</li>
</ul>

<h2>Responsive Design</h2>

Das Theme sollte eigentlich und hoffentlich auf jedem Gerät gut aussehen und unterstützt drei++ Breiten:

<ul>
<li>Volle Breite + Sidebar rechts</li>
<li>Volle Breite + Zweispaltige Sidebar am Ende der Seite</li>
<li>Variable Breite (die, für das Gerät beste Breite mit einem) + Einspaltige Sidebar am Ende der Seite.</li>
</ul>

Außerdem passt sich das Menü automatisch an die Größen an und das ganz ohne JavaScript! ...beim Drop-Down Menü gibt es zwar noch keine Möglichkeit das Menü wieder zu schließen, aber wer will das schon ;)

<h2>Was jetzt noch?</h2>

Da mir das themen ne Menge Spaß gemacht hat werde ich wohl auch weiterhin fleißig an SemPress weiter basteln und es noch semantischer und WordPressiger machen. Falls ihr irgendwelche Fehler findet oder Dinge besser könnt wie ich... bitte helft mir und <a href="https://github.com/pfefferle/SemPress">forkt SemPress</a>!