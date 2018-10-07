---
ID: 1627
post_title: Mozilla Jetpack (und Microformats)
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/06/05/mozilla-jetpack-und-microformats/
published: true
post_date: 2009-06-05 08:50:38
---
<a href="https://jetpack.mozillalabs.com">Jetpack</a> ist das jüngste Baby der <em>Mozilla Labs</em> und bietet eine Art API, die es Entwicklern ermöglicht, den Firefox mit klassischen Web-Techniken (HTML, JavaScript und CSS) zu erweitern. Statt mit <abbr title="XML User Interface Language"><a href="http://www.mozilla.org/projects/xul/">XUL</a></abbr> kann man seine Firefox Addons demnächst vielleicht wirklich mit HTML und CSS gestalten. Großartige Idee!

https://vimeo.com/4752576

Übrigens unterstützt Jetpack, <a href="https://notiz.blog/2008/09/16/ubiquity-und-microformats/">wie auch Ubiquity</a>, die ab der Version 3 in Firefox nativ implementierte <a href="https://developer.mozilla.org/En/Using_microformats">Microformats API</a>. Der folgende Code zeigt, wie man die Microformats API in Jetpack-Skripte integrieren kann. Das Beispiel zählt z.B. alle hCards der Seite, auf der man sich gerade befindet und zeigt das Ergebnis per Info-Message an:

<pre>Components.utils.import("resource://gre/modules/Microformats.js");

// count hCards
jetpack.tabs.onFocus(function() {
  // load HTML
  var doc = jetpack.tabs.focused.contentDocument;
  // count microformats
  var uFcount = Microformats.count('hCard', doc);
  // load notifier
  jetpack.notifications.show({
    title: 'hCards',
    body: 'number of hCards on this website: ' + uFcount,
    icon: 'http://microformats.org/favicon.ico'
  });
});</pre>

<ins datetime="2009-06-05T10:24:01+00:00"><strong>Nachtrag</strong></ins>:

Unter Windows und Linux scheinen die Messages nicht so ganz zu funktionieren, deshalb gibt's hier nochmal nen Beispiel wo der Counter in der Statusbar ausgegeben wird:

<pre>Components.utils.import("resource://gre/modules/Microformats.js");

jetpack.statusBar.append({
  html: '&lt;img src="http://microformats.org/favicon.ico"&gt;
           hCards: &lt;span id="hcard-count"&gt;0&lt;/span&gt;',
  onReady: function(jetpackWidget) {
    function counthCard(){
      //load HTML
      var doc = jetpack.tabs.focused.contentDocument;
      // count microformats
      var uFcount = Microformats.count('hCard', doc);
      if (uFcount > 0) {
       $(jetpackWidget).find('#hcard-count').html(uFcount);
      }
    }
    jetpack.tabs.onFocus(counthCard);
  }
});</pre>

Mal schaun ob mir demnächst noch etwas sinnvolleres Einfällt ;)