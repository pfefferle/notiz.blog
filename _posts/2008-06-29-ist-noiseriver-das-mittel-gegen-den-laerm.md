---
ID: 934
post_title: >
  Ist NoiseRiver DAS Mittel gegen den
  Lärm?
author: Matthias Pfefferle
post_date: 2008-06-29 12:57:37
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/06/29/ist-noiseriver-das-mittel-gegen-den-laerm/
published: true
aktt_tweeted:
  - "1"
---
Vor ungefähr <a href="http://notiz.blog/2008/05/09/apml-als-filter-ein-use-case/">einem Monat</a> habe ich schon einmal darüber geschrieben, wie wichtig Filter für Informationsmedien wie Feed-Reader oder Lifestreams sind. Der Artikel beschreibt, wie man <a href="http://apml.org">Attention-Daten</a> benutzen könnte um die enorme Informationsflut nach Interessen zu filtern.

<a href="http://www.noiseriver.com/">NoiseRiver</a> ist ein erster Versuch die Informationsmenge von <a href="http://friendfeed.com">FriendFeed</a> durch einige Filter übersichtlicher zu gestalten.

<blockquote>You're an addicted user of FriendFeed, and we understand you! isn't it just so Magic!. NoiseRiver is not intended to replace FriendFeed, it's an experimental service still in early alpha stage of developement that aims to extend friendFeed with some cool features like ranking on your interests and/or your feelings about other friendfeed's users. Give it a try, login with your nickname and remote Key!</blockquote>

Für NoiseRiver ist keine separate Registrierung notwendig, man loggt sich einfach mit seinem FriendFeed-Username und dem API-Key ein und bekommt seinen unveränderten <abbr title="FriendFeed">FF</abbr>-Stream präsentiert.

Um diesen Stream leserlicher zu gestalten bietet NoiseRiver zwei Filter-Arten:

<h2>Nach Interessen filtern</h2>

Über den <em><a href="http://www.noiseriver.com/settings/interests">Interessens-Filter</a></em> hat der Nutzer die Möglichkeit seine Interessen als Keywords anzulegen und sie über einen Schieberegler zu gewichten.

<img class="aligncenter" src="http://notiz.blog/wp-content/uploads/2008/06/noiseriver-your-interests-what-you-like-and-what-you-hate.jpg" alt="NoiseRiver - Your interests - What you like and what you hate" border="0" width="480" height="130" />

Um Einträge mit einem speziellen Keyword komplett auszublenden, muss man den Schieberegler einfach nur komplett nach links ziehen und den Punkt "Hide entries with a very high hated rank? (-100%)" aktivieren.

Diese Methode ist leider etwas umständlich, da man neben seinen Interessen auch all seine "Nicht-Interessen" angeben muss, damit sie aus dem Stream verschwinden. Eleganter wäre ein Sortiermechanismus, nach Relevanz und Zeit, der alle Einträge die nicht zu den <em>Interessen</em> des Users gehören, einfach automatisch ausblendet.

...natürlich habe ich sofort nach einer Möglichkeit gesucht um APML-Feeds zu importieren.

<img class="aligncenter" src="http://notiz.blog/wp-content/uploads/2008/06/noiseriver.jpg" alt="NoiseRiver" border="0" width="480" height="159" />

Leider gibt es nur einen <a href="http://www.noiseriver.com/settings/import">Import per Upload</a> (der auch noch nicht ganz funktioniert) und keine Möglichkeit einen APML-Feed direkt zu abonnieren.

<h2>Der Filter über Personen</h2>

Der <em>Personen-Filter</em> ist im Prinzip nichts anderes als der <em>Interessens-Filter</em> auf Basis von Nicknames.

<img class="aligncenter" src="http://notiz.blog/wp-content/uploads/2008/06/noiseriver-your-neighborhood-who-you-like-and-who-you-hate.jpg" alt="NoiseRiver - Your Neighborhood - Who you like and who you hate.jpg" border="0" width="480" height="85" />

Leider werden die Freunde von <abbr title="FriendFeed">FF</abbr> noch nicht in NoiseRiver übernommen und es gibt leider auch noch keine Möglichkeit sie z.B. per <a href="http://notiz.blog/2007/07/15/mit-wevent-freundeslisten-importieren/">hCards</a> zu importieren.

Bisher wird auch bei diesem Filter nicht nach Relevanz sortiert. Die Einträge werden lediglich farblich gekennzeichnet.

<h2>Fazit</h2>

Der Service ist sicherlich nicht ausgereift und braucht noch einige Zeit um ein wirkliches Relevance-Ranking anbieten zu können, spart durch das Ausblenden und Hervorheben von Einträgen jetzt schon eine Menge Zeit beim Lesen.

(via <a href="http://www.louisgray.com/live/2008/06/new-noiseriver-app-adds-interest.html">louisgray.com</a> via Carsten Pötters <a href="http://feeds.feedburner.com/CarstenPoetterSharedItems">Shared-Items</a> (sehr lesenswert))