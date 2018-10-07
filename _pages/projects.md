---
ID: 320
post_title: Projekte
author: Matthias Pfefferle
post_excerpt: ""
layout: page
permalink: https://notiz.blog/projects/
published: true
post_date: 2007-03-06 19:20:28
---
Inhalt: <a href="#openweb-icons">OpenWeb Icons</a>, <a href="#wordpress-plugins">WordPress Plugins</a>, <a href="#wordpress-themes">WordPress Themes</a>, <a href="#microformats">Microformats</a>, <a href="#podcast">OpenWeb Podcast</a>, <a href="#twelvethings">12things</a>

<hr />

<h2 id="openweb-icons">OpenWeb Icons - <small>A font!</small></h2>

<img src="//notiz.blog/wp-content/uploads/2012/05/OpenWeb-Icons.jpg" alt="OpenWeb Icons (a font)" title="OpenWeb Icons (a font)" width="484" height="323" class="alignright size-full wp-image-4242" /><em><a href="http://pfefferle.github.com/openwebicons/">OpenWeb Icons</a></em> ist ein Font mit Icons/Logos von Web-Standards, offenen Formaten oder von Organisation / Initiativen für ein besseres und freies Web.

Warum ein <em>OpenWeb Icons</em> - Font? Weil Font Awesome kein RSS-icon hatte und es etwas langweilig wäre einen Font mit nur einem Icon zu bauen ;)

...außerdem kann ich nur "Open Web"!

<strong>Also zeigt euren Support und nutzt den Font!</strong>

Der Font beinhaltet unter anderem Folgende Icons:

<ul><li>RSS/ATOM</li>
<li>OpenID</li>
<li>OAuth</li>
<li>Federated Social Web</li>
<li>Creative Commons</li></ul>

uvm...

Ich würde mich übrigens sehr über jegliche Hilfe freuen: <a href="https://github.com/pfefferle/openwebicons">https://github.com/pfefferle/openwebicons</a>

<hr />

<h2 id="wordpress-plugins">WordPress Plugins</h2>

<img src="https://notiz.blog/wp-content/uploads/2007/03/wordpress-logo.png" alt="WordPress Logo" title="WordPress Logo" width="150" height="150" class="alignright size-full" />Ich liebe die Open/Federated-Web-Idee und ich liebe WordPress... und daraus entstanden über die Jahre ein paar Plugins. Falls ihr Lust habt mir bei einem der Plugins unter die Arme zu greifen, dann lasst es mich bitte wissen. Ich bin dankbar für jede Hilfe!

Hier eine kleine Auswahl an Plugins:
<ul>
<li><a href="http://wordpress.org/plugins/indieweb/">IndieWeb for WordPress</a></li>
<li><a href="http://wordpress.org/plugins/ostatus-for-wordpress/">OStatus for WordPress</a></li>
<li><a href="http://wordpress.org/plugins/oexchange/">OExchange</a></li>
<li><a href="http://wordpress.org/plugins/webmention/">Webmention</a></li>
<li><a href="http://wordpress.org/plugins/pubsubhubbub/">WebSub/PubSubHubbub</a></li>
<li><a href="http://wordpress.org/plugins/webfinger/">WebFinger</a></li>
<li><a href="http://wordpress.org/plugins/activitystream-extension/">ActivityStream extension</a></li>
<li><a href="http://wordpress.org/plugins/host-meta/">host-meta</a></li>
<li><a href="http://wordpress.org/plugins/open-search-document/">Open Search Document</a></li>
<li><a href="https://notiz.blog/projects/wp-hcard-commenting/">hCard Commenting</a></li>
<li><a href="https://notiz.blog/projects/apml-for-wordpress/">APML Support für WordPress</a></li>
</ul>

Weitere auf <a href="https://profiles.wordpress.org/pfefferle">WordPress.org</a> oder <a href="https://github.com/search?utf8=✓&q=topic%3Awordpress+user%3Apfefferle+org%3Aindieweb+org%3Aapml+org%3Adiso&type=Repositories">Github</a>.

<h2 id="wordpress-themes">WordPress Themes</h2>

Eigentlich wollte ich ja nur einen <a href="http://wordpress.org/extend/themes/toolbox">Toolbox</a> Fork erstellen und das Theme um Microdata/Schema.org erweitern und dann hat es doch so viel Spaß gemacht, dass ein eigenes Theme daraus wurde. <a href="https://github.com/pfefferle/SemPress">SemPress</a> ist ein hoch semantische HTML5 Theme, SEO optimiert und responsive.

Hier ein paar Einzelheiten:

<ul>
<li><strong><a href="http://diveintohtml5.info/semantics.html#new-elements">Semantische Tags</a></strong> - Ich habe einfach mal geschaut welche Tags Toolbox noch nicht unterstützt und sie dann, hoffentlich richtig eingebaut :).</li>
<li><strong><a href="http://diveintohtml5.info/forms.html">HTML5 Input-Types</a></strong> - SemPress unterstützt einige der neuen Input-Types wie z.B. "search", "email" und "url". Mehr dazu in einem älteren <a href="https://notiz.blog/2011/07/11/html5-input-types-form-validierung-und-wordpress/">Artikel</a>.</li>
<li><strong>Microformats</strong> - Toolbox selbst unterstütz Microformats ja schon von Haus aus und ich musste nur kleine hAtom fixes und die richtigen <em><a href="http://microformats.org/wiki/rel-profile">Profile Header</a></em> setzen.</li>
<li><strong>Microformats v2</strong> - Ich bin zwar <a href="https://notiz.blog/2012/07/03/microformats-the-next-generation/">kein großer Fan</a> von <a href="http://microformats.org/wiki/microformats_2">Microformats 2</a>, aber ich wollte testen wie leicht sich das Theme um neues HTML-Classes erweitern lässt und wie viel Arbeit es bedeutet. SemPress unterstützt hCard 2 und hAtom 2.</li>
<li><strong>Microdata/Schema.org</strong> - Ähnlich wie bei Microformats v2 wollte ich testen wie schwer es ist, <a href="http://schema.org/">Schema.org</a> einzubauen. Das Theme unterstützt http://schema.org/Blog, http://schema.org/BlogPosting and http://schema.org/Person.</li>
</ul>

Mehr dazu hier: <a href="https://notiz.blog/2012/09/06/ive-made-a-wordpress-theme-kind-of/">I’ve made a WordPress Theme… kind of…</a>

<hr />

<h2 id="microformats">Microformats</h2>
<img src="https://notiz.blog/wp-content/uploads/2007/03/mf-white.png" alt="mf-white" title="mf-white" width="150" height="150" class="alignright size-full" />Ich bin großer Microformats Fan (und wäre ein noch größerer wenn sich die Community für <a href="https://notiz.blog/tag/microdata/">Microdata</a> als neuen Container entscheiden würde).
<ul><li><a href="https://notiz.blog/projects/mycroformats/">mycroformats</a>: a firefox mycroft plugin to search the microformats wiki/blog.</li>
<li><a href="https://notiz.blog/projects/microformats-icons/">Microformats Icons</a>: some icons based on the microformats-icons devkit.</li>
<li><a href="https://notiz.blog/projects/haudio-icons/">hAudio Icons</a>: hAudio icons based on the microformats-icons devkit.</li>
<li><a href="https://notiz.blog/projects/operator-user-scripts/">Operator User Scripts</a>: some user scripts for the operator firefox plugin.</li>
<li><a href="https://web.archive.org/web/20130615010926/http://planetmikroformate.de/" rel="me">Planet Mikroformate</a>: Die deutsche Version von <a href="http://planetmicroformats.com">Planet-Microformats</a>.</li>
<li><a href="http://www.microform.at" rel="me">microform.at</a>: <strong>Der</strong> Microformats-Transformer von <a href="http://weborganics.co.uk/" rel="contact">Martin McEvoy</a>!</li></ul>

<hr />

<h2 id="podcast">OpenWeb Podcast</h2>

<strong>2008 riefen Sebastian Küpers, Christian Scholz und ich den <a href="http://openwebpodcast.de/" rel="me">OpenWeb Podcast</a> ins leben. Bis 2011 entstanden 33 Folgen zu Themen wie OpenID, OAuth und Microformats. 2012 haben wir uns entschieden den Podcast einzustellen und uns der <a href="http://technikwuerze.de/das-team/#teammod_mf" rel="me">Technikwürze</a> anzuschließen.</strong>

<img src="//notiz.blog/wp-content/uploads/2012/01/owp-logo-300.jpg" alt="OpenWebPodcast Logo" title="OpenWebPodcast Logo" width="300" height="300" class="alignright withborder size-full wp-image-4154" />Kaum ein Tag vergeht ohne die Gründung eines neuen Startups rund um den Bereich des Social Networking. Wie ein normaler Benutzer all diese Services und Netzwerke allerdings noch managen soll, ist fraglich. Jeder Service, jedes Netzwerk will wieder persönliche Daten haben, will Freunde finden, braucht einen Account. Das ist im 2D-Web so und das ist mehr und mehr auch im 3D-Bereich bei virtuellen Welten so.

Dem soll Abhilfe geschaffen werden und weltweit sind viele Leute dabei, Standards und Best Practices zu entwerfen, die diese Probleme beheben.

Vieles davon geschieht nicht in Deutschland und bleibt daher dem gemeinen Internetnutzer verborgen. Der <a href="http://openwebpodcast.de/" rel="me">OpenWeb-Podcast</a> soll dies ändern und ein bisschen Licht in das Dunkel dieser Standards bringen.

<h3>Links zum Podcast</h3>

<ul><li><a href="http://openwebpodcast.de/feed/">RSS Feed</a></li>
<li><a href="http://phobos.apple.com/WebObjects/MZStore.woa/wa/viewPodcast?id=294732929">iTunes</a></li></ul>

<h3>Folgen</h3>

<ul>
	<li><a href="http://openwebpodcast.de/37/episode-1-eine-einfuhrung/" title="Episode 1 – Eine Einführung" rel="bookmark">Episode 1 – Eine Einführung</a></li>
	<li><a href="http://openwebpodcast.de/36/episode-2-die-openid-einfuhrung/" title="Episode 2 – Die OpenID Einführung" rel="bookmark">Episode 2 – Die OpenID Einführung</a></li>
	<li><a href="http://openwebpodcast.de/35/episode-3-oauth/" title="Episode 3 – OAuth" rel="bookmark">Episode 3 – OAuth</a></li>
	<li><a href="http://openwebpodcast.de/33/episode-4-openid-fur-tekkies/" title="Episode 4 – OpenID für Tekkies" rel="bookmark">Episode 4 – OpenID für Tekkies</a></li>
	<li><a href="http://openwebpodcast.de/32/episode-5-microformats/" title="Episode 5 – Microformats" rel="bookmark">Episode 5 – Microformats</a></li>
	<li><a href="http://openwebpodcast.de/31/episode-6-distributed-social-networking/" title="Episode 6 – Distributed Social Networking" rel="bookmark">Episode 6 – Distributed Social Networking</a></li>
	<li><a href="http://openwebpodcast.de/30/episode-7-opensocial/" title="Episode 7 – OpenSocial" rel="bookmark">Episode 7 – OpenSocial</a></li>
	<li><a href="http://openwebpodcast.de/28/episode-8-facebook-connect-myspaceid-google-friend-connect-und-der-open-stack/" title="Episode 8 – Facebook Connect, MySpaceID, Google Friend Connect und der Open Stack" rel="bookmark">Episode 8 – Facebook Connect, MySpaceID, Google Friend Connect und der Open Stack</a></li>
	<li><a href="http://openwebpodcast.de/27/episode-9-weihnachten-naht-und-wir-machen-bestandsaufnahme/" title="Episode 9 – Weihnachten naht und wir machen Bestandsaufnahme" rel="bookmark">Episode 9 – Weihnachten naht und wir machen Bestandsaufnahme</a></li>
	<li><a href="http://openwebpodcast.de/26/episode-10-privatsphare/" title="Episode 10 – Privatsphäre" rel="bookmark">Episode 10 – Privatsphäre</a></li>
	<li><a href="http://openwebpodcast.de/25/episode-news-news-news/" title="Episode 11 – News News News" rel="bookmark">Episode 11 – News News News</a></li>
	<li><a href="http://openwebpodcast.de/24/facebook/" title="Episode 12 – Facebook" rel="bookmark">Episode 12 – Facebook</a></li>
	<li><a href="http://openwebpodcast.de/98/episode-13-news-und-zensursula/" title="Episode 13 – News und Zensursula" rel="bookmark">Episode 13 – News und Zensursula</a></li>
	<li><a href="http://openwebpodcast.de/107/episode-14-was-bringt-eigentlich-data-portability/" title="Episode 14 – Was bringt eigentlich Data Portability?" rel="bookmark">Episode 14 – Was bringt eigentlich Data Portability?</a></li>
	<li><a href="http://openwebpodcast.de/115/episode-15-web-of-identities/" title="Episode 15 – Web of Identities" rel="bookmark">Episode 15 – Web of Identities</a></li>
	<li><a href="http://openwebpodcast.de/137/episode-16-wir-bitten-um-ihre-aufmerksamkeit/" title="Episode 16 – Wir bitten um Ihre Aufmerksamkeit!" rel="bookmark">Episode 16 – Wir bitten um Ihre Aufmerksamkeit!</a></li>
	<li><a href="http://openwebpodcast.de/171/owp17/" title="Episode 17 – Ein Nachrichtenüberblick" rel="bookmark">Episode 17 – Ein Nachrichtenüberblick</a></li>
	<li><a href="http://openwebpodcast.de/177/owp18/" title="Episode 18 – Offenes Deutschland?" rel="bookmark">Episode 18 – Offenes Deutschland?</a></li>
	<li><a href="http://openwebpodcast.de/187/owp19/" title="Episode 19 – Die Google-Welle" rel="bookmark">Episode 19 – Die Google-Welle</a></li>
	<li><a href="http://openwebpodcast.de/205/episode-20-wer-bin-ich/" title="Episode 20 – Wer bin ich?" rel="bookmark">Episode 20 – Wer bin ich?</a></li>
</ul>

<hr />

<h2 id="twelvethings">12things</h2>

[caption id="attachment_14883" align="aligncenter" width="900"]<a href="https://notiz.blog/projects/12things-website/" rel="attachment wp-att-14883"><img src="https://notiz.blog/wp-content/uploads/2007/03/12things-website-900x660.png" alt="12things Website" width="900" height="660" class="size-large wp-image-14883" /></a> 12things Website[/caption]