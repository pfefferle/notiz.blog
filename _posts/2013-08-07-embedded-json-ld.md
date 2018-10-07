---
ID: 5530
post_title: Embedded JSON(-LD)
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2013/08/07/embedded-json-ld/
published: true
post_date: 2013-08-07 17:01:21
---
<!-- wp:paragraph -->
<p><a href="https://developers.google.com/gmail/schemas/reference/formats/json-ld">Gmail</a> unterstützt seit ein paar Tagen auch <a href="http://json-ld.org/spec/latest/json-ld/#embedding-json-ld-in-html-documents">Embedded <abbr title="JSON for Linking Data">JSON-LD</abbr></a>... So ne Art "<a href="http://json-ld.org/spec/latest/json-ld/">JSON Version von RDF</a>" für HTML-Dokumente:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;script type="application/ld+json">
{
  "@context": "http://json-ld.org/contexts/person.jsonld",
  "@id": "http://dbpedia.org/resource/John_Lennon",
  "name": "John Lennon",
  "born": "1940-10-09",
  "spouse": "http://dbpedia.org/resource/Cynthia_Lennon"
}
&lt;/script></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Embedded JSON? Wirklich? Und warum? Weil's geht?</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Neben Microformats, Microdata, RDFa, eRDF, OpenGraph Protocol und Twitter Cards jetzt also auch noch JSON? Super Idee!</p>
<!-- /wp:paragraph -->