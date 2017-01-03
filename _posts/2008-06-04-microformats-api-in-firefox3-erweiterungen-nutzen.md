---
ID: 896
post_title: >
  Microformats API in
  Firefox3-Erweiterungen nutzen
author: Matthias Pfefferle
post_date: 2008-06-04 20:46:21
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/06/04/microformats-api-in-firefox3-erweiterungen-nutzen/
published: true
aktt_tweeted:
  - "1"
---
<a href="http://www.ibm.com/developerworks/xml/library/x-tipffoxmicroapi/#author">Rob Crowther</a> hat für <a href="http://www.ibm.com/developerworks/">IBM developerWorks</a> eine großartige Anleitung (mit Beispiel-Code) geschrieben, <a href="http://www.ibm.com/developerworks/xml/library/x-tipffoxmicroapi/">wie man die Microformats API in Firefox3 Extensions nutzen kann</a>.

<blockquote>The upcoming Firefox 3.0 release has built-in support for microformats in the form of an API that you can access from a Firefox extension. In this tip, you follow a simple example of how to use this API from within your extension code. You take a skeleton Hello World extension and give it the ability to store an hCard from any Web page and then use that stored hCard to populate a Web form.</blockquote>

Die <a href="http://www.ibm.com/developerworks/xml/library/x-tipffoxmicroapi/#download">Beispiel-Erweiterung</a> von Crowther nutzt hCard-Informationen um ein (im Beispiel beiliegendes) Profil-Formular auszufüllen.

<img src="http://notiz.blog/wp-content/uploads/2008/06/hcardformfiller.jpg" alt="hcardformfiller.jpg" border="0" width="480" height="230" />

Ablauf: Zuerst auf ne Seite mit hCard, linken Knopf drücken, dann auf das Fromular und rechten Knopf drücken.

<h4>hCardFormFiller für WordPress</h4>

Um dem Beispiel etwas mehr Nutzen zu geben, habe ich es testweise für das WordPress Kommentarformular umgeschrieben. Die Einzige notwendige Änderung ist, folgenden Code in der <code>overlay.js</code>:

<pre class="code">onToolbarButtonPasteCommand: function(e) {
 if (this.uF.fn) {
   content.document.getElementById('name').value = this.uF.fn;
   content.document.getElementById('email').value = this.uF.email[0].value;
   content.document.getElementById('homepage').value = this.uF.url[0];
   content.document.getElementById('address1').value = this.uF.adr[0]['street-address'];
   content.document.getElementById('address2').value = this.uF.adr[0].locality;
   content.document.getElementById('city').value = this.uF.adr[0].region;
   content.document.getElementById('postcode').value = this.uF.adr[0]['postal-code'];
 }
}</pre>

durch folgenden Code:

<pre class="code">onToolbarButtonPasteCommand: function(e) {
 if (this.uF.fn) {
   content.document.getElementById('author').value = this.uF.fn;
   content.document.getElementById('email').value = this.uF.email[0].value;
   content.document.getElementById('url').value = this.uF.url[0];
 }
}</pre>

zu ersetzen und das war's. Jetzt könnt ihr mit einer <a href="http://microformats.org/wiki/hCard">hCard</a> bewaffnet losziehen und WordPress Blogs zuspammen :)

Wer das Addon mal ausprobieren möchte kann sich den angepassten <a href="http://notiz.blog/wp-content/uploads/2008/06/hcardformfiller.xpi" rel="enclosure">hCardFormFiller for WordPress</a> runterladen... den original Code findet man <a href="http://www.ibm.com/developerworks/xml/library/x-tipffoxmicroapi/#download">hier</a>.

<a href="http://notiz.blog/2008/05/21/wo-sind-die-microformats-im-firefox-3/">Nachdem die Microformats kein <abbr title="User Interface">UI</abbr> spendiert bekommen haben</a>, gibt es vielleicht demnächst einige Addons die diese Lücke füllen werden.

Interessante Links:
<ul><li><a href="http://www.ibm.com/developerworks/xml/library/x-tipffoxmicroapi/">Use the new microformats API in your Firefox 3.0 Extensions</a></li>
<li><a href="http://www.kaply.com/weblog/2008/05/20/where-are-the-microformat-in-firefox-3/" title="Where are the microformats in Firefox 3?">Where are the microformats in Firefox 3?</a></li></ul>