---
ID: 638
post_title: OpenID und hCard Teil II
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/11/06/openid-und-hcard-teil-ii/
published: true
post_date: 2007-11-06 22:01:31
---
<!-- wp:paragraph -->
<p>...oder was man mit der <a href="https://www.myopenid.com/">myOpenID</a> <abbr title="Uniform Resource Locator">URL</abbr> noch so alles anstellen kann.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Carsten Pötter hat mich in <a href="https://notiz.blog/2007/11/04/hcard-als-attribute-exchange-fuer-openid/#comment-3653">einem Kommentar</a> darauf hingewiesen dass myOpenID schon ne ganze Weile die <a href="http://www.notsorelevant.com/2007-06-21/openid-as-hcards/">hCard für das "Public Profile" verwendet</a>. Das "Öffentliche Profil" ist unter der gleichen URL erreichbar wie der Authentifizierungslink, wenn man es vorher über das Admin-Interface frei schaltet.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":639,"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2007/11/public-profile.jpg" alt="" class="wp-image-639" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Das schöne an dieser Tatsache ist, dass man die URL (Beispielsweise: <code>http://mustermann.myopenid.com</code>) sowohl für die OpenID Authentifizierung, als auch über einen Profilaustausch per <a href="http://microformats.org/wiki/hcard">hCard</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ein tolles Anwendungs-Beispiel (<a href="http://www.bragster.com/signup">www.bragster.com/signup</a>) für einen hCard Import habe ich vor einigen Tagen <a href="http://twitter.com/microformats/statuses/380556902">gezwitschert</a> bekommen, ein anderes schönes Beispiel (<a href="http://getsatisfaction.com/people/new">getsatisfaction.com/people/new</a>) hat <a href="http://suda.co.uk/">Brian Suda</a> in seinem <a href="https://notiz.blog/2007/10/11/microformats-vortraege-auf-der-web-20-expo/">Microformats-Vortrag</a> auf der <a href="http://twitter.com/berlinblase/statuses/391828312">web20expo</a> erwähnt.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Beide Seiten benutzen <a href="http://microformats.org/">Microformats</a> um den Registrierungsprozess zu beschleunigen. <a href="https://www.bragster.com/signup#">Bragster</a> unterstützt einige vorgefertigten Links (Bsp.: Twitter, Last.fm, ...) oder die Möglichkeit, selbst eine Seite wählen. Jetzt muss man nur noch seine OpenID URL eintragen...</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":640,"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2007/11/login-bragster.jpg" alt="" class="wp-image-640" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>...danach werden die entsprechenden Felder (soweit vorhanden) automatisch ausgefüllt.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":641,"align":"center"} -->
<figure class="wp-block-image aligncenter"><img src="https://notiz.blog/wp-content/uploads/2007/11/reg-form.jpg" alt="" class="wp-image-641" /></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Ich bin mal gespannt, ob <a href="http://microformats.org/wiki/hCard">hCard</a> und <a href="http://openid.net/">OpenID</a> irgendwann auf einen <a href="http://willnorris.com/2007/11/try-reuse-catch-ex-reinvent">gemeinsamen</a> <a href="https://notiz.blog/2007/11/04/hcard-als-attribute-exchange-fuer-openid/">Nenner</a> kommen und welche neuen Authentifizierungs-Systeme dadurch ermöglicht werden.</p>
<!-- /wp:paragraph -->