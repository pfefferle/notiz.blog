---
ID: 1320
post_title: OpenID für Flock
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/12/02/openid-fuer-flock/
published: true
post_date: 2008-12-02 21:54:19
---
<!-- wp:paragraph -->
<p>Bei Vidoop hab ich gerade von dem neuen <a href="http://blog.vidoop.com/2008/12/identity-in-the-browser-takes-a-big-step-forward/">OpenID Plugin für Flock</a> gelesen. Das Plugin ist eine Zusammenarbeit zwischen Vidoop, MySpace und Flock und basiert auf dem Know-How des <strong><a href="https://notiz.blog/2008/08/07/identity-in-the-browser-an-openid-firefox-extension/"><abbr title="Identity in the Browser">IDIB</abbr> (Identity in the Browser) Plugins</a></strong> für den Firefox.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ähnlich wie bei <abbr title="Identity in the Browser">IDIB</abbr> für Firefox kann man auch bei der Flock Version mehrere OpenIDs voreinstellen. Neu beim Flock-Plugin ist die Automatische Erkennung von <em>OpenID Providern</em> und <em>OpenID Relying Parties</em>. Besuchte <em>OpenID Profider</em> wie z.B. Yahoo! oder MySpace merkt sich das Plugin und schlägt sie unter "Suggested OpenID's" vor.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/12/flock-openid-config.png" alt="Flock-openid-config.png" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><em>OpenID Consumer</em> oder <em>Relying Parties</em> werden wohl nur noch am Login-Feld <code>&lt;input id="openid_identifier" /></code> und nicht mehr (wie bei <abbr title="Identity in the Browser">IDIB</abbr>) über <a href="http://code.google.com/p/idib/wiki/RelyingPartyImplementation">XRDS-Simple</a> erkannt. Ist ein OpenID Login möglich, werden einem die vorher angelegten OpenIDs angeboten und man kann sich bequem über das Plugin anmelden.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2008/12/flock-openid-login.png" alt="Flock-openid-login.png" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Für die Audio-Visuellen unter euch gibt es auch noch eine kurze Einführung per ScreenCast.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Download OpenID Plugin: <a href="https://extensions.flock.com/extensions/">https://extensions.flock.com/extensions/</a></p>
<!-- /wp:paragraph -->