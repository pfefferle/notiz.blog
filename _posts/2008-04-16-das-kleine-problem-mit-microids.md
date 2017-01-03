---
ID: 816
post_title: Das kleine Problem mit MicroIDs
author: Matthias Pfefferle
post_date: 2008-04-16 21:49:45
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/04/16/das-kleine-problem-mit-microids/
published: true
aktt_tweeted:
  - "1"
---
Nach den <a href="http://www.notsorelevant.com/2008-04-14/mybloglog-adds-microid-and-foaf/">Ankündigungen</a>, dass <a href="http://www.mybloglog.com/">myBlogLog</a> <a href="http://www.microid.org/">MicroID</a> für die eigenen Profilseiten einsetzt (bsp.: <a href="http://www.mybloglog.com/buzz/members/pfefferle/">www.mybloglog.com/buzz/members/pfefferle/</a>) habe ich mich gefragt, warum myBlogLog MicroIDs nur anbietet, nicht aber für die <a href="http://www.notsorelevant.com/2008-02-15/mybloglog-supports-microformats-but-not-microid/">Verifizierung der Blogs</a> verwendet.

Aber zuerst mal eine kurze Einführung. MicroID ist eine einfache Möglichkeit, den Besitz von Webseiten zu validieren.

<blockquote>MicroID enables anyone to claim verifiable ownership over content hosted anywhere on the web (social networking sites, discussion forums, blogs, etc.).</blockquote>

Das Prinzip ist einfach, es wird ein Hash-Wert aus zwei unterschiedlichen URLs (auch Pseudo-URLs wie z.B. "mailto:" oder "xmpp://" sind möglich) gebildet und als Metatag in die Webseite eingebunden.

<pre><code>hash = sha1(
    sha1( "mailto:mustermann@example.com" ) 
    + 
    sha1( "http://www.example.com/" ) 
  )</code></pre>

Alternativ zu sha1 kann z.B. auch MD5 verwendet werden. Der Aufbau des Metatags sieht folgendermassen aus <code>uri+uri:algo:hash</code>

<pre><code>&lt;meta name="microid" 
  content="mailto+http:sha1:
    ba37d92454792b65838c9827a8d75171c7241924" /&gt;</code></pre>

<h4>Der Vorteil eines proprietären Formats im Gegensatz zu MicroID</h4>

Was die genauen Gründe dafür sind, dass <a href="http://www.mybloglog.com/">myBlogLog</a> ein eigenes Format verwendet weiß ich natürlich nicht, aber schaut man sich MicroID etwas genauer an, findet man doch einige kleine Problemchen.

Eigentlich ist es ja nur ein wirkliches Problem, und zwar die <abbr title="Uniform Resource Locator">URL</abbr>... Eine <abbr title="Uniform Resource Locator">URL</abbr> kann man auf zu viele verschieden Weisen schreiben, als dass sie eine valide ID abgeben könnte:

<ul><li><code>http://example.com</code></li>
<li><code>http://<strong>www.</strong>example.com</code></li>
<li><code>http://example.com<strong>/</strong></code></li></ul>

Zusammen mit der E-Mail - Adresse <code>mustermann@example.com</code> bekommt man drei verschiedene Hash-Werte:

<ul><li><code>19358536d8c443614bc7d861f4b050ee34a549b9</code></li>
<li><code>05c732700bfa89cd234bb7fc08cb673f7c0d88b8</code></li>
<li><code>9275b4dcd7cc2c997b2a5249420b422e937d36e0</code></li></ul>

Das heißt, es kommt immer darauf an wie der Benutzer seine <abbr title="Uniform Resource Locator">URL</abbr> bei einem entsprechenden Service angibt. Ist für den Metatag der Webseite <code>http://example.com</code> verwendet und beim Service <code>http://www.example.com/</code> angegeben worden, kann die Webseite nicht verifiziert werden, da sich die Hash-Werte unterscheiden.

<h4>Lösungsvorschläge</h4>

Eine mögliche Lösung wäre alle denkbaren <abbr title="Uniform Resource Locator">URL</abbr>s auszuprobieren, was nicht sehr performant wäre und eine menge Zeit beanspruchen würde. Die (meiner Meinung nach) bessere Lösung wäre eine Art "<a href="http://notiz.blog/2008/04/15/xrds-simple-und-dataportability/#service-catalogue">service catalogue</a>" an, in dem festgelegt ist wie z.B. die von myBlogLog verwendete MicroID-<abbr title="Uniform Resource Locator">URL</abbr> aussieht.

Ein Beispiel: <code>http://www.mybloglog.com/buzz/members/<strong>Username</strong>/</code>

Das Problem bezieht sich natürlich nur auf Services/Communities, bei denen man keinen Einfluss auf die MicroID hat. Bei persönlichen Weblogs ist das natürlich was anderes, da die <abbr title="Uniform Resource Locator">URL</abbr> und der Matatag vom Benutzer selbst angelegt werden.

Falls jemand noch nen tollen Lösungsvorschlag hätte wäre ich sehr dankbar, weil ich MicroID trotz allem gerne einsetzen würde... Das Prinzip ist einfach so schön simpel :)