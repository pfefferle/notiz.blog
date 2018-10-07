---
ID: 636
post_title: hCard als Attribute Exchange für OpenID
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/11/04/hcard-als-attribute-exchange-fuer-openid/
published: true
post_date: 2007-11-04 21:34:03
---
<!-- wp:image {"align":"right"} -->
<div class="wp-block-image"><figure class="alignright"><img src="https://notiz.blog/wp-content/uploads/2007/11/openid.png" alt="OpenID Logo"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>"OpenID ist ein dezentrales System zur Identifizierung" (<a href="http://de.wikipedia.org/wiki/OpenID">WikiPedia</a>).<br/>
	<a href="http://openid.net/">OpenID</a> bietet die Möglichkeit, Login Daten an zentraler Stelle anzugeben und diese als Authentifizierung für andere Webseiten zu verwenden. <a href="http://openid.net/specs/openid-simple-registration-extension-1_0.html">Simple Registration Extension</a> (kurz SREG) ist eine Erweiterung zu der OpenID Authentifizierung, der einen simplen Profil-"Austausch" erlaubt.<br/> SREG ist, wie der Name schon sagt, "nur" ein Simples Format, deshalb wurde eine Erweiterung mit dem Namen <a href="http://openid.net/specs/openid-attribute-exchange-1_0-07.html">Attribute Exchange</a> (AX), welches wesentlich mehr Informationen beinhaltet, entwickelt.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="http://factoryjoe.com/">Chris Messina</a> stellt sich in seinem Artikel "<a href="http://factoryjoe.com/blog/2007/11/01/hcard-for-openid-simple-registration-and-attribute-exchange/">hCard for OpenID Simple Registration and Attribute Exchange</a>" die Frage warum bei der Definition der ersten <a href="http://www.axschema.org/types/"><abbr title="Attribute Exchange">AX</abbr>-Typen</a> (genauso wie bei SREG) versucht wird, Profil-Daten neu zu definieren, anstatt auf bestehende Standards wie die vCard (<a href="http://tools.ietf.org/html/rfc2426">RFC2426</a>) zurück zu greifen. Er argumentiert sein Anliegen mit der weiten Verbreitung der vCard und seines XHTML Pendants der <a href="http://microformats.org/wiki/hCard">hCard</a>:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote"><p>Most importantly, however, hcard and vcard is already widely supported in existing applications like Outlook, Mail.app and just about every mobile phone on the planet and in just about any other application that exchanges profile data.</p></blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Chris hat sich die Mühe gemacht, die drei Standards einander gegenüber zu stellen:<br/></p>
<!-- /wp:paragraph -->

<!-- wp:more -->
<!--more-->
<!-- /wp:more -->

<!-- wp:table -->
<table class="wp-block-table"><thead><tr><th>Attribute</th><th>SREG</th><th>AX</th><th>vCard</th></tr></thead><tbody><tr><th>Nickname</th><td><code>nickname</code></td><td><code>namePerson/friendly</code></td><td><code>nickname</code></td></tr><tr><th>Full Name</th><td><code>fullname</code></td><td><code>namePerson</code></td><td><code>n (family-name, given-name)</code> <a href="http://microformats.org/wiki/hcard#Implied_.22n.22_Optimization%22">or</a> <code>fn</code></td></tr><tr><th>Birthday</th><td><code>dob</code></td><td><code>birthDate</code></td><td><code>bday</code></td></tr><tr><th>Gender</th><td><code>gender</code></td><td><code>gender</code></td><td><code>gender</code></td></tr><tr><th>Email</th><td><code>email</code></td><td><code>contact/email</code></td><td><code>email</code></td></tr><tr><th>Postal Code</th><td><code>postcode</code></td><td><code>contact/postalCode/home</code></td><td><code>postal-code</code></td></tr><tr><th>Country</th><td><code>country</code></td><td><code>contact/country/home</code></td><td><code>country-name</code></td></tr><tr><th>Language</th><td><code>language</code></td><td><code>pref/language</code></td><td>N/A</td></tr><tr><th>Timezone</th><td><code>timezone</code></td><td><code>pref/timezone</code></td><td><code>tz</code></td></tr><tr><th>Photo</th><td>N/A</td><td><code>media/image/default</code></td><td><code>photo</code></td></tr><tr><th>Company</th><td>N/A</td><td><code>company/name</code></td><td><code>org</code></td></tr><tr><th>Biography</th><td>N/A</td><td><code>media/biography</code></td><td><code>note</code></td></tr><tr><th>URL</th><td>N/A</td><td><code>contact/web/default</code></td><td><code>URL</code></td></tr></tbody></table>
<!-- /wp:table -->

<!-- wp:paragraph -->
<p><ins>Update: Chris Messina hat eine vollständige Liste der Attribute im <a href="http://microformats.org/wiki/attribute-exchange">Microformats Wiki</a> erstellt.</ins></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><abbr title="Attribute Exchange">AX</abbr> und vCard/hCard haben zwar weitestgehend die gleichen Attribute, unterscheiden sich jodoch in der Bezeichnung, was es Entwicklern unnötig schwer macht, die verschiedenen Formate zu implementieren.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="http://tantek.com/">Tantek Çelik</a> (einer der Microformats Ur-Väter) beschäftigt sich weiter mit dem Problem und <a href="http://tantek.com/log/2007/11.html#d02t2318">definiert mögliche Schritte</a> um die hCard als Attribute Exchange für OpenID zu verwenden:</p>
<!-- /wp:paragraph -->

<!-- wp:quote -->
<blockquote class="wp-block-quote"><p><strong>URLs for properties.</strong> Every SREG property has a URL in its Attribute Exchange (AX) version that defines that property. hCard does too, through the hCard profile. However, there are two differences which may be seen as shortcomings. Currently the hCard profile on microformats.org is in a wiki, and not proper XMDP (there is an hCard XMDP profile at W3C that some are using), and, URLs for specific properties use # fragment identifiers.</p></blockquote>
<!-- /wp:quote -->

<!-- wp:paragraph -->
<p>Soweit ich das ganze verstanden habe ist AX sowieso eine weitgehend offene Definition, welche es ermöglicht Typen über URIs zu definieren. D.h. es sollte möglich sein z.B. den vCard/hCard-Typ <code>fn</code> folgendermassen zu implementieren:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>openid.ax.type.fn=http://microformats.org/profile/hcard#fn</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Bitte korrigiert mich falls ich etwas falsch verstanden habe.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ich finde die Idee, Microformats für OpenID einzusetzen, sehr gut und bin generell für die Nutzung von offenen Standards. Je höher die Wiederverwendbarkeit von Standards, desdo geringer der ist die Barriere sie einzusetzen. Jeder der schon mehr als ein fremdes System über eine proprietäre API angebunden hat wird mir da sicher zustimmen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Weiterführende Informationen:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul>
	<li><a href="http://microformats.org/wiki/openid-brainstorming">OpenID Brainstorming im Microformats Wiki</a></li>
</ul>
<!-- /wp:list -->