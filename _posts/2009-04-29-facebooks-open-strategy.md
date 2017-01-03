---
ID: 1499
post_title: Facebooks Open Strategy?
author: Matthias Pfefferle
post_date: 2009-04-29 08:56:29
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/04/29/facebooks-open-strategy/
published: true
aktt_notify_twitter:
  - 'yes'
aktt_tweeted:
  - "1"
---
In den letzten Tagen hat Facebook einige so spannende Ankündigungen gemacht, dass ich sogar kurz mal meinen Umzugsstress unterbrechen und darüber bloggen muss :)

<h4>Die Facebook Open Stream API</h4>

<a href="http://developers.facebook.com/news.php?blog=1&story=225">Die erste Ankündigung betrifft Facebooks <em>Activity Stream</em></a> der spätestens seit dem <a href="http://blog.facebook.com/blog.php?post=59195087130">letzten Redesign</a> das zentrale Feature von Facebook geworden zu sein scheint. Mit der <em>Open Stream API</em> führt Facebook diese Strategie fort und öffnet die Aktivitäten auch für externe Applikationen und Services. Besonders lobenswert ist, dass Facebook neben einer proprietären API (zum lesen und schreiben) auch einen <em>Atom-Feed+Activity Extension</em><a href="http://notiz.blog/2009/04/29/facebooks-open-strategyfacebooks-open-strategy/#open-facebook-1"><sup>1</sup></a> zum weiterverarbeiten des <em>Activity Streams</em> anbietet. Leider ist aber auch der Atom-Feed über den Facebook-Authentifizierungsprozess geschützt und kann dadurch nicht ohne weiteres mit z.B. einem Feedreader abonniert werden.

Dass Facebook die proprietäre <em><a href="http://wiki.developers.facebook.com/index.php/Using_the_Open_Stream_API">Open Stream API</a></em> entwickelt, statt die OpenSocial RESTFul API einzusetzen ist leider zu verstehen, immerhin ist OpenSocial als Googles Antwort auf die Facebook-Apps entstanden. Schade!

<h4>OpenID Login</h4>

<a href="http://notsorelevant.com/2009-02-06/facebook-is-on-the-board-and-now/">Als Facebook letztes Jahr der OpenID-Foundation beigetreten ist</a>, um sie speziell in Sachen Usability/User Experience zu unterstützt, hatte ich natürlich große Hoffnung, dass Facebook in naher Zukunft auch selbst auf OpenID umstellen würde. Seit Montag ist jetzt klar, <a href="http://www.insidefacebook.com/2009/04/27/facebook-announces-users-will-soon-be-able-to-login-to-facebook-with-an-openid/">dass Facebook an einem OpenID-Login arbeitet</a>, der hoffentlich auch irgendwann ein fester Bestandteil von Facebook-Connect wird.

Aber Facebook wäre nicht Facebook, wenn sie einfach <em>nur</em> einen klassischen OpenID-Login umsetzen würden. Wie Carsten Pötter auf SpreadOpenID beschreibt, <a href="http://spreadopenid.org/2009/04/28/facebook-will-become-a-relying-party/">plant Facebook eine Art OpenID-Auto-Discovery</a>:

<blockquote>Facebook will automatically check to see if users have logged into any OpenID account when they hit Facebook.com, and give them the option to automatically login to Facebook without entering new information.</blockquote>

Leider ist dieses Feature, wohl nicht global für alle OpenID-Provider und definitiv nicht ohne <em>Directed Identity</em> möglich... aber man wird sehen (vielleicht spinn ich hier im Blog demnächst mal ein paar Szenarien (Worst-Cases) durch).

<hr class="footnote gloss" />

<small><sup id="open-facebook-1">1</sup> Die <a href="http://martin.atkins.me.uk/specs/activitystreams/atomactivity"><em>Atom Activity Extensions</em></a> erweitert die <a href="http://www.atomenabled.org/developers/syndication/">Atom Spezifikation</a> um eine Aktivitäten-Syntax. Die Idee entstand im Rahmen des DiSo-Projekts und wird unter anderem auch schon von <a href="http://www.myspace.com">MySpace</a> und <abbr title="Your Internet ID"><a href="http://www.yiid.com/">YIID</a></abbr> unterstützt. Darauf werde ich demnächst sicherlich noch etwas detaillierter eingehen.</small>