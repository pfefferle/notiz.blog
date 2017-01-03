---
ID: 921
post_title: 'hForms &#8211; Semantische Formulare'
author: Matthias Pfefferle
post_date: 2008-06-28 15:09:39
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/06/28/hforms-semantische-formulare/
published: true
aktt_tweeted:
  - "1"
---
Warum sollte nur die Ausgabe ((X)HTML) semantisch anreichern und die Eingabe vernachlässigen?

Beim <em>spielen</em> mit dem <a href="http://notiz.blog/2008/03/28/hcard-mapper/">hCard-Mappers</a> und der <a href="http://notiz.blog/2008/06/04/microformats-api-in-firefox3-erweiterungen-nutzen/">Firefox-Microformats-API</a> kam mir die Idee, auch Formulare semantisch auszuzeichnen...

In dem Artikel <em><a href="http://www.ibm.com/developerworks/xml/library/x-tipffoxmicroapi/">Use the new microformats API in your Firefox 3.0 Extensions</a></em> beschreibt Rob Crowther wie man mit Hilfe der Firefox-Microformats-API eine hCard speichert um sie zum Ausfüllen verschiedener Formulare weiterverwenden zu können.

Das Problem: Das Prinzip funktioniert leider nur bei Formularen die dem festgelegten Aufbau entsprechen. Im Fall des Beispiels wäre das:

<pre class="code">&lt;h1&gt;hCardFormFiller Target Form&lt;/h1&gt;
&lt;form action="#" method="post"&gt;
    &lt;label&gt;Name: &lt;input type="text" id="name" /&gt;&lt;/label&gt;&lt;br /&gt;
    &lt;label&gt;Email: &lt;input type="text" id="email" /&gt;&lt;/label&gt;&lt;br /&gt;
    &lt;label&gt;Home page: &lt;input type="text" id="homepage" /&gt;&lt;/label&gt;&lt;br /&gt;
    &lt;label&gt;Street Address: &lt;input type="text" id="address1" /&gt;&lt;/label&gt;&lt;br /&gt;
    &lt;label&gt;City: &lt;input type="text" id="address2" /&gt;&lt;/label&gt;&lt;br /&gt;
    &lt;label&gt;Region: &lt;input type="text" id="city" /&gt;&lt;/label&gt;&lt;br /&gt;
    &lt;label&gt;Postcode: &lt;input type="text" id="postcode" /&gt;&lt;/label&gt;&lt;br /&gt;
    &lt;input type="submit" /&gt;
&lt;/form&gt;</pre>

Warum nicht gleich das Formular als hCard-From aufbauen?

<pre class="code">&lt;form action="#" method="post" id="vcard" &gt;
  &lt;fieldset <strong>id="fn"</strong>&gt;
    &lt;legend&gt;Name&lt;/legend&gt;
    &lt;label for="given-name"&gt;Vorname:&lt;/label&gt;
      &lt;input type="text" <strong>id="given-name"</strong> /&gt;
    &lt;label for="family-name"&gt;Nachname:&lt;/label&gt;
      &lt;input type="text" <strong>id="family-name"</strong> /&gt;
  &lt;/fieldset&gt;
  &lt;label for="email"&gt;Email:&lt;/label&gt;
    &lt;input type="text" <strong>id="email"</strong> /&gt;
  &lt;label for="url"&gt;Homepage:&lt;/label&gt;
    &lt;input type="text" <strong>id="url"</strong> /&gt;
  &lt;fieldset <strong>id="adr"</strong>&gt;
    &lt;legend&gt;Adresse&lt;/legend&gt;
    &lt;label for="street-address"&gt;Straße:&lt;/label&gt;
      &lt;input type="text" <strong>id="street-address"</strong> /&gt;
    &lt;label for="locality"&gt;Stadt:&lt;/label&gt;
      &lt;input type="text" <strong>id="locality"</strong> /&gt;
    &lt;label for="region"&gt;Region:&lt;/label&gt;
      &lt;input type="text" <strong>id="region"</strong> /&gt;
    &lt;label for="postal-code"&gt;Postleitzahl:&lt;/label&gt;
      &lt;input type="text" <strong>id="postal-code"</strong> /&gt;
  &lt;/fieldset&gt;
  &lt;input type="submit" /&gt;
&lt;/form&gt;</pre>

Das Einheitliche Format für Ein- (Formular) und Ausgabe (Microformats) hätte zur Folge, dass keine aufwendigen Mapper (wie z.B. <a href="http://notiz.blog/2008/03/28/hcard-mapper/">hCard-Mapper</a>) mehr nötig wären um ein Formular per <a href="http://microformats.org/wiki/hCard">hCard</a> auszufüllen...

Schöne neue Welt :)