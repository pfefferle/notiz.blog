---
ID: 15292
post_title: OpenID Connect Federation
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2018/02/14/openid-connect-federation/
published: true
post_date: 2018-02-14 21:45:32
---
Irgendwann letzte oder vorletzte Woche ist die Überschrift "OpenID Connect Federation 1.0 - draft XX" in meinem Feed-Reeder aufgetaucht und auf Buzz-Words wie <strong>Federation</strong> o. Ä. springe ich natürlich immer noch sofort auf!

Spezifikationen lesen, macht ja generell nicht viel Spaß, aber bei der <em><a href="http://openid.net/specs/openid-connect-federation-1_0.html"><strong>OpenID Connect Federation 1.0</strong></a></em> kam ich nicht mal bis zur Hälfte. Bevor man wirklich versteht was das Protokoll eigentlich macht (für mich hört es sich ähnlich an wie <a href="https://openid.net/specs/openid-connect-registration-1_0.html"><strong>OpenID Connect Dynamic Client Registration</strong></a>), geht es um Metadaten, <a href="https://tools.ietf.org/html/rfc7515">JSON Web Signature (JWS)</a>, JSON Web Tokens (JWT) und <a href="https://tools.ietf.org/html/rfc7517">JSON Web Keys (JWK)</a>.

Eigentlich dachte ich, dass <em>OpenID Connect</em> durch <em>OAuth 2</em> super simpel sein soll... Immerhin basiert ja <em>OAuth 2</em> auf SSL/TLS und nicht wie <em>OAuth 1</em> auf komplizierte Signaturen.

<blockquote>
    <p>The majority of failed OAuth 1.0 implementation attempts are caused by the complexity of the cryptographic requirements of the specification. The fact that the original specification was poorly written didn’t help, but even with the newly published <a href="http://tools.ietf.org/html/rfc5849">RFC 5849</a>, OAuth 1.0 is still not trivial to use on the client side. The convenient and ease offered by simply using passwords is sorely missing in OAuth.</p><cite><a href="https://hueniverse.com/introducing-oauth-2-0-b5681da60ce2">Eran Hammer﻿</a></cite></blockquote>

Die OpenID Foundation scheint ihre Meinung geändert zu haben... SSL scheint wohl doch nicht auszureichen.

<blockquote>
    <p>Another problem that has been raised is the dependency on TLS as the sole protection against attacks on the transferred information. These last couple of years a number of problems with OpenSSL, which is probably the most widely used TLS library, have been discovered that put reasonable doubt into this dependency.</p><cite> <a href="https://openid.net/specs/openid-connect-registration-1_0.html">OpenID Connect Dynamic Client Registration</a></cite></blockquote>

Schade, schade...

Wer eine wirkliche Alternative zu <em>OpenID Connect</em> sucht, der soll sich mal <a href="https://www.w3.org/TR/indieauth/"><strong>IndieAuth</strong></a> anschauen. <strong>IndieAuth</strong> kommt der ursprünglichen Idee von <a href="https://web.archive.org/web/20100609191041/http://openidconnect.com:80/"><em>OpenID Connect</em></a> sehr nahe und ist relativ einfach zu verstehen und auch zu implementieren!