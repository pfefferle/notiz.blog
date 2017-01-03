---
ID: 1844
post_title: 'NoisePress: Nie wieder irrelevante Inhalte'
author: Matthias Pfefferle
post_date: 2010-11-05 08:16:27
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2010/11/05/noisepress-nie-wieder-irrelevante-inhalte/
published: true
---
<img src="http://notiz.blog/wp-content/uploads/2010/06/noisepress-logo.png" alt="Erst filtern, dann abonnieren!" title="NoisePress" width="128" height="128" class="alignright size-full wp-image-2913" />Die Informationsflut im Internet nimmt immer mehr zu und FeedReader bieten bisher keine wirkliche Möglichkeit diese Informationen sinnvoll zu filtern und da man nicht wirklich (zeitnah) Einfluss auf die Weiterentwicklung von NetNewsWire, Google Reader &amp; Co. hat, bleibt nur noch eins: <strong>Erst filtern, dann abonnieren!</strong>

<a href="http://notiz.blog/?noisepress=feedfilter">NoisePress</a> erlaubt Seitenbesucher, einen RSS/ATOM-Feed mit Hilfe von <abbr title="Attention Profiling Mark-up Language"><a href="http://notiz.blog/2007/11/23/apml-attention-profiling-mark-up-language/">APML</a></abbr> vorzufiltern.

(Zum ausprobieren braucht man ein APML-Profil. Wer keines hat, sollte sich entweder das <a href="http://wordpress.org/extend/plugins/apml/">WordPress Plugin</a> installieren oder heimlich <a href="http://notsorelevant.com/apml">Carstens Profil</a> benutzen ;) )

<h4>Warum mit APML filtern?</h4>

Man könnte natürlich auch mit <em>WordPress</em>-Bordmitteln eine Menge Rauschen ausfiltern, und wirklich nur das abonnieren was gerade wichtig ist:

<ul><li>Tags Feed:  <a href="http://notiz.blog/tag/openid,oauth/feed/">http://notiz.blog/tag/openid,oauth/feed/</a></li>
<li>Category Feed: <a href="http://notiz.blog/category/openweb-notizen/feed/">http://notiz.blog/category/openweb-notizen/feed/</a></li></ul>

Das Problem: Ändert sich dieses Interesse, müssen alle Feeds mühsam aussortiert (und neue gesammelt) werden. Außerdem besteht die Gefahr, dass einige <em>spannende</em> Themen, die nicht genau die abonnierte Kategorie/den abonnierten Tag besitzen, durch das Raster fallen können.

Das Prinzip von NoisePress: APML ist eine Art semantische Tag-Clound die das Interesse einer Person widerspiegelt. Das <em>Interessens-Profil</em> wird in der Regel automatisch generiert und sollte sich somit auch den diversen Interessensveränderungen anpassen.

Am Beispiel <em>WordPress Plugin</em>: Das Plugin erstellt ein APML-File anhand der Häufigkeit der verwendeten Tags und Kategorien. Schreibt jemand viel über OpenID, kann man davon ausgehen, dass er das Thema für wichtig hält. Ändert sich der Fokus des Blogs, wird OpenID auch im APML-Feed immer irrelevanter.

<h4>Hört sich nach Geek-Zeugs an?</h4>

Richtig! :) ...aber NoisePress ist auch erst einmal nur ein Test ob meine Idee überhaupt funktioniert! Im besten Fall soll der User von all der Technik gar nichts mitbekommen. Ich hoffe dass sich Firefox' <a href="http://www.mozilla.com/en-US/firefox/accountmanager/">Account Manager</a> oder <a href="http://xauth.org">XAuth</a> schnell weiter entwickeln und ich eine dieser Techniken für NoisePress <em>missbrauchen</em> könnte.

Ich würde mich übrigens sehr über ein bisschen Feedback freuen!