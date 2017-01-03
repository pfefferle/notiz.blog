---
ID: 272
post_title: Microformats in WordPress nutzen
author: Matthias Pfefferle
post_date: 2006-12-03 12:53:04
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2006/12/03/microformats-in-wordpress-nutzen/
published: true
---
Wer zu faul ist seine Blog-Posts im richtigen Microformat zu formatieren oder es in sein Theme zu implementieren, der bekommt hier ein paar Erleichterungen.

<strong>Plugins</strong>

<strong><a href="http://www.aes.id.au/?page_id=28">hReview WordPress Plugin</a></strong> ist ein simples Plugin um hReviews in normalen Einträgen zu erstellen. Nach dem aktivieren erscheint in "Write Posts" ein neuer Butten über dem Textfeld. Also zuerst den normalen Text schreiben, dann hReview Knopf drücken Formular ausfüllen und ab damit. Andrew E. Scott hatte gerne <a href="http://www.aes.id.au/?page_id=28#comments">Rückmeldung</a> ob alles sauber funktioniert, also macht ihm doch den gefallen.

<strong><a href="http://factorycity.net/projects/wp-microformatted-blogroll/">WP Microformatted Blogroll 0.2</a></strong> lässt euch Linklisten (<a href="http://de.wikipedia.org/wiki/Blogrolle">Blogrollen</a>), gekennzeichnet durch <a href="http://microformats.org/wiki/xoxo">XOXO</a>, <a href="http://microformats.org/wiki/hcard">hCard</a> und <a href="http://xmpg.org/xfn">XFN</a> erstellen.

<strong><a href="http://www.richardkmiller.com/blog/archives/2006/03/microid-plugin-for-wordpress">MicroID Plugin for WordPress</a></strong> Von <a href="http://www.microid.org/">MicroID</a> hatte ich bisher noch nicht gehört, aber es ist ziemlich simpel. Es erstellt einen Hash-Wert aus der E-Mail Adresse und der eigenen URL, welchen man zur Identifizierung verwenden kann. Also im Prinzip so ähnlich wie die <a href="http://www.gravatar.com">Gravatare</a>. Meiner z.B. ist <code>9198c94d942fa09454fa84b2ce447362d70abc1a</code>. Das Plugin, schreibt diesen Wert in die Metatags von Wordpress
<p class="code">&lt;meta name="microid" content="9198c94d942fa09454fa84b2ce447362d70abc1a" /&gt;</p> zum Kennzeichnen des Blogs oder von Autoren eines einzelnen Eintrags.

Und zu <a href="http://microformats.org/wiki/geo">GEO</a>-Informationen gibt es ne ganze Menge <a href="http://wp-plugins.net/?filter=geo">Plugins</a>.

<strong>Themes</strong>

Folgende Themes unterstützen hAtom:
<ul>
<li><a href="http://www.plaintxt.org/themes/sandbox/">Sandbox</a> ein Theme für Themer</li>
<li><a href="http://www.whump.com/dropbox/Strangelove.zip">Strangelove</a> ein modifiziertes <a href="http://binarybonsai.com/wordpress/kubrick/">Kubrick Theme</a></li>
</ul>

Das <a href="http://getk2.com">K2 Theme</a> von <a href="http://binarybonsai.com/about/">Michael Heilemann</a> zeigt die Autoren aller Einträge im hCard Format an und das Datum in Form der <a href="http://microformats.org/wiki/abbr-design-pattern">abbr-design-pattern</a>.

Oder für die, die ihre Microformats mit einem StyleSheet selbst formatieren wollen gibt es unter <a href="http://www.mindgarden.de/downloads/microformats.css">mindgarden.de</a> ein schönes CSS Template.

<small>Abschließend noch: Die <a href="http://kitchen.technorati.com/search/notiz.blog">Technorati Microformats-Suche</a> funktioniert mittlerweile einwandfrei.</small>