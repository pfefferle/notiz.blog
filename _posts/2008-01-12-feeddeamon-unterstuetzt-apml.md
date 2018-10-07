---
ID: 704
post_title: FeedDemon unterstützt APML
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/01/12/feeddeamon-unterstuetzt-apml/
published: true
post_date: 2008-01-12 18:06:49
---
<!-- wp:paragraph -->
<p>Nachdem <a href="http://www.newsgator.com">newsgator</a>, die Firma hinter <a href="http://www.newsgator.com/Individuals/NetNewsWire/Default.aspx">NetNewsWire</a> (NNW) und <a href="http://www.newsgator.com/Individuals/FeedDemon/Default.aspx">FeedDemon</a>, <a href="http://www.newsgator.com/CompanyInfo/Press/Archive.aspx?post=144">am Mittwoch bekannt gab</a> dass die neuen Versionen ihrer <abbr title="Really Simple Syndication">RSS</abbr> Reader ab sofort kostenlos erhältlich seien...</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>NewsGator Releases New Versions of Client Products; Best-of-Breed RSS Readers Now Free. <a href="http://www.newsgator.com/CompanyInfo/Press/Archive.aspx?post=144">#</a></p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>...habe ich mir mal den neuen FeedDemon angeschaut und entdeckt, dass er ab der Verion 2.6 schon <abbr title="Attention Profiling Mark-up Language"><a href="http://www.apml.org">APML</a></abbr> unterstützt.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/01/feeddeamon-apml.jpg" alt="feeddemon apml" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Wie schon im Oktober angekündigt unterstützt diese Version zuerst einmal den Export der Feeds in <abbr title="Attention Profiling Mark-up Language">APML</abbr> (ähnlich wie beim <abbr title="Outline Processor Markup Language">OPML</abbr> export):</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>The first step will be APML export, which is already underway. Once we've worked out a few details, we'll also support <abbr title="Attention Profiling Mark-up Language">APML</abbr> import.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Die <abbr title="Attention Profiling Mark-up Language">APML</abbr> Sources sehen beispielsweise so aus:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><abbr title="Attention Profiling Mark-up Language">APML</abbr>: <code>&lt;Source key="http://feeds.feedburner.com/notsorelevant" from="Not So Relevant" updated="2008-01-11T00:00:28" value="0,00" type="application/rss+xml" path="Web 2.0"/></code></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Es handelt bei dem Feed-<abbr title="Attention Profiling Mark-up Language">APML</abbr> also um eine Art OPML-File mir Bewertung.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><abbr title="Outline Processor Markup Language">OPML</abbr>: <code>&lt;outline text="Not So Relevant" title="Not So Relevant" type="rss" xmlUrl="http://feeds.feedburner.com/notsorelevant" htmlUrl="http://www.notsorelevant.com" description="another look on music and the web"/></code></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Wer genau wissen will wie sich der <code>value</code> Wert errechnet, kann ja mal den "<a href="http://nick.typepad.com/blog/2007/11/how-does-feedde.html">How Does FeedDemon Calculate Attention?</a>" - Artikel bei Nick Bradbury lesen. Mal gespannt wie die APML-Importfunktion aussehen wird und wann die anderen Feed Reader von <a href="http://www.newsgator.com">newsgator</a> nachziehen werden.</p>
<!-- /wp:paragraph -->