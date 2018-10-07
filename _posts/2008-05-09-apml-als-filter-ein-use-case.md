---
ID: 855
post_title: APML als Filter (ein Use-Case)
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/05/09/apml-als-filter-ein-use-case/
published: true
post_date: 2008-05-09 19:48:21
---
<!-- wp:image {"align":"right"} -->
<figure class="wp-block-image alignright"><img src="https://notiz.blog/wp-content/uploads/2007/11/apml-icon-128x128.png" alt="APML Logo" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Letzte Woche ist auf <a href="http://www.basicthinking.de/blog/2008/05/02/apml/">Robert Basics Artikel zu APML</a> eine interessante Diskussion zu dem Sinn und Zweck von <abbr title="Attention Profiling Mark-up Language">APML</abbr> entstanden. Einer der größten Kritikpunkte an dem <a href="http://www.apml.org">Attentiondata-Format</a> ist das fehlende "normierte Vokabular" und die <a href="http://www.basicthinking.de/blog/2008/05/02/apml/#comment-822501">daraus entstehenden Probleme</a> beim verarbeiten.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ich kann diese Kritikpunkte zwar nachvollziehen, bin aber dennoch der Meinung dass es auch für die aktuelle Form des <a href="http://www.apml.org/developers/spec/">Attention-XMLs</a> einige Anwendungs-Szenarien gibt, die ich hier beschreiben möchte...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Die Informationsflut im Internet wird immer größer und schneller, wie Herr Scoble in seinem Artikel "<em><a href="http://scobleizer.com/2008/05/08/the-noise-reduction-system/">The noise reduction system</a></em>" sehr treffend bemerkt:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Oh, the glorious noise! Everyone loves beating me up for causing the noise. No, I am not the cause. I pass it along. You should see my inbound streams. Every second or two a new Twitter is aimed at me. Every few seconds, a new blog post comes into Google Reader. Every few seconds, a new thing on FriendFeed.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Der Artikel ist auf alle Fälle lesenswert und beschreibt auch einige Lösungsansätze, auf die ich aber nicht weiter eingehen möchte. Was ich viel interessante finde ist, dass <abbr title="Attention Profiling Mark-up Language">APML</abbr> genau der richtige Filter für dieses <a href="http://netzwertig.com/2008/05/09/linkwertig-der-biblische-signal-noise-kampf/">Signal-Noise-Ratio</a> - Problem ist.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2><abbr title="Attention Profiling Mark-up Language">APML</abbr> als News-Filter</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Einer der Themen in Scobles Beitrag ist die enorme Flut von Informationen/News die täglich in seinem News-Reader auflaufen. Um diesem Problem Herr zu werden bräuchte man einen Filter, der selbstständig entscheidet was für ihn relevant ist und was nicht.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ein APML-File bietet alles was für einen einfachen Filter notwendig ist:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li>Eine Gewichtung meiner Interessen</li>
	<li>Eine einfache Struktur</li>
	<li>URLs/Feeds die ich bevorzuge</li>
</ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Mit diesen Informationen sollte es doch recht einfach möglich sein, die Neuigkeiten die in (z.B.) meinem Feed-Reader auflaufen zu bewerten und mir einen (ausgewählten) News-Stream zu präsentieren. So zusagen ein Spam-Filter für News (und einem Spam-Filter sind wir ja auch nicht böse wenn mal eine Mail durchrutscht, weil er uns doch ne ganze menge Arbeit erspart).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Da es sich bei diesem Filter nur um ein optionales Feature handelt, bleibt es dem Nutzer selbst überlassen welcher Art des Informations-Konsums er frönen will.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="http://www.newsgator.com/">NewsGator</a>, einer der führenden Feed-Reader Anbieter, hat auch schon einige Schritte in diese Richtung angekündigt und bietet bei einigen seiner Produkte auch schon ein paar <a href="https://notiz.blog/?s=apml+newsgator">APML-Funktionalitäten</a> an.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>APML als Kommunikations-Filter</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Der andere angesprochene Punkt ist die Kommunikation verursacht durch Microblogging-Dienste wie <a href="http://twitter.com">Twitter</a>, <a href="http://jaiku.com">Jaiku</a> oder <a href="http://friendfeed.com">FriendFeed</a>. Will man diese aktiv verfolgen ist es nahezu unmöglich nebenher noch einer normalen Tätigkeit nach zu gehen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Um noch einmal Herrn Scoble zu zitieren:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>The problem? Twitter and FriendFeed have brought new noise into our lives (at least for the early adopter types) and there aren’t good ways to reduce the noise.</p>
	<p>But FriendFeed shows us a way out. How about seeing only posts that have at least two “likes?” Isn’t that a way to reduce the noise? Yes! [...]</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Auch hier würde ein Filter in Form meiner Attention-Daten den Kommunikations-Stream enorm reduzieren. Wenn Auszeichnungen wie <a href="http://hashtags.org/">#hashtags</a> weiter Verbreitung finden sollte es nicht schwer sein, diese mit meinen Attention-Tags zu vergleichen und zu bewerten. Selbst ohne #hashtags ist es immer noch möglich, den Inhalt (sind ja nur 140 Zeichen) mit den Interessen abgleichen.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/05/facebook-einstellungen.jpg" alt="facebook-einstellungen.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Im nächsten Schritt könnte man den User (ähnlich wie bei Facebook) entscheiden lassen, welches Ranking die Inhalte mindestens haben müssen um angezeigt zu werden.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ich denke gerade bei diesen zwei Anwendungsbeispiele ist die einfache XML-Struktur eher ein Vorteil als ein Nachteil. Das Ranking sollte schnell und unkompliziert funktionieren und es sollte auch kein Problem sein, wenn eine Information durch diesen Filter rutschen sollte.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="http://netzwertig.com/2008/05/09/linkwertig-der-biblische-signal-noise-kampf/">Via Marcel Weiss' Artikel "Der biblische Signal-Noise-Kampf"</a></p>
<!-- /wp:paragraph -->