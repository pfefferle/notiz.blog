---
ID: 3840
post_title: >
  HTML5, Input-Types, Form-Validierung und
  WordPress
author: Matthias Pfefferle
post_date: 2011-07-11 20:46:37
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2011/07/11/html5-input-types-form-validierung-und-wordpress/
published: true
---
<img src="http://notiz.blog/wp-content/uploads/2011/07/HTML5_Logo_256.png" alt="HTML5 Logo" width="256" height="256" class="alignright size-full wp-image-3841" />Dass HTML5 ein paar neue input-types definiert, habe ich durch die <a href="http://microformats.org/wiki/hcard-input-brainstorming#HTML5_input_types">hcard-input-brainstorming</a> so am Rande auf geschnappt, mir aber nichts weiter dabei gedacht... Durch Zufall bin ich heute aber über folgenden <a href="http://twitter.com/sprungmarkers/status/90305500108947457">Tweet</a> von Sylvia Egger gestoßen:

<blockquote>Just implemented native #HTML5 form validation on #wp comments form - it' quite simple & should be in #wp default theme</blockquote>

und habe bissle recherchiert... Mit den neuen Input-Types ist es doch tatsächlich möglich Input-Felder über den Browser validieren zu lassen... Ich bin begeistert! :)

Trägt man beispielsweise eine Nicht-Email-Adresse in folgendes Feld...

<pre><code>&lt;input type="email" /></code></pre>

bekommt man...

<img src="http://notiz.blog/wp-content/uploads/2011/07/firefox-email-validation.jpg" alt="Email Validation im Firefox" title="Email Validation im Firefox" width="500" height="120" class="aligncenter size-full wp-image-3855" />

Schön wenn man sich noch über solche Kleinigkeiten freuen kann oder ;)

Lange rede kurzer Sinn: Da WordPress alle Formulare an zentraler Stelle definiert, ist es ziemlich einfach sie mit ein paar neuen Input-Types zu versehen. Mit dem folgenden Code wird das Kommentar-Formular mit den Typen "email" und "url" und das Suchformular mit dem Typ "search" (funktioniert nur in den WebKit-Browsern) erweitert:

<ins datetime="2011-07-12T06:58:09+00:00"><strong>Code-Update</strong>: <a href="http://yatil.de/">Eric Eggert</a> hat mich in den <a href="http://notiz.blog/2011/07/11/html5-input-types-form-validierung-und-wordpress/#comment-173210">Kommentaren</a> darauf hingewiesen, dass man mit <code>&lt;input required /&gt;</code> auch noch die Pflichtfelder validieren kann. Danke!</ins>

<ins datetime="2011-07-12T06:58:09+00:00"><strong>Code-Update 2</strong>: Dank <a href="http://www.im-tal.net" rel="external" class="url">maxe</a> werden jetzt auch die WordPress Settings berücksichtigt (Comment author must fill out name and e-mail) und das "Comment"-Feld ist natürlich auch <code>required</code></ins>

<pre><code>&lt;?php
/*
Plugin Name: html5 input-types
Plugin URI: http://notiz.blog/
Description: Adds the new HTML5 input-types to WordPress' default forms
Version: 0.1
Author: pfefferle
Author URI: http://notiz.blog/
*/

add_filter("comment_form_default_fields", "change_comment_input_types");

function change_comment_input_types($fields) {
  if (get_option("require_name_email", false)) {
    $fields['author'] = preg_replace('/&lt;input/', '&lt;input required', $fields['author']);
    $fields['email'] = preg_replace('/"text"/', '"email" required', $fields['email']);
  } else {
    $fields['email'] = preg_replace('/"text"/', '"email"', $fields['email']);
  }

  $fields['url'] = preg_replace('/"text"/', '"url"', $fields['url']);

  return $fields;
}

add_filter("get_search_form", "change_search_form_input_types");

function change_search_form_input_types($form) {
  return preg_replace('/"text"/', '"search"', $form);
}

add_filter("comment_form_field_comment", "change_comment_field_input_types");

function change_comment_field_input_types($field) {
  return preg_replace('/&lt;textarea/', '&lt;textarea required', $field);
}
?&gt;</code></pre>

Funktioniert als Plugin und in Child-Themes (einfach in die <code>functions.php</code> kopieren).

Danke auch an <a href="http://marcgoertz.de/">Marc Görtz</a> der mich über <a href="http://twitter.com/dreamseer">Twitter</a> reichlich mit Links zu dem Thema versorgt hat:

<ul><li><a href="http://diveintohtml5.info/forms.html">A Form of Madness (den hab ich selber gefunden)</a></li>
<li><a href="http://html5pattern.com/">HTML5 Pattern</a></li>
<li><a href="http://flowplayer.org/tools/demos/validator/index.html">Fallback jQuery Validator</a></li></ul>

Testen könnt ihr das übrigens hier auf notiz.blog.