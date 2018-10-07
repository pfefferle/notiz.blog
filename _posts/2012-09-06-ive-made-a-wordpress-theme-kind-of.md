---
ID: 4459
post_title: >
  I’ve made a WordPress Theme… kind
  of…
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2012/09/06/ive-made-a-wordpress-theme-kind-of/
published: true
post_date: 2012-09-06 22:54:53
---
<!-- wp:paragraph -->
<p>Eigentlich wollte ich ja nur einen <a href="http://wordpress.org/extend/themes/toolbox">Toolbox</a> Fork erstellen und das Theme um Microdata/Schema.org erweitern und dann hat es doch so viel Spaß gemacht, dass ein eigenes Theme daraus wurde... Ich präsentiere euch <a href="https://github.com/pfefferle/SemPress">SemPress</a>, das hoch semantische HTML5 Theme mit ner Prise Responsiveness und <abbr title="Search Engine Optimization">SEO</abbr> :)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Das Theme verschönert übrigens das <a href="https://notiz.blog/">notizBlog</a> und ist aus folgenden Gründen großartig:</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>POSH - Plain Old Semantic HTML5</h2>
<!-- /wp:heading -->

<!-- wp:image {"align":"right"} -->
<figure class="wp-block-image alignright" style="max-width:50%"><img src="https://notiz.blog/wp-content/uploads/2011/07/HTML5_Logo_256.png" alt="HTML5 Logo" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>SemPress basiert, wie schon erwähnt, auf Toolbox und die HTML5 Struktur wurde auch weitestgehend beibehalten. Ich habe lediglich einige Tags in (meiner Meinung nach) semantisch passendere getauscht. Im Detail:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li><strong><a href="http://diveintohtml5.info/semantics.html#new-elements">Semantische Tags</a></strong> - Ich habe einfach mal geschaut welche Tags Toolbox noch nicht unterstützt und sie dann, hoffentlich richtig eingebaut :).</li>
    <li><strong><a href="http://diveintohtml5.info/forms.html">HTML5 Input-Types</a></strong> - SemPress unterstützt einige der neuen Input-Types wie z.B. &quot;search&quot;, &quot;email&quot; und &quot;url&quot;. Mehr dazu in einem älteren <a href="https://notiz.blog/2011/07/11/html5-input-types-form-validierung-und-wordpress/">Artikel</a>.</li>
</ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2>Websemantics</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Eigentlich hab ich das ganze Projekt (wie schon erwähnt) ja nur gestartet, damit ich mal wieder was produktives mit Microformats machen und Schema.org lernen kann. Hier also der <em>Semantic Overload</em>:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li><strong>Microformats</strong> - Toolbox selbst unterstütz Microformats ja schon von Haus aus und ich musste nur kleine hAtom fixes und die richtigen <em><a href="http://microformats.org/wiki/rel-profile">Profile Header</a></em> setzen.</li>
    <li><strong>Microformats v2</strong> - Ich bin zwar <a href="https://notiz.blog/2012/07/03/microformats-the-next-generation/">kein großer Fan</a> von <a href="http://microformats.org/wiki/microformats_2">Microformats 2</a>, aber ich wollte testen wie leicht sich das Theme um neues HTML-Classes erweitern lässt und wie viel Arbeit es bedeutet. SemPress unterstützt hCard 2 und hAtom 2.</li>
    <li><strong>Microdata/Schema.org</strong> - Ähnlich wie bei Microformats v2 wollte ich testen wie schwer es ist, <a href="http://schema.org/">Schema.org</a> einzubauen. Das Theme unterstützt http://schema.org/Blog, http://schema.org/BlogPosting and http://schema.org/Person.</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Was ich noch gerne einbauen will ist hMedia für alle möglichen Medieninhalte wie z.B. auch WordPress &quot;Images&quot; und &quot;Galleries&quot; und natürlich auch das Schema.org Pendant.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>WordPress Features</h2>
<!-- /wp:heading -->

<!-- wp:image {"align":"right"} -->
<figure class="wp-block-image alignright" style="max-width:50%"><img src="https://notiz.blog/wp-content/uploads/2007/03/wordpress-logo.png" alt="" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Neben dem ganzen semantik Gedöns, hab ich natürlich auch ne Menge WordPress-Features eingebaut.</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li><strong>Post Thumbnails</strong> - SemPress unterstützt diverse <em><a href="http://codex.wordpress.org/Post_Thumbnails">Post-Thumbnail</a></em> Größen (maximal 600px) und versucht sie bestmöglich darzustellen. Alle Bilder kleiner als 480px werden z.B. mit <em>float right</em> in den Text integriert.</li>
    <li><strong>Post Types</strong> - Im Gegensatz zu Toolbox unterstützt SemPress folgende <em><a href="https://codex.wordpress.org/Post_Types">Post-Types</a></em>: &quot;aside, status, gallery, video, audio, link, image&quot; und fast alle haben auch ein individuelles Layout spendiert bekommen.</li>
    <li>...außerdem: <a href="http://codex.wordpress.org/Translating_WordPress">Localization</a>, Sidebar-Widgets und die WordPress&#x27; Navigation Menu.</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Mal schauen ob ich noch ein <a href="http://en.support.wordpress.com/themes/custom-header-image/">Custom-Header-Image</a> mit rein nehmen werde...</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>CSS und Design</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Zuerst sollte SemPress gar kein Design bekommen, aber man muss ja auch bei CSS und Fonts auf dem Laufenden bleiben! Ich mach das ja schließlich nicht zum Spaß sondern zur Fortbildung :). Da ich aber kein wirklich großer Designer bin, hab ich mir ne Menge Ideen und CSS bei folgenden großartigen Projekten ausgeliehen:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li>Das Basis-CSS hab&#x27; ich von <a href="http://wordpress.org/extend/themes/toolbox">Toolbox</a> übernommen.</li>
    <li>Die Tabellen, Buttons, Input-Felder, Code-Boxen habe ich mir bei <em><a href="http://twitter.github.com/bootstrap/">Twitters Bootstrap</a></em> gemopst.</li>
    <li>Die Icons, die vor einigen Artikeln erscheinen (z.B. die vom Typ Video oder Audio) sind von von <a href="http://fortawesome.github.com/Font-Awesome/">Font Awesome</a>.</li>
    <li>Danke auch an <a href="http://html5boilerplate.com/">HTML5 Boilerplate</a> für einige Ideen!</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Ein paar weitere Kleinigkeiten (auf die ich auch bissle Stolz bin):</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li>Man kann den bei dem &lt;code /&gt;-Tag die Programmiersprache mir <code>data-programming-language=&quot;PHP&quot;</code> setzen und es wird wie folgend angezeigt:
        <code>&lt;?php echo &quot;Hallo Welt&quot;; ?&gt;</code>
    </li>
    <li>Das Theme kommt komplett ohne Bilder aus.</li>
</ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2>Responsive Design</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Das Theme sollte eigentlich und hoffentlich auf jedem Gerät gut aussehen und unterstützt drei++ Breiten:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
    <li>Volle Breite + Sidebar rechts</li>
    <li>Volle Breite + Zweispaltige Sidebar am Ende der Seite</li>
    <li>Variable Breite (die, für das Gerät beste Breite mit einem) + Einspaltige Sidebar am Ende der Seite.</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Außerdem passt sich das Menü automatisch an die Größen an und das ganz ohne JavaScript! ...beim Drop-Down Menü gibt es zwar noch keine Möglichkeit das Menü wieder zu schließen, aber wer will das schon ;)</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Was jetzt noch?</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Da mir das themen ne Menge Spaß gemacht hat werde ich wohl auch weiterhin fleißig an SemPress weiter basteln und es noch semantischer und WordPressiger machen. Falls ihr irgendwelche Fehler findet oder Dinge besser könnt wie ich... bitte helft mir und <a href="https://github.com/pfefferle/SemPress">forkt SemPress</a>!</p>
<!-- /wp:paragraph -->