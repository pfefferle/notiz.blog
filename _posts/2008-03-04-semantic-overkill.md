---
ID: 766
post_title: Semantic Overkill
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/03/04/semantic-overkill/
published: true
post_date: 2008-03-04 20:40:47
---
<!-- wp:paragraph -->
<p>Wer sich nicht zwischen RDFa und Microformats entscheiden kann und nicht sehr viel von dem Transformation-System <abbr title="Gleaning Resource Descriptions from Dialects of Languages">GRDDL</abbr> hält, kann seine HTML Inhalte natürlich auch mit beiden Formaten auszeichnen. Gerade die Profil- und Kalender-Semantiken bieten sich wegen ihrer Ähnlichkeit besonders an.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="http://microformats.org/wiki/hCard">hCard</a> und RDFa vCard:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;body xmlns:contact="http://www.w3.org/2001/vcard-rdf/3.0#">
  &lt;div class="vcard">
    &lt;span class="fn" property="contact:fn">Max Mustermann&lt;/span>
    &lt;a class="email" rel="contact:email" href="mailto:max.mustermann@example.org">
      max.mustermann@example.org
    &lt;/a>
    &lt;div class="adr" property="contact:adr">
      &lt;span class="street-address" property="contact:street">Street&lt;/span>
      &lt;span class="country-name" property="contact:country">Country&lt;/span>
    &lt;/div>
  &lt;/div>
&lt;/body></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>...oder <a href="http://microformats.org/wiki/hCal">hCalendar</a> und RDFa iCalendar:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;body xmlns:cal="http://www.w3.org/2002/12/cal/ical#">
  &lt;div class="vevent" instanceof="cal:Vevent">
    &lt;span class="summary" property="cal:summary">Ein Event&lt;/span>
    &lt;span property="cal:dtstart" content="20070916T1600-0500">
      &lt;abbr class="dtstart" title="20070916T1600-0500">
        September 16th at 4pm.
      &lt;/abbr>
    &lt;/span>
  &lt;/div>
&lt;/body></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Legende: Microformats bzw. RDFa</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>So, als nächstes schau ich mir mal die RDFa Attribute näher an...</p>
<!-- /wp:paragraph -->