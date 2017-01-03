---
ID: 690
post_title: Microformats und JSON
author: Matthias Pfefferle
post_date: 2007-12-30 23:58:32
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/12/30/microformats-und-json/
published: true
---
Ich bin vor <a href="http://notiz.blog/2007/09/16/microjson-microformats-in-json/">einiger Zeit</a> schon auf das <a href="http://www.microjson.org">microJSON</a> Projekt gestoßen und fand die Idee, ein einheitliches JSON Format für alle <a href="http://microformats.org/">Microformats</a> zu erstellen, prinzipiell nicht schlecht, deshalb habe ich auch versucht microJSON für mein <a href="http://wordpress.org/extend/plugins/hcard-commenting/">hCard-Commenting</a> Script einzusetzen.

Bei genauerem Betrachten gibt es bei der <a href="http://microjson.org/wiki/JCard">jCard</a> aber zwei unschöne Eigenschaften:
<ol><li>Das <code>n</code> Attribut wird in JSON als <code>name</code> dargestellt.</li>
<li>Das <code>fn</code> Attribut wird gat nicht abgebildet.</li></ol>

Da ich, um den Username in den WordPress Kommentaren darzustellen, auf <code>fn</code> angewiesen bin, habe ich mir verschiedene andere "hCard to JSON" Services angeschaut.
<!--more-->
Test-hCard: <a href="http://pfefferle.org/static/microformats/hcard-test.html">http://pfefferle.org/static/microformats/hcard-test.html</a>

<h3>Überblick der einzelnen JSON Objekte</h3>

<a href="http://microformatique.com/optimus/">Optimus</a>:

<pre class="code">{
  from: "http://pfefferle.org/static/microformats/hcard-test.html",
  title: "hCard Test",
  hcard: {
    "adr": {
      "street-address": "Street",
      "region": "State",
      "locality": "City",
      "postal-code": "12345",
      "country-name": "Country"
    },
    "email": {
      href: "mailto:mail@examle.org",
      value: "mail@examle.org"
    },
    "fn": "Mustermann Max",
    "org": "Organisation",
    "tel": "111-222-333",
    url: [
      "http://example.org", 
      "http://pfefferle.org/static/microformats/aim:goim?screenname=aim", 
      "http://pfefferle.org/static/microformats/ymsgr:sendIM?yim"
    ]
  }
}</pre>

<a href="http://lab.backnetwork.com/ufXtract/">ufXtract</a>:

<pre class="code">// ufXtract 
{
  "vcard": [{
    "fn": "Mustermann Max",
    "n": {
      "given-name": ["Mustermann" ],
      "family-name": ["Max" ]
    },
    "adr": [{
      "street-address": ["Street" ],
      "locality": "City",
      "region": "State",
      "postal-code": "12345",
      "country-name": "Country"
    }],
    "org": {
      "organization-name": "Organisation"
    },
    "email": ["mail@examle.org" ],
    "tel": ["111-222-333" ],
    "url": [
      "http:\/\/example.org\/",
      "aim:goim?screenname=aim",
      "ymsgr:sendIM?yim"
    ]
  }]
}
</pre>

<a href="http://tools.microformatic.com/help/xhtml/hkit/">hKit Service</a> (hKit + JSON)

<pre class="code">json[{
  "fn":"Mustermann Max",
  "adr":{
    "street-address":"Street",
    "postal-code":"12345",
    "country-name":"Country",
    "region":"State",
    "locality":"City"
  },
  "email":"mail@examle.org",
  "org":"Organisation",
  "tel":"111-222-333",
  "url":[
    "http:\/\/example.org",
    "http:\/\/pfefferle.org\/static\/microformats\/aim:goim?screenname=aim",
    "http:\/\/pfefferle.org\/static\/microformats\/ymsgr:sendIM?yim"
  ],
  "n":{
    "given-name":"Mustermann",
    "family-name":"Max"
  }
}]</pre>

<a href="http://microjson.org/">microJSON</a> (<a href="http://microjson.org/wiki/JCard">jCard</a>)

<pre class="code">{
"vcard":{
  "name":{
    "given":"Mustermann",
    "family":"Max"
  },
  "org":"Company",
  "email":"mail@examle.org",
  "address":{
    "street-address":"Street",
    "postal-code":"12345",
    "country-name":"Country",
    "region":"State",
    "locality":"City"
  },
  "tel":"111-222-333",
  "aim":"aim",
  "yim":"yim",
  "url":"http:\/\/example.org"
}</pre>

Leider unterscheidet sich jedes dieser JSON Formate (wenn auch teilweise nur gering) vom anderen, was ja prinzipiell kein wirklich großes Problem ist. Zum Problem wird es erst dann, wenn man einen dieser Dienste durch einen anderen ersetzt, da ein solcher Vorgang immer mit Änderungen am Quellcode verbunden ist.

Es ist im <a href="http://de.wikipedia.org/wiki/Serviceorientierte_Architektur"><abbr title="service oriented architecture">SOA</abbr></a> Ansatz zwar nicht definiert, dass die Services ähnlich wie bei der <a href="http://de.wikipedia.org/wiki/Mehrschichtige_Architektur">Multi-Tier-Architektur</a> austauschbar sein sollten, es würde jedoch eine Menge an Arbeit erspahren.

Microformats sind wohl definierte offene Standards, wieso nicht auch die Austauschformate wohl definieren?

Weiterführende Links:
<ul><li><a href="http://microformats.org/wiki/json">JSON im Microformats Wiki</a></li>
<li><a href="http://microjson.org/wiki/">microJSON Wiki</a></li></ul>