---
ID: 781
post_title: Welche hCard ist die richtige?
author: Matthias Pfefferle
post_date: 2008-03-16 19:24:26
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/03/16/welche-hcard-ist-die-richtige/
published: true
aktt_tweeted:
  - "1"
---
Wer schonmal versucht hat <a href="http://microformats.org/wiki/hcard">hCard</a> Profile zu importieren wird sicherlich auf ein Problem stoßen: <em>Welche hCard ist die richtige?</em>

Vor ein paar Tagen habe ich ein Gespräch zwischen <span class="hcard"><a href="http://twitter.com/dirk_olbertz/statuses/771154238" class="url fn">Dirk Olbertz</a></span> und <span class="hcard"><a href="http://twitter.com/t/statuses/771155935" class="url fn">Tantek Çelik</a></span> via Twitter verfolgt, bei dem es genau um dieses Problem ging...

Das Problem der <em>representative hCard</em> kann auf zwei verschiedene Weisen gelöst werden:
<blockquote cite="http://twitter.com/t/statuses/771155935">...in short 1. url==uid==source. 2. url has rel-me</blockquote>

<h3>url==uid==source</h3>

Die einfachste Möglichkeit ist, zu überprüfen ob eine der (unter der angegebenen Source-<abbr title="Uniform Resource Locator">URL</abbr>) gefundenen hCards als <abbr title="Uniform Resource Locator">URL</abbr> die die Source-<abbr title="Uniform Resource Locator">URL</abbr> enthält. Wenn man sicher gehen will, sollte man die URL zusätzlich noch als <a href="http://microformats.org/wiki/uid">UID</a> (<a href="http://www.ietf.org/rfc/rfc2426.txt" class="external" title="http://www.ietf.org/rfc/rfc2426.txt" rel="nofollow">RFC2426</a>) auszeichnen.

Ein Beispiel für eine <em><a href="http://microformats.org/wiki/representative-hcard">representative hCard</a></em> für <code>http://notsorelevant.com</code> wäre:

<pre class="code">&lt;span class=&quot;vcard&quot;&gt;
	&lt;span class=&quot;fn&quot;&gt;Carsten Pötter&lt;/span&gt;
	&lt;span class=&quot;url uid&quot;&gt;http://notsorelevant.com&lt;/span&gt;
&lt;/span&gt;</pre>

<h3>rel-me</h3>

Die zweite Möglichkeit ist, nach hCards mit <code><a href="http://microformats.org/wiki/rel-me">rel="me"</a></code> <abbr title="Uniform Resource Locator">URL</abbr>s zu suchen.

Diese Variante lässt sich natürlich auch mit der Ersten verbinden:

<pre class="code">&lt;span class=&quot;vcard&quot;&gt;
	&lt;span class=&quot;fn&quot;&gt;Carsten Pötter&lt;/span&gt;
	&lt;span class=&quot;url uid&quot; rel=&quot;me&quot;&gt;http://notsorelevant.com&lt;/span&gt;
&lt;/span&gt;</pre>

Wer also ganz sicher gehen möchte sollte das letzte Beispiel nutzen :)

Für Web-Seiten die gar keine Profile oder zumindest keine Profile auf der Startseite haben, könnte <code><a href="http://microformats.org/wiki/rel-me">rel="me"</a></code> auch als <em>Delegation</em> zu einer (anderen) Seite mit einer <em>representative hCard</em> genutzt werden.

Beispiel: <code>&lt;link rel="me" href="http://www.notsorelevant.com/ueber/" /&gt;</code>

Da es für <abbr title="PHP: Hypertext Preprocessor">PHP</abbr> (meines Wissens) noch keinen <abbr title="XHTML Friends Network">XFN</abbr>-Parser gibt, habe ich mich beim <a href="http://notiz.blog/projects/wp-hcard-commenting/" rel="me">hCard-Commenting WordPress Plugin</a> für die erste Variante (url==uid==source) entschieden... Ich hoffe es funktioniert :)

Weitere Informationen zu <em>representative hCards</em> im Microformats-Wiki:
<ul><li><a href="http://microformats.org/wiki/representative-hcard" rel="bookmark">representative hCard</a></li>
<li><a href="http://microformats.org/wiki/representative-hcard-parsing" rel="bookmark">representative hCard parsing</a></li>
<li><a href="http://microformats.org/wiki/rel-me" rel="bookmark">rel-me</a></li></ul>