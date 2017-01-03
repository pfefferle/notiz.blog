---
ID: 683
post_title: >
  myOpenID Neuerungen mit WordPress
  abbilden
author: Matthias Pfefferle
post_date: 2007-12-18 18:30:32
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/12/18/myopenid-neuerungen-mit-wordpress-abbilden/
published: true
---
Bei <a href="http://www.myopenid.com/">myOpenID</a> gibt es seit kurzem zwei große Erweiterungen:
<ul>
<li><strong>Identity Pages</strong> (das öffentliche Profil: http://username.myopenid.com) unterstützt jetzt neben verschiedenen Themes auch einige "Web 2.0 technologies" wie z.B. <a href="http://microformats.org/wiki/hcard">hCard</a>, <a href="http://pavatar.com/">Pavatar</a> und <a href="http://microid.org/">MicroID</a>.</li>
<li>Über <strong>Attribute Exchange</strong> ist es zusätzlich möglich, mehrere Personen-Profile abzugleichen.</li>
</ul>

Wer das ganze im Sinne von <abbr title="distributed social networking concepts"><a href="http://www.diso-project.org/">DiSo</a></abbr> mit seinem <a href="http://wordpress.org">WordPress</a> Blog nachbauen will, braucht nur folgende Plugins:
<ul><li><strong>hCard</strong>: Themes wie <a href="http://getk2.com">K2</a> zeichnen generell jeden Autor als hCard aus, ohne dass man irgendein Plugin benötigt und <a href="http://diso.googlecode.com/svn/wordpress/wp-diso-contactlist/">wp-diso-contactlist</a> zeichnet die komplette Blogrolle mit hCard und XFN aus.</li>
<li><strong>Pavatar</strong>: Das <a href="http://www.john-noone.com/2006/10/08/identikit/">Identikit</a> von John Noone bietet neben einigen Avatar-Implementierungen auch Support für Pavartar.</li>
<li><strong>MicroID</strong>: Das <a href="http://willnorris.com/projects/wp-microid">MicroID WordPress Plugin</a> von Will Norris bietet die Möglichkeit, mehrere IDs anhand verschiedener E-Mail Adressen oder OpenIDs zu erstellen.</li>
<li><strong>OpenID/Attribute Exchange</strong>: <a href="http://willnorris.com/projects/wp-openid">WP OpenID</a> ist offizieller Teil des DiSo-Projekts und bietet einen umfangreichen OpenID Client, basierend auf der <a href="http://openidenabled.com/php-openid/">PHP OpenID Library</a> von <a href="http://janrain.com/">JanRain</a>. Ein OpenID Server ist noch nicht vorhanden, es gibt jedoch einige <a href="http://http://diso-project.org/wiki/index.php?title=Main_Page#OpenID">Delegation Plugins</a> und DiSo plant auch noch eine ganze Menge in Richtung OpenID</li></ul>

Falls ihr noch einige gute Plugins kennt, die hier nicht gelistet sind (vielleicht eine alternative zum Pavatar Plugin) würde ich mich über ein Kommentar freuen.