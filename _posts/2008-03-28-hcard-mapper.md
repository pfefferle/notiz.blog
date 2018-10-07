---
ID: 787
post_title: hCard Mapper
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/03/28/hcard-mapper/
published: true
post_date: 2008-03-28 09:41:36
---
<!-- wp:paragraph -->
<p>...oder <em>How to use hCards to fill in forms</em>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="http://lib.omnia-computing.de/hcardmapper">hCardMapper</a> ist eine JavaScript-Klasse (basierend auf <a href="http://www.prototypejs.org/">Prototype</a>) um Kontakt- oder Profil-Formulare mit Hilfe einer hCard automatisch zu füllen, ähnlich wie bei <a href="https://www.bragster.com/signup">bragster.com</a> oder <a href="http://getsatisfaction.com/people/new">getsatisfaction.com</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Das schöne an hCardMapper ist seine flexible Struktur. Die JavaScript Klasse ist so aufgebaut, dass sie eigentlich <a href="https://notiz.blog/2007/05/24/microformats-parser/">Microformats-Parser</a> unabhängig funktionieren sollte, da sie die Daten über einen "Proxy" abfrägt. Die einzige Vorgabe ist, dass dieser Proxy eine <a href="https://notiz.blog/2007/09/16/microjson-microformats-in-json/">JSON formatierte hCard</a> (<a href="http://microjson.org/wiki/JCard">jCard</a>) zurückgibt. Das Problematische an dieser Variante ist, dass jeder Parser unterschiedliche Ergebnisse liefert... ich werde es heute abend mal mit dem <a href="http://allinthehead.com/hkit">hKit</a>-Parser testen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Ein weiter Vorteil ist die Formular-Unabhängige Programmierung die es ermöglicht, das Script auch problemlos auf vorhandene Formulare anzuwenden. Über <code>mappnings</code> werden die hCard-Attribute den entsprechenden Formular-Felder zugeordnet.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>Event.observe(window, 'load', function() {
  hcr = new com.omniacomputing.HCardMapper({
    register: true,
    proxy: '/hcardmapper/hcard?uri=',
    insertBelowEl: 'hcr-hook',
    mappings: {
      given_name: 'first',
      family_name: 'last',
      tel: {tel: 'phone', work: 'phone', cell:'phone'},
      email: 'email',
      org: {org: 'company', organization_name: 'company'},
      url: 'website',
      street_address: 'street',
      postal_code: 'zip',
      locality: 'town' 
    }
  })
});</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Quelle: <a href="http://lib.omnia-computing.de/hcardmapper">http://lib.omnia-computing.de/hcardmapper</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Tolle Idee, mal schau'n wie gut das Script mit den (oben schon erwähnten) unterschiedlichen Verarbeitungsweisen der Parser umgeht...</p>
<!-- /wp:paragraph -->