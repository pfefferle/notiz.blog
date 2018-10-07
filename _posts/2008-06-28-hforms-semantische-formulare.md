---
ID: 921
post_title: 'hForms &#8211; Semantische Formulare'
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/06/28/hforms-semantische-formulare/
published: true
post_date: 2008-06-28 15:09:39
---
<!-- wp:paragraph -->
<p>Warum sollte nur die Ausgabe ((X)HTML) semantisch anreichern und die Eingabe vernachlässigen?</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Beim <em>spielen</em> mit dem <a href="https://notiz.blog/2008/03/28/hcard-mapper/">hCard-Mappers</a> und der <a href="https://notiz.blog/2008/06/04/microformats-api-in-firefox3-erweiterungen-nutzen/">Firefox-Microformats-API</a> kam mir die Idee, auch Formulare semantisch auszuzeichnen...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In dem Artikel <em><a href="http://www.ibm.com/developerworks/xml/library/x-tipffoxmicroapi/">Use the new microformats API in your Firefox 3.0 Extensions</a></em> beschreibt Rob Crowther wie man mit Hilfe der Firefox-Microformats-API eine hCard speichert um sie zum Ausfüllen verschiedener Formulare weiterverwenden zu können.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Das Problem: Das Prinzip funktioniert leider nur bei Formularen die dem festgelegten Aufbau entsprechen. Im Fall des Beispiels wäre das:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;h1>hCardFormFiller Target Form&lt;/h1>
&lt;form action="#" method="post">
    &lt;label>Name: &lt;input type="text" id="name" />&lt;/label>&lt;br />
    &lt;label>Email: &lt;input type="text" id="email" />&lt;/label>&lt;br />
    &lt;label>Home page: &lt;input type="text" id="homepage" />&lt;/label>&lt;br />
    &lt;label>Street Address: &lt;input type="text" id="address1" />&lt;/label>&lt;br />
    &lt;label>City: &lt;input type="text" id="address2" />&lt;/label>&lt;br />
    &lt;label>Region: &lt;input type="text" id="city" />&lt;/label>&lt;br />
    &lt;label>Postcode: &lt;input type="text" id="postcode" />&lt;/label>&lt;br />
    &lt;input type="submit" />
&lt;/form></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Warum nicht gleich das Formular als hCard-From aufbauen?</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>&lt;form action="#" method="post" id="vcard" >
  &lt;fieldset id="fn">
    &lt;legend>Name&lt;/legend>
    &lt;label for="given-name">Vorname:&lt;/label>
      &lt;input type="text" id="given-name" />
    &lt;label for="family-name">Nachname:&lt;/label>
      &lt;input type="text" id="family-name" />
  &lt;/fieldset>
  &lt;label for="email">Email:&lt;/label>
    &lt;input type="text" id="email" />
  &lt;label for="url">Homepage:&lt;/label>
    &lt;input type="text" id="url" />
  &lt;fieldset id="adr">
    &lt;legend>Adresse&lt;/legend>
    &lt;label for="street-address">Straße:&lt;/label>
      &lt;input type="text" id="street-address" />
    &lt;label for="locality">Stadt:&lt;/label>
      &lt;input type="text" id="locality" />
    &lt;label for="region">Region:&lt;/label>
      &lt;input type="text" id="region" />
    &lt;label for="postal-code">Postleitzahl:&lt;/label>
      &lt;input type="text" id="postal-code" />
  &lt;/fieldset>
  &lt;input type="submit" />
&lt;/form></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Das Einheitliche Format für Ein- (Formular) und Ausgabe (Microformats) hätte zur Folge, dass keine aufwendigen Mapper (wie z.B. <a href="https://notiz.blog/2008/03/28/hcard-mapper/">hCard-Mapper</a>) mehr nötig wären um ein Formular per <a href="http://microformats.org/wiki/hCard">hCard</a> auszufüllen...</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Schöne neue Welt :)</p>
<!-- /wp:paragraph -->