---
ID: 1177
post_title: >
  OpenID, XRDS-Simple, OAuth und Portable
  Contacts perfekt kombiniert
author: Matthias Pfefferle
post_date: 2008-10-04 14:22:21
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/10/04/openid-xrds-simple-oauth-und-portable-contacts-perfekt-kombiniert/
published: true
aktt_tweeted:
  - "1"
---
Nach der Demo von Brian Ellin auf dem <a href="http://notiz.blog/2008/09/11/portablecontacts-hacks/">Portable Contacts</a> Summit...

<blockquote>Brian Ellin of JanRain has successfully combined OpenID, XRDS-Simple, OAuth, and the Portable Contacts API to start showing how each of these building blocks should come together.</blockquote>

und der <a href="http://notiz.blog/2008/09/18/interessante-portable-contacts-ankuendigungen/">Ankündigung</a>, <em>Portable Contacts</em> in myOpenID zu integrieren...

<blockquote>Portable Contacts is an emerging standard for transferring profile data and social connections across websites. Look for upcoming support of this new standard in myOpenID!</blockquote>

...habe ich endlich auch eine <a href="http://portablecontactsdemo.janrain.com/">funktionierende Demo</a> im Web gefunden. Notwendig für die Testanwendung sind ein <a href="https://www.myopenid.com/signup">myOpenID Profil</a> und ein <a href="https://www.plaxo.com/signup">Plaxo-Account</a>.

Zuerst muss man über den <a href="https://www.myopenid.com/settings_pcp">myOpenID Einstellungen</a> Plaxo als seinen <em>Portable Contacts - Provider</em> angeben,

<img src="http://notiz.blog/wp-content/uploads/2008/09/openid-porc.jpg" alt="openid-porc.jpg" width="480" height="200" class="aligncenter" />

sich mit seiner OpenID an der Demoseite anmelden,

<img src="http://notiz.blog/wp-content/uploads/2008/10/openid-with-portable-contacts-demo.png" alt="" width="480" height="320" class="aligncenter" />

den Zugriff auf die eigenen Daten gewähren

<img src="http://notiz.blog/wp-content/uploads/2008/10/plaxo-pulse.jpg" alt="Plaxo Pulse.jpg" border="0" width="480" height="200" class="aligncenter" />

und die Demo-Anwendung bekommt meine Kontakte übermittelt.

<img src="http://notiz.blog/wp-content/uploads/2008/10/openid-with-portable-contacts-demo.jpg" alt="OpenID with Portable Contacts Demo.jpg" width="480" height="484" class="aligncenter" />

Im besten Fall laufen diese Schritte völlig automatisch ab und der Anwender hat nicht mehr zu tun als seine Einverständniserklärung per Knopfdruck zu geben. Ein schöner Anwendungsfall für dieses Beispiel wäre z.B. eine OpenID-Neuanmeldung bei einer Community mit anschließendem Import aller Kontakte.

Was ich an diesem Beispiel außerdem sehr schätze ist, dass JanRain die <em>Portable Contacts API</em> in seinen OpenID-Provider integriert hat ohne sie wirklich integriert zu haben... Der Fokus von myOpenID bleibt weiterhin auf OpenID und die <em>Portable Contacts</em> Anfragen werden <em>lediglich</em> <a href="http://portablecontacts.net/draft-spec.html#discovery">über XRDS-Simple</a> an z.B. Plaxo weiterdelegiert.

So zentral kann dezentral sein :)