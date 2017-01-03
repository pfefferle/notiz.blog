---
ID: 838
post_title: >
  Operator Userscripts zukünftig im
  OpenService XML-Format
author: Matthias Pfefferle
post_date: 2008-04-30 12:47:38
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/04/30/operator-userscripts-zukuenftig-im-openservice-xml-format/
published: true
aktt_tweeted:
  - "1"
---
<span class="vcard"><a class="url fn" href="http://www.kaply.com/weblog/">Michael Kaply</a></span> plant einige interessante <a href="http://www.kaply.com/weblog/2008/04/29/update-on-activities-microformats-and-operator/">neue Features für Operator</a> (Firefox Microformats-Addon).

Um User-Skripte vor der Installation nicht erst herunterladen zu müssen, sollen die Skripte von <abbr title="Java Script">JS</abbr> auf XML umgestellt werden. Als Basis für das XML-Modell wurde das, von Microsoft spezifizierte, <a href="http://msdn.microsoft.com/en-us/library/cc304072(VS.85).aspx">OpenService Format</a> angedacht.

So könnte ein Script z.B. aussehen:

<pre class="code">&lt;?xml version="1.0" encoding="utf-8"?&gt;
&lt;openServiceDescription
  xmlns="http://www.microsoft.com/schemas/openservicedescription/1.0"&gt;
  &lt;display&gt;
    &lt;name&gt;Find with MapQuest&lt;/name&gt;
    &lt;icon&gt;http://www.mapquest.com/favicon.ico&lt;/icon&gt;
  &lt;/display&gt;
  &lt;homepageUrl&gt;http://www.mapquest.com&lt;/homepageUrl&gt;
  &lt;activity category="Map"&gt;
    &lt;activityAction context="hCard.adr"&gt;
      &lt;execute method="get"
        action="http://www.mapquest.com/maps/map.adp?searchtype=address"&gt;
        &lt;parameter name="address" value="{street-address}"/&gt;
        &lt;parameter name="city" value="{locality}"/&gt;
        &lt;parameter name="state" value="{region}"/&gt;
        &lt;parameter name="zipcode" value="{postal-code}"/&gt;
        &lt;parameter name="country" value="{country-name}"/&gt;
      &lt;/execute&gt;
    &lt;/activityAction&gt;
  &lt;/activity&gt;
&lt;/openServiceDescription&gt;</pre>

Weitere Gedanken zu der <em>"OpenService extension for microformats contexts"</em> oder <em>"Automatic Discovery"</em> findet ihr im <a href="http://microformats.org/wiki/OpenService_Extensions">Microformats Wiki</a>