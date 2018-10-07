---
ID: 1356
post_title: OpenID vs. Facebook Connect
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/12/11/openid-vs-facebook-connect/
published: true
post_date: 2008-12-11 14:54:08
---
Seit dem Start von <em>Facebook Connect</em> wurde das proprietäre System immer wieder mit OpenID verglichen. Dass OpenID im direkten Vergleich den kürzeren zieht ist klar, immerhin handelt es sich bei dem offenen Standard "nur" um ein <strong>Single-Sign-On</strong> System und nicht, wie bei <em>Facebook Connect</em>, um ein umfassende Komplettlösung.

Wie Marc Canter schon vor einigen Tagen bemerkt hat sollte OpenID eher als ein kleines Teil des "<strong>Identity Puzzles</strong>" ansehen:

<blockquote>...that OpenID is NOT a full solution - it is an important piece of the identity puzzle ... but OpenID can - <strong>actually solve all these issues</strong> - by embracing other complementary technologies (like oAuth, OpenSocial, Portable Contacts, microformats, FOAF and RSS/Atom) to create a <em>wrapper solution oriented approach </em>- focused on simplifying the the whole ID conundrum for end-users.&nbsp; Barriers of entry, usability issues and confusing messages can all be solved by OpenID positioning itself as a single point-of-contact solution.</blockquote>

Warum aber so viele kleine Standards und nicht einfach <em>OpenID</em> zum <em>Open Connect</em> aufblasen?
OpenID in seiner jetzigen Form hält den <em><a href="https://notiz.blog/2008/09/23/one-stack-to-access-them-all/">Open Stack</a></em> dezentral und macht die Komponenten austauschbar:

<ul><li>Jeder der oben genannten Standards ist sowohl alleine als auch in Kombination nutzbar, was den Entwicklungsaufwand für Spezialfälle vereinfacht. Braucht eine Community eine Single-Sign-On Lösung, ist auch nur ein OpenID in seiner jetzigen (unaufgeblasenen) Form nötig. Steigen nachträglich die Anforderungen, kann der <em>Stack</em> beliebig erweitert werden.</li>
<li>Bestehende Informationen können (wenn eine entsprechende Schnittstelle besteht) wiederverwendet werden und müssen nicht alle über ein System bereitgestellt werden, der <em>OpenID Provider</em> muss nur wissen wo diese Informationen zu finden sind. (Ein schönes Beispiel für ein solches dezentrales System ist die <a href="https://notiz.blog/2008/10/04/openid-xrds-simple-oauth-und-portable-contacts-perfekt-kombiniert/">OpenID + PortableContacts Beispiel-Implementierung von JanRain</a>)</li>
<li>Die Komponenten des <em>Open Stack</em> sind beliebig austauschbar. Es ist prinzipiell egal ob man den <em>Sozialen Graphen</em> über <em>XFN</em>, <em>FoaF</em> oder <em>Portable Contacts</em> importiert oder alle Varianten unterstützt.</li></ul>

Das vorgestern angekündigte <a href="http://mrtopf.de/blog/en/myspaceid-and-the-myspace-open-platform-arrived-at-developermyspacecom/">MySpaceID</a> (<abbr title="also known as">aka</abbr> <a href="https://notiz.blog/2008/08/15/dataavailability-doch-offener-als-gedacht/">Data Availability</a>) scheint ein erster Schritt in Richtung <em>Open Stack</em> zu sein und auch Googles <a href="http://www.neunetz.com/2008/12/04/facebook-connect-eine-win-win-situation/#comment-4201372">Friend Connect ist auf einem guten Weg</a>. Es gibt sicherlich noch einiges zu tun um die Bausteine etwas besser miteinander zu verbinden (z.B. <a href="http://code.google.com/p/step2/">OpenID und OAuth zu kombinieren</a>) aber ich bin weiterhin optimistisch und glaube dass sich der offene und dezentrale Ansatz durchsetzen wird.