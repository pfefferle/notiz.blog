---
ID: 4039
post_title: oAlternative
author: Matthias Pfefferle
post_date: 2011-11-15 02:07:50
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2011/11/15/oalternative/
published: true
---
Was das OpenWeb so kompliziert macht ist das Wörtchen "<strong>alternativ</strong>"!

<ul>
<li>OpenID Discovery basiert auf Meta-Tags, <strong>alternativ</strong> funktioniert aber auch XRDS(-Simple)/Yadis oder Webfinger.</li>
<li>OpenID stellt über SREG Profilinformationen bereit, <strong>alternativ</strong> aber auch über Attribute Exchange.</li>
<li> RDFa 1.1 ist folgendermaßen aufgebaut:
<pre><code>&lt;html
  prefix="foaf: http://xmlns.com/foaf/0.1/"
  &gt;
  ...
  &lt;span property="foaf:name">John Doe&lt;/span&gt;
  ...
&lt;/html&gt;</code></pre>

<strong>alternativ</strong> aber auch:

<pre><code>&lt;div vocab="http://xmlns.com/foaf/0.1/" about="#me"&gt;
  &lt;span property="name">John Doe&lt;/span&gt;
&lt;/div&gt;</code></pre>

...oder:

<pre><code>&lt;div profile="http://xmlns.com/foaf/0.1/" about="#me"&gt;
  &lt;span property="foaf:name">John Doe&lt;/span&gt;
&lt;/div&gt;</code></pre>
</li>
<li>OpenSocial, oEmbed, ActivityStrea.ms und host-meta benutzen JSON, <strong>alternativ</strong> aber auch XML</li>
<li>OAuth verschlüsselt mit HMAC-SHA1, <strong>alternativ</strong> aber auch mit RSA-SHA1 oder PLAINTEXT</li>
</ul>
To be continued...

Wie viel Komplexität man sich sparen könnte wenn man sich auf eine Variante beschränken würde.