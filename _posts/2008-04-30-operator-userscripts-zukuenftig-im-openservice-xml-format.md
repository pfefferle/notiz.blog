---
ID: 838
post_title: >
  Operator Userscripts zukünftig im
  OpenService XML-Format
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/04/30/operator-userscripts-zukuenftig-im-openservice-xml-format/
published: true
post_date: 2008-04-30 12:47:38
---
<!-- wp:paragraph -->
<p><a href="http://www.kaply.com/weblog/">Michael Kaply</a> plant einige interessante <a href="http://www.kaply.com/weblog/2008/04/29/update-on-activities-microformats-and-operator/">neue Features für Operator</a> (Firefox Microformats-Addon).</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Um User-Skripte vor der Installation nicht erst herunterladen zu müssen, sollen die Skripte von <abbr title="Java Script">JS</abbr> auf XML umgestellt werden. Als Basis für das XML-Modell wurde das, von Microsoft spezifizierte, <a href="http://msdn.microsoft.com/en-us/library/cc304072(VS.85).aspx">OpenService Format</a> angedacht.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>So könnte ein Script z.B. aussehen:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;?xml version="1.0" encoding="utf-8"?>
&lt;openServiceDescription
  xmlns="http://www.microsoft.com/schemas/openservicedescription/1.0">
  &lt;display>
    &lt;name>Find with MapQuest&lt;/name>
    &lt;icon>http://www.mapquest.com/favicon.ico&lt;/icon>
  &lt;/display>
  &lt;homepageUrl>http://www.mapquest.com&lt;/homepageUrl>
  &lt;activity category="Map">
    &lt;activityAction context="hCard.adr">
      &lt;execute method="get"
        action="http://www.mapquest.com/maps/map.adp?searchtype=address">
        &lt;parameter name="address" value="{street-address}"/>
        &lt;parameter name="city" value="{locality}"/>
        &lt;parameter name="state" value="{region}"/>
        &lt;parameter name="zipcode" value="{postal-code}"/>
        &lt;parameter name="country" value="{country-name}"/>
      &lt;/execute>
    &lt;/activityAction>
  &lt;/activity>
&lt;/openServiceDescription></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Weitere Gedanken zu der <em>"OpenService extension for microformats contexts"</em> oder <em>"Automatic Discovery"</em> findet ihr im <a href="http://microformats.org/wiki/OpenService_Extensions">Microformats Wiki</a></p>
<!-- /wp:paragraph -->