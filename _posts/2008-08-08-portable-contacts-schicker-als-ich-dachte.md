---
ID: 1046
post_title: >
  Portable Contacts (schicker als ich
  dachte)
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/08/08/portable-contacts-schicker-als-ich-dachte/
published: true
post_date: 2008-08-08 11:51:35
---
<!-- wp:paragraph -->
<p>In der aktuellen Folge (<a href="http://www.thesocialweb.tv/blog/2008/08/episode-5-the-p.html">Episode 5: The Portable Contacts Initiative</a>) sprechen John McCrea, Joseph Smarr und Chris Messina über das <a href="http://portablecontacts.net/"><em>Portable Contacts</em></a> - Projekt über welches ich <a href="https://notiz.blog/2008/06/30/wie-viel-portabilitiy-brauchen-wir-noch/">vor kurzem</a> noch so gescholten habe... Und ich muss sagen, ich hatte unrecht! Ich glaube kleine Gruppen mit dem Fokus auf ein spezielles Problem können wesentlich effektiver arbeiten als eine so große und über die ganze Welt verstreute Organisation wie <a href="http://dataportability.org">DataPortability</a> (da wird wohl auch die <a href="http://liako.biz/2008/07/the-dataportability-governance-framework-a-template/">Steering Group</a> nichts ändern können... aber man wird sehen).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Die (<a href="http://portablecontacts.net/draft-spec.html">Portable Contacts (1.0 Draft B)</a> - Spezifikation basiert auf sehr vielen aus dem DataPortability - Umfeld bekannten Techniken wie z.B. <a href="http://xrds-simple.net/">XRDS-Simple</a> als Discovery-Service und <a href="http://oauth.net">OAuth</a> für die Authentifizierung.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Was mir besonders gefällt, ist das <a href="http://portablecontacts.net/draft-spec.html#schema">Contacts Schema</a> welches hauptsächlich auf dem (<a href="http://portablecontacts.net/draft-spec.html#schema">wenn auch etwas abgeänderten</a>) <a href="http://tools.ietf.org/html/rfc2426">vCard-Standard</a> basiert und fehlende Felder von anderen Standards wie z.B. <a href="http://code.google.com/apis/opensocial/docs/0.8/restfulspec.html">OpenSocial</a> übernommen wurden. Dass es auch anders geht, hat z.B. das <a href="https://notiz.blog/2007/11/04/hcard-als-attribute-exchange-fuer-openid/">AX-Schema</a> bewiesen...</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>Die Verbindung zu Microformats</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Schade dass die vCard nicht zu 100% übernommen wurde... sonst hätte man ohne größere Änderungen auch die JSON-Serialisierte hCard (<a href="http://microformats.org/wiki/jCard">jCard</a>) in den Prozess integrieren können. Spannend wäre es vor allem für Services wie Twitter, die das Freundesnetzwerk sowieso mit <a href="http://microformats.org/wiki/hCard">hCards</a> auszeichnen.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Vergleich:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong><a href="http://microformats.org/wiki/jCard">jCard</a></strong></p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>{
  "fn" : "Max Mustermann",
  "email":
    [{
      "value": "max@example.com",
      "type": ["work"],
    }]
}</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p><strong><a href="http://portablecontacts.net/draft-spec.html#anchor19">Portable Contacts 1.0 Draft B</a></strong></p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>{
  "name" : "Max Mustermann",
  "emails":
    [{
      "value": "max@example.com",
      "type": "work",
    }]
}</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Man erkennt zumindest eine Ähnlichkeit :)</p>
<!-- /wp:paragraph -->