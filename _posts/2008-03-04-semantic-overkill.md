---
ID: 766
post_title: Semantic Overkill
author: Matthias Pfefferle
post_date: 2008-03-04 20:40:47
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/03/04/semantic-overkill/
published: true
aktt_tweeted:
  - "1"
---
Wer sich nicht zwischen RDFa und Microformats entscheiden kann und nicht sehr viel von dem Transformation-System <abbr title="Gleaning Resource Descriptions from Dialects of Languages">GRDDL</abbr> hält, kann seine HTML Inhalte natürlich auch mit beiden Formaten auszeichnen. Gerade die Profil- und Kalender-Semantiken bieten sich wegen ihrer Ähnlichkeit besonders an.

<a href="http://microformats.org/wiki/hCard">hCard</a> und RDFa vCard:

<pre class="code">&lt;body <span style="color: #00f;">xmlns:contact="http://www.w3.org/2001/vcard-rdf/3.0#"</span>&gt;
  &lt;div <span style="color: #0f0;">class="vcard"</span>&gt;
    &lt;span <span style="color: #0f0;">class="fn"</span> <span style="color: #00f;">property="contact:fn"</span>&gt;Max Mustermann&lt;/span&gt;
    &lt;a <span style="color: #0f0;">class="email"</span> <span style="color: #00f;">rel="contact:email"</span> href="mailto:max.mustermann@example.org"&gt;
      max.mustermann@example.org
    &lt;/a&gt;
    &lt;div <span style="color: #0f0;">class="adr"</span> <span style="color: #00f;">property="contact:adr"</span>&gt;
      &lt;span <span style="color: #0f0;">class="street-address"</span> <span style="color: #00f;">property="contact:street"</span>&gt;Street&lt;/span&gt;
      &lt;span <span style="color: #0f0;">class="country-name"</span> <span style="color: #00f;">property="contact:country"</span>&gt;Country&lt;/span&gt;
    &lt;/div&gt;
  &lt;/div&gt;
&lt;/body&gt;</pre>

...oder <a href="http://microformats.org/wiki/hCal">hCalendar</a> und RDFa iCalendar:

<pre class="code">&lt;body <span style="color: #00f;">xmlns:cal=&quot;http://www.w3.org/2002/12/cal/ical#&quot;</span>&gt;
  &lt;div <span style="color: #0f0;">class=&quot;vevent&quot;</span> <span style="color: #00f;">instanceof=&quot;cal:Vevent&quot;</span>&gt;
    &lt;span <span style="color: #0f0;">class=&quot;summary&quot;</span> <span style="color: #00f;">property=&quot;cal:summary&quot;</span>&gt;Ein Event&lt;/span&gt;
    &lt;span <span style="color: #00f;">property=&quot;cal:dtstart&quot; content=&quot;20070916T1600-0500&quot;&gt;</span>
      &lt;abbr <span style="color: #0f0;">class=&quot;dtstart&quot; title=&quot;20070916T1600-0500&quot;</span>&gt;
        September 16th at 4pm.
      &lt;/abbr&gt;
    &lt;/span&gt;
  &lt;/div&gt;
&lt;/body&gt;</pre>

Legende: <span style="color: #0f0;">Microformats</span> bzw. <span style="color: #00f;">RDFa</span>

So, als nächstes schau ich mir mal die RDFa Attribute näher an...