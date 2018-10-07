---
ID: 1177
post_title: >
  OpenID, XRDS-Simple, OAuth und Portable
  Contacts perfekt kombiniert
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/10/04/openid-xrds-simple-oauth-und-portable-contacts-perfekt-kombiniert/
published: true
post_date: 2008-10-04 14:22:21
---
<!-- wp:paragraph -->
<p>Nach der Demo von Brian Ellin auf dem <a href="https://notiz.blog/2008/09/11/portablecontacts-hacks/">Portable Contacts</a> Summit...</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
    <p>Brian Ellin of JanRain has successfully combined OpenID, XRDS-Simple, OAuth, and the Portable Contacts API to start showing how each of these building blocks should come together.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>und der <a href="https://notiz.blog/2008/09/18/interessante-portable-contacts-ankuendigungen/">Ankündigung</a>, <em>Portable Contacts</em> in myOpenID zu integrieren...</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
    <p>Portable Contacts is an emerging standard for transferring profile data and social connections across websites. Look for upcoming support of this new standard in myOpenID!</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>...habe ich endlich auch eine <a href="http://portablecontactsdemo.janrain.com/">funktionierende Demo</a> im Web gefunden. Notwendig für die Testanwendung sind ein <a href="https://www.myopenid.com/signup">myOpenID Profil</a> und ein <a href="https://www.plaxo.com/signup">Plaxo-Account</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Zuerst muss man über den <a href="https://www.myopenid.com/settings_pcp">myOpenID Einstellungen</a> Plaxo als seinen <em>Portable Contacts - Provider</em> angeben,</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/09/openid-porc.jpg" alt="openid-porc.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>sich mit seiner OpenID an der Demoseite anmelden,</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/10/openid-with-portable-contacts-demo.png" alt="" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>den Zugriff auf die eigenen Daten gewähren</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/10/plaxo-pulse.jpg" alt="Plaxo Pulse.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>und die Demo-Anwendung bekommt meine Kontakte übermittelt.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/10/openid-with-portable-contacts-demo.jpg" alt="OpenID with Portable Contacts Demo.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Im besten Fall laufen diese Schritte völlig automatisch ab und der Anwender hat nicht mehr zu tun als seine Einverständniserklärung per Knopfdruck zu geben. Ein schöner Anwendungsfall für dieses Beispiel wäre z.B. eine OpenID-Neuanmeldung bei einer Community mit anschließendem Import aller Kontakte.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Was ich an diesem Beispiel außerdem sehr schätze ist, dass JanRain die <em>Portable Contacts API</em> in seinen OpenID-Provider integriert hat ohne sie wirklich integriert zu haben... Der Fokus von myOpenID bleibt weiterhin auf OpenID und die <em>Portable Contacts</em> Anfragen werden <em>lediglich</em> <a href="http://portablecontacts.net/draft-spec.html#discovery">über XRDS-Simple</a> an z.B. Plaxo weiterdelegiert.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>So zentral kann dezentral sein :)</p>
<!-- /wp:paragraph -->