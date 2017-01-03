---
ID: 1152
post_title: WordPress wird OpenID-Provider
author: Matthias Pfefferle
post_date: 2008-09-17 23:12:18
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/09/17/wordpress-wird-openid-provider/
published: true
aktt_tweeted:
  - "1"
---
Will Norris hat vorgestern ausführlich über die neuen Features seines WordPress-Plugins berichtet. Das wohl interessanteste Feature von wp-openid 3.0 ist der neue <a href="http://willnorris.com/2008/09/providing-and-delegating-openids">OpenID-Provider</a>:

<blockquote cite="http://willnorris.com/2008/09/providing-and-delegating-openids">The next major release of wp-openid includes a built-in OpenID provider and delegation engine. This will certainly be the most exciting feature of this release for most people, so let me explain a bit how it works. Each authorized user on the WordPress blog will have an OpenID at the author posts URL (ie. http://example.com/author/admin). Authorization to use the OpenID provider is controlled based on user roles and is managed in the main OpenID settings page.</blockquote>

Das Plugin kann in zwei verschiedenen Modi betrieben werden. <em>Multi-user</em> erstellt aus jeder Autor-URL (z.B. http://example.com/author/admin/) eine OpenID während <em>blog-owner</em> für Private-Blogs mit nur einem Autor gedacht ist und die Home-URL zur OpenID (z.B. http://example.com) macht:

<blockquote>In multi-user, the default configuration, the server supports a feature in OpenID 2.0 called OpenID Provider driven identifier selection. What this means is that ANY user on that blog can enter the home URL as their OpenID, and the OpenID provider itself will make sure that the correct identifier is returned to the relying party. The final identifier will still be something like http://example.com/author/admin/, but the user only needs to enter example.com at a relying party. If you’ve used ever used Yahoo’s OpenID provider, then you’ve probably seen how this works.</blockquote>

Zwei weitere spannende Features sind die Hooks, als Schnittstelle für z.B. andere Plugins...

<blockquote>I haven’t sat down to document them all yet, but I’m adding in more hooks for other plugins to add functionality. Want to pull profile data from FOAF instead of sreg? No problem, now you have a hook you can implement. This makes everything in the plugin much more lightweight and “loosely joined” which is always good. All of the existing non-core OpenID functionality (like SREG) is currently using these hooks.</blockquote>

...und die Unterstützung des OpenID-Firefox-Plugins (welches übrigens auch mit der Version 2.x funktioniert) über das <em><a href="http://diso.googlecode.com/svn/wordpress/wp-xrds-simple/branches/refactoring/">DiSo XRDS-Simple Plugin</a></em>.

Ich habe das Plugin bisher nur einmal ausprobiert, da es noch einige kleine Fehler hat und die Admin-Oberfläche des OpenID-Providers noch gänzlich fehlt. Trotz dieser kleinen Fehler merkt man, dass sich Will Norris für diese Version sehr viel Zeit (<a href="http://factoryjoe.com/blog/2008/05/13/im-joining-vidoop-to-work-on-diso-full-time/">die er sicherlich auch hatte</a>) genommen hat und ich bin sehr gespannt auf die fertige Version.

Wer sich nochmal ausführlich mit den Features beschäftigen will, sollte unbedingt Will Norris' Artikel darüber lesen:
<ul>
<li><a href="http://willnorris.com/2008/09/the-next-steps-with-wp-openid">The Next Steps with wp-openid</a></li>
<li><a href="http://willnorris.com/2008/09/wp-openid-faster-stronger-better">Making the plugin more stable, extensible, and overall simpler</a></li>
<li><a href="http://willnorris.com/2008/09/providing-and-delegating-openids">OpenID Providing and Delegation</a></li>
</ul>