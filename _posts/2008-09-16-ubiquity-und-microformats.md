---
ID: 1141
post_title: Ubiquity und Microformats
author: Matthias Pfefferle
post_date: 2008-09-16 20:38:37
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/09/16/ubiquity-und-microformats/
published: true
aktt_tweeted:
  - "1"
---
Ubiquity bietet (neben <a href="https://addons.mozilla.org/de/firefox/addon/4106">Operator</a>) endlich einen echten Anwendungsfall für die <em>Microformats Firefox API</em>. Die <a href="http://developer.mozilla.org/En/Using_microformats">Microformats API</a> basiert auf JavaScript und lässt sich somit auch direkt (und ohne viel Aufwand) in die <a href="https://wiki.mozilla.org/Labs/Ubiquity/Commands_In_The_Wild">Ubiquity-Commands</a> integrieren.

Das folgende wirklich sinnvolle Beispiel zählt alle <a href="http://microformats.org/wiki/hCard">hCards</a> einer Seite und gibt das Ergebnis als <a href="https://wiki.mozilla.org/Labs/Ubiquity/Ubiquity_0.1_Author_Tutorial#Hello_World:_The_First_Command">System-Message</a> aus:

<pre>Components.utils.import("resource://gre/modules/Microformats.js");
CmdUtils.CreateCommand({
  name: "count-hcards",
  execute: function() {
    var doc = Application.activeWindow.activeTab.document;	
    var uFcount = Microformats.count('hCard', doc);
    displayMessage( uFcount );
  }
})</pre>

<span class="vcard"><a href="http://weborganics.co.uk" class="url fn">Martin McEvoy</a></span> hat ein paar wesentlich schickere Commands gebaut, die mit Hilfe des <a href="http://www.transformr.co.uk/">Transformrs</a> Mikroformate verarbeitet. Da für diese Verarbeitung ein Redirect (oder das öffnen einer zweiten Seite) notwendig ist, überprüft er mit Hilfe der Microformats-API zuerst ob sich die notwendigen Mikroformate überhaupt auf der Seite befinden.

Der folgende Code (von Martin) testet z.B. ob mind. ein hCalendar verfügbar ist, bevor er diesen verarbeitet:

<pre>CmdUtils.CreateCommand({
  icon: "http://transformr.co.uk/favicon.ico",
  name: "get-webcal",
  author: {name: "Martin McEvoy", email: "weborganics@googlemail.com"},
  help: "Subscribe to a webcal feed using the 
&lt;a href=\"http://microformats.org/wiki/hcalendar\"&gt;hCalendar&lt;/a&gt; Microformat.",
  preview: function ( pblock ) {
    pblock.innerHTML = "Subscribe to web calendar";
  },
  execute: function() {
    var doc = Application.activeWindow.activeTab.document;
    var mFcount = Microformats.count('hCalendar', doc,{ showHidden : true });
    if (mFcount > 0) {
      var url = "webcal://transformr.co.uk/hcalendar/";
      url += CmdUtils.getWindowInsecure().location ; 
      Utils.openUrlInBrowser(url);
    } else {
      displayMessage('Sorry No hCalendar Events Found!');
    }
  }
})</pre>

Quelle: <a href="http://transformr.co.uk/commands">http://transformr.co.uk/commands</a>

Weitere großartige Ubiquity-Commands im <a href="http://microformats.org/wiki/ubiquity">Microfromats-Wiki</a>...