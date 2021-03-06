---
ID: 745
post_title: Openavatar
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/02/16/openavatar/
published: true
post_date: 2008-02-16 17:47:23
---
<!-- wp:image {"align":"right"} -->
<figure class="wp-block-image alignright"><img src="https://notiz.blog/wp-content/uploads/2008/02/openavatar-logo.png" alt="openavatar-logo.png" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>...oder "nicht noch ein Avatar System".</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Auf <a href="http://www.konterfai.com/?p=265">Pierros Weblog</a> bin ich heute auf <a href="http://www.openvatar.com/">Openavatar</a> gestossen und war von der Idee ein <a href="http://www.openid.net">OpenID</a> Bild als Avatar zu verwenden zuerst begeistert:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote">
	<p>Openvatar is your Openid avatar image (80x80). Your avatar appear beside your name when you participate (comments or other contents) on Openvatar enabled sites.</p>
</blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Beim näherem betrachten des Systems wurde ich aber sehr schnell enttäuscht. Openavatar bietet kein Plugin um ein in <a href="http://axschema.org/">OpenIDs <abbr title="Attribute Exchange">AX</abbr>-Schema</a> definiertes <a href="http://axschema.org/media/image/default/">Image</a> als Avatar anzuzeigen sondern "nur" einen Service im Stil von <abbr title="Globally Recognized Avatar">Gravatar</abbr>. Der einzige Unterschied zu dem <strong>G</strong>lobally <strong>R</strong>ecognized <strong>Avatar</strong> ist, dass anstatt der E-Mail - Adresse die OpenID URL zur Autentifizierung verwendet wird.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Beispielsweise: <code>http://www.openvatar.com/avatar.php?<br/>
openvatar_id=9b2894b2fa12ea24c455f4be9331d3fe&amp;size=50<br/>
&amp;default="http://www.mysite.com/avatar.jpg"</code></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ich habe das ganze trotzdem einmal ausprobiert und mich testweise mit meiner <a href="http://myopenid.com">myOpenID</a> <abbr title="Uniform Resource Locator">URL</abbr> angemeldet und wurde noch einmal enttäuscht. Anstatt das in meinem OpenID Profil definierte Image zu verwendet fordert mich die Webseite auf, ein weiteres Bild hochzuladen.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/02/openvatar-upload.jpg" alt="openvatar-upload.jpg" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Warum dieser Service? Eigentlich hat das System, außer für die Anmeldung, nichts mit OpenID zu tun und würde auch mit jeder x-beliebigen <abbr title="Uniform Resource Locator">URL</abbr> funktionieren. Ein Gravatar für die in OpenID verwendete E-Mail - Adresse oder ein über meinen OpenID Endpoint definiertes <a href="http://pavatar.com/"><abbr title="Personal Avatar">Pavatar</abbr></a> (wie bei <a href="https://notiz.blog/2007/12/18/myopenid-neuerungen-mit-wordpress-abbilden/">myOpenID</a>) hätte es doch auch getan.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Leider ist es trotz <a href="http://dataportability.org">DataPotablity</a> und <a href="http://www.diso-project.org">DiSo</a> immer noch sehr weit verbreitet eigene Systeme zu entwickeln, anstatt bewährte Standards aufzugreifen und darauf aufbauend sinnvolle Services/Plugins zu schaffen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ein ähnliches Problem im Zusammenhang mit proprietären Formaten beschreibt Carsten Pötter in seinem Artikel über <a href="http://www.notsorelevant.com/2008-02-15/mybloglog-supports-microformats-but-not-microid/">MyBlogLogs neue Features</a>.</p>
<!-- /wp:paragraph -->