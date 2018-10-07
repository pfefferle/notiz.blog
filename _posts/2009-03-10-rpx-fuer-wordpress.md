---
ID: 1424
post_title: RPX für WordPress
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/03/10/rpx-fuer-wordpress/
published: true
post_date: 2009-03-10 20:23:09
---
<!-- wp:paragraph -->
<p><a href="http://rpxnow.com/">RPX</a> ist ein SingleSignOn-Service von <a href="http://www.janrain.com">JanRain</a> (der Firma hinter <a href="http://myopenid.com">myOpenID</a>) welcher alle gängigen SignOn-Mechanismen wie z.B. <a href="https://notiz.blog/tag/openid">OpenID</a>, <a href="https://notiz.blog/2008/12/11/openid-vs-facebook-connect/">Facebook-Connect</a>, <a href="https://notiz.blog/2008/08/15/dataavailability-doch-offener-als-gedacht/">MySpaceID</a> oder <a href="https://notiz.blog/2008/10/27/windows-live-id-wird-openid-provider/">Microsofts Live ID</a> in einem Dienst vereint. Der Vorteil für Webseiten-Betreiber liegt in der, für sie einheitlichen, Verarbeitung der verschiedenen offenen Standards und proprietären Formate. Der Login wird praktisch komplett an RPX weiter delegiert und die ganze Logik läuft über die Server von JanRain. Nach erfolgreicher Authentifizierung bekommt der Betreiber dann alle Informationen (bei OpenID z.B. Profil-Daten die per SReg übertragen wurden) in einheitlicher Form übermittelt... "SingleSignOn as a Service" so zu sagen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Mit dem <a href="http://wordpress.org/extend/plugins/rpx/">Plugin für WordPress</a> sind all diese Features jetzt auch für den privaten Blog nutzbar.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1425,"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2009/03/rpx-wordpress-login.png" alt="rpx-wordpress-login" class="wp-image-1425" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Das Plugin ist sicherlich ein genialer Marketing-Coup um RPX zu promoten, bietet für mich aber (außer dem breiten Spektrum an Login-Möglichkeiten) keine wirkliche Alternative zu dem klassischen <a href="http://wordpress.org/extend/plugins/openid/">OpenID-Plugin von Will Norris</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Was mich an RPX besonders stört:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li>Für jeden der sich beim Kommentieren über RPX authentifiziert wird ein WordPress-Profil angelegt, auch wenn die Registrierung für WordPress deaktiviert wurde.</li>
	<li>Der ganze Login-Prozess wird über JanRain abgehandelt, was ja eigentlich auch nicht der Idee von OpenID entspricht. "Man in the middle" mit Ansage!</li>
	<li>Man muss sich zuerst relativ umständlich bei RPX registrieren um einen API-Key zu bekommen</li>
</ul>
<!-- /wp:list -->