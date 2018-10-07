---
ID: 781
post_title: Welche hCard ist die richtige?
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/03/16/welche-hcard-ist-die-richtige/
published: true
post_date: 2008-03-16 19:24:26
---
<!-- wp:paragraph -->
<p>Wer schonmal versucht hat <a href="http://microformats.org/wiki/hcard">hCard</a> Profile zu importieren wird sicherlich auf ein Problem stoßen: <em>Welche hCard ist die richtige?</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Vor ein paar Tagen habe ich ein Gespräch zwischen <a href="http://twitter.com/dirk_olbertz/statuses/771154238">Dirk Olbertz</a> und <a href="http://twitter.com/t/statuses/771155935">Tantek Çelik</a> via Twitter verfolgt, bei dem es genau um dieses Problem ging...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Das Problem der <em>representative hCard</em> kann auf zwei verschiedene Weisen gelöst werden:<br/>
</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote"><p>...in short 1. url==uid==source. 2. url has rel-me</p></blockquote>
<!-- /wp:quote -->

<!-- wp:heading {"level":3} -->
<h3>url==uid==source</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Die einfachste Möglichkeit ist, zu überprüfen ob eine der (unter der angegebenen Source-<abbr title="Uniform Resource Locator">URL</abbr>) gefundenen hCards als <abbr title="Uniform Resource Locator">URL</abbr> die die Source-<abbr title="Uniform Resource Locator">URL</abbr> enthält. Wenn man sicher gehen will, sollte man die URL zusätzlich noch als <a href="http://microformats.org/wiki/uid">UID</a> (<a href="http://www.ietf.org/rfc/rfc2426.txt">RFC2426</a>) auszeichnen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ein Beispiel für eine <em><a href="http://microformats.org/wiki/representative-hcard">representative hCard</a></em> für <code>http://notsorelevant.com</code> wäre:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;span class="vcard">
	&lt;span class="fn">Carsten Pötter&lt;/span>
	&lt;span class="url uid">http://notsorelevant.com&lt;/span>
&lt;/span></code></pre>
<!-- /wp:code -->

<!-- wp:heading {"level":3} -->
<h3>rel-me</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Die zweite Möglichkeit ist, nach hCards mit <code><a href="http://microformats.org/wiki/rel-me">rel="me"</a></code> <abbr title="Uniform Resource Locator">URL</abbr>s zu suchen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Diese Variante lässt sich natürlich auch mit der Ersten verbinden:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;span class="vcard">
	&lt;span class="fn">Carsten Pötter&lt;/span>
	&lt;span class="url uid" rel="me">http://notsorelevant.com&lt;/span>
&lt;/span></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Wer also ganz sicher gehen möchte sollte das letzte Beispiel nutzen :)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Für Web-Seiten die gar keine Profile oder zumindest keine Profile auf der Startseite haben, könnte <code><a href="http://microformats.org/wiki/rel-me">rel="me"</a></code> auch als <em>Delegation</em> zu einer (anderen) Seite mit einer <em>representative hCard</em> genutzt werden.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Beispiel: <code>&lt;link rel="me" href="http://www.notsorelevant.com/ueber/" /></code></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Da es für <abbr title="PHP: Hypertext Preprocessor">PHP</abbr> (meines Wissens) noch keinen <abbr title="XHTML Friends Network">XFN</abbr>-Parser gibt, habe ich mich beim <a href="https://notiz.blog/projects/wp-hcard-commenting/">hCard-Commenting WordPress Plugin</a> für die erste Variante (url==uid==source) entschieden... Ich hoffe es funktioniert :)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Weitere Informationen zu <em>representative hCards</em> im Microformats-Wiki:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><a href="http://microformats.org/wiki/representative-hcard">representative hCard</a></li>
	<li><a href="http://microformats.org/wiki/representative-hcard-parsing">representative hCard parsing</a></li>
	<li><a href="http://microformats.org/wiki/rel-me">rel-me</a></li>
</ul>
<!-- /wp:list -->