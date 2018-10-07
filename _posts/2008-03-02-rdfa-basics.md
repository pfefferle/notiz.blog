---
ID: 762
post_title: RDFa Basics
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/03/02/rdfa-basics/
published: true
post_date: 2008-03-02 14:58:54
---
Wer sich viel mit <a href="http://microformats.org">Microformats</a> beschäftigt, ist sicher schon öfters über den Begriff RDFa gestolpert. Die Idee, (X)HTML semantischer zu machen, ist bei beiden Formaten gleich, der Unterschied liegt hauptsächlich in der Syntax.
Während Microformats ausschließlich auf HTML 4.01 bzw. XHTML 1.0 validen Tags und Attributen basiert:

<pre class="code">&lt;div class="vcard"&gt;
  &lt;span class="fn"&gt;Max Mustermann&lt;/span&gt;
  &lt;a class="email" href="mailto:max.mustermann@example.org"&gt;
    max.mustermann@example.org
  &lt;/a&gt;
&lt;/div&gt;</pre>

<small>Beispiel <a href="http://microformats.org/wiki/hCard">hCard</a></small>

...basiert RDFa auf dem klassischen <a href="http://www.w3.org/TR/rdf-primer/"><abbr title="Resource Description Framework">RDF</abbr></a> und mit XHTML 2.0 neu eingeführten Attributen wie z.B. <code>property</code> und <code>about</code>:

<pre class="code">&lt;body xmlns:contact="http://www.w3.org/2001/vcard-rdf/3.0#"&gt;
  &lt;span property="contact:fn"&gt;Max Mustermann&lt;/span&gt;
  &lt;a rel="contact:email" href="mailto:max.mustermann@example.org"&gt;
    max.mustermann@example.org
  &lt;/a&gt;
&lt;/body&gt;</pre>

<small>Beispiel <a href="http://www.w3.org/TR/vcard-rdf">vCard RDF</a> in <a href="http://www.w3.org/TR/xhtml-rdfa-primer/#publishing-contact-info">RDFa</a></small>

Eine gute Einführung in das Thema RDFa bietet das Video von Manu Sporny:

https://www.youtube.com/watch?v=ldl0m-5zLz4

Rein Technisch gesehen ist RDFa, durch die Nutzung von Namespaces und die bessere Skalierbarkeit durch URIs, definitiv der bessere Standard. Ich denke trotzdem nicht dass RDFa die Microformats in näherer Zukunft ablösen wird, da RDFa nur unter XHTML 2.0 möglich ist und (meines Wissens) im Konkurrenz-Format (X)HTML 5.0 nicht angedacht wird. Es ist deshalb notwendig beide Formate weiter voranzutreiben und so weit wie möglich auf einem einheitlichen Standard, wie z.B. der vCard im oben beschriebenen Beispiel, aufzubauen. Während der Übergangsphase ist es so relativ einfach mit <a href="http://www.w3.org/TR/grddl/"><abbr title="Gleaning Resource Descriptions from Dialects of Languages">GRDDL</abbr></a> zwischen den beiden Formaten zu transformieren.
 
In seinem Artikel "<a href="http://evan.prodromou.name/RDFa_vs_microformats">RDFa vs microformats</a>" beschreibt Evan Prodromou die für ihn notwendigen Schritte für die Zukunft von RDFa:
<ol><li>RDFa gets acknowledged and embraced by microformats.org as the future of semantic-data-in-XHTML</li>
<li>The RDFa group makes an effort to encompass existing microformats with a minimum of changes</li>
<li>microformats.org leaders join in on the RDFa authorship process</li>
<li>microformats.org becomes a focus for developing real-world RDFa vocabularies</li></ol>

Mal schauen wie es wirklich kommt und was sich in Zukunft durchsetzen wird...

Wer sich für das Thema interessiert, kann ja mal <a href="http://sioc-project.org/firefox">Semantic Radar für Firefox</a> ausprobieren. Semantic Radar macht (ähnlich wie Operator für Microformats) RDF und RDFa Inhalte in Webseiten sichtbar.