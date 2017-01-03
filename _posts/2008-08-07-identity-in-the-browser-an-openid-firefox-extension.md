---
ID: 1038
post_title: 'Identity In The Browser &#8211; an OpenID Firefox Extension'
author: Matthias Pfefferle
post_date: 2008-08-07 09:10:41
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/08/07/identity-in-the-browser-an-openid-firefox-extension/
published: true
aktt_tweeted:
  - "1"
---
<img src="http://notiz.blog/wp-content/uploads/2008/08/add-ons.jpg" alt="Add-ons.jpg" border="0" width="482" height="225" />

Gestern veröffentlichte Vidoop eine erste Version ihrer <em><a href="http://labs.vidoop.com/2008/08/06/developer-preview-identity-in-the-browser-idib/">Identity In The Browser</a></em>-Extension für den <a href="http://wiki.mozilla.org/Firefox3">Firefox 3</a>. <abbr title="Identity In The Browser">IDIB</abbr> ist OpenSource und soll die <a href="http://openid.net">OpenID</a>-Verarbeitung, speziell in den Punkten Sicherheit und Browser-Redirects, verbessern.

Die derzeitige Version des Addons bietet folgende Möglichkeiten:
<ul>
<li>we help to reduce or eliminate browser-based redirects typically involved in authenticating against identity providers</li>
<li>we add security to reduce the potential for phishing/man-in-the-middle attacks</li>
</ul>

Mit <abbr title="Identity In The Browser">IDIB</abbr> möchte Vidoop einen Anfang machen, um die Kommunikation zwischen Mozilla und OpenID wieder anzutreiben:

<blockquote cite="http://labs.vidoop.com/2008/08/06/developer-preview-identity-in-the-browser-idib/">It was almost two years ago when the Firefox 3.0 roadmap was <a title="Firefox 3.0 Requirements are out" href="http://radar.oreilly.com/2007/01/firefox-30-requirements-are-ou.html" target="_blank">announced</a> and OpenID was mentioned as a new component to the platform. The Mozilla Firefox team looked to members of the OpenID community to step up and provide guidance on what exactly we imagined identity in the browser looking like, but we failed to mobilize and answer their call.</blockquote>

Leider benötigt das Addon einige kleine Erweiterungen (<a href="http://code.google.com/p/idib/wiki/RelyingPartyImplementation">Relying Parties</a>) zum aktuellen OpenID-Standard, die alle im <a href="http://code.google.com/p/idib/wiki/RelyingPartyImplementation">Entwickler-Wiki</a> dokumentiert sind... 

(Da <a href="http://willnorris.com/">Will Norris</a> (der Entwickler des <a href="http://wordpress.org/extend/plugins/openid/">OpenID-Plugins für WordPress</a>) aktuell für Vidoop arbeitet, sollte es aber nicht all zu lange dauern bis eine erste, angepasste Version seinen Plugins erhältlich ist.)