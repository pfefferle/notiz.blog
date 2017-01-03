---
ID: 786
post_title: DataPortability für Desktop-Anwendungen
author: Matthias Pfefferle
post_date: 2008-03-27 20:12:21
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/03/27/dataportability-fuer-desktop-anwendungen/
published: true
aktt_tweeted:
  - "1"
---
Anfang Februar habe ich einen interessanten Bericht über "<a href="http://skypejournal.com/blog/2008/02/how_portable_is_your_skype_dat.html">How portable is your Skype data?</a>" von <a href="http://skypejournal.com/">Phil Wolff</a> gelesen. Der Artikel befasst sich mit der Daten-Portabilität von Nicht-Web-Applikationen am Beispiel von Skype. Leider wird diese Art des Datenaustauschs (z.B. zwischen Desktop-Anwendungen und Web-Anwendungen) auch von <a href="http://dataportability.org">DataPortability.org</a> noch nicht ausreichend behandelt und es fehlen Formate die diese Art von Austausch ermöglichen (<a href="http://apml.org"><abbr title="Attention Profiling Mark-up Language">APML</abbr></a> mal ausgenommen).

Genau diesen Bericht müssen auch <a href="http://dev.live.com/blogs/devlive/archive/2008/03/25/237.aspx">Microsoft</a> und <a href="http://googledataapis.blogspot.com/2008/03/3-2-1-contact-api-has-landed.html">Google</a> gelesen haben bevor beide diesen Monat ihre Contacts-APIs veröffentlichten :)

Nach den Beschreibungen von <a href="http://googledataapis.blogspot.com/2008/03/3-2-1-contact-api-has-landed.html">Google</a>:
<ul><li>Import a user's Google contacts into their web or desktop application</li><li>Export their application's contact list to Google</li><li>Write sync applications for mobile devices or popular, desktop-based contact management applications</li></ul>

...und <a href="http://dev.live.com/blogs/devlive/archive/2008/03/25/237.aspx">Microsoft</a>:
<blockquote cite="http://dev.live.com/blogs/devlive/archive/2008/03/25/237.aspx">To tackle the issue of contact data portability it is important to reconcile the larger issue of data ownership.  Who owns the data, like email addresses in a Windows Live Hotmail address book?  We firmly believe that we are simply stewards of customers’ data and that customers should be able to choose how they control and share their data. We think customers should be able to share their data in the most safe and secure way possible, but historically this openness has been achieved largely through a mechanism called “screen-scraping,” which unduly puts customers at risk for phishing attacks, identity fraud, and spam. Now with the Windows Live Contacts API, we have provided an alternative to “screen-scraping” that is equally open but unequivocally safer and more secure for customers.</blockquote>

...könnte man fast meinen, dass die Hürde des Datenaustauschs zwischen Desktop-Anwendungen und Web-Anwendungen überwunden wäre. 

Nicht ganz... Leider basieren beide Systeme "noch" auf proprietären Webservices und müssen unterschiedlich angesprochen werden, was eine Menge zusätzlichen Entwicklungsaufwand bedeutet. Die wesentlich bessere Lösung wäre natürlich eine einheitliche Contacts-API oder wie <a href="http://www.notsorelevant.com/2008-03-25/microsoft-introduces-contacts-api/">Carsten Pötter</a> meint:

<blockquote>Of course, it was great if a more open protocol like OAuth was used, but the announcement might encourage more social networks and other corporations to pursue similar steps.</blockquote>

Immerhin gehören die <a href="http://www.brianoberkirch.com/2008/01/04/this-antipattern-is-kryptonite-to-the-open-social-web/">Social-Network-Anti-Patterns</a> durch diese Entwicklungen hoffentlich bald der Vergangenheit an...