---
ID: 2745
post_title: 'OpenWeb-Notizen: XAuth, OExchange, Firefox Sync, RDFa'
author: Matthias Pfefferle
post_date: 2010-06-02 20:09:15
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2010/06/02/openweb-notizen-xauth-oexchange-firefox-sync-rdfa/
published: true
---
<strong>Chris Messina erklärt XAuth</strong>
XAuth ist eine Art <em>Cross-Domain</em> Cookie mit dem man Versucht die Flut an Share, Like und Login Icons auf ein Minimum zu reduzieren.

<object type="application/x-shockwave-flash" style="width:480px; height:360px" data="http://vimeo.com/moogaloop.swf?clip_id=12121710&amp;server=vimeo.com&amp;show_title=0&amp;show_byline=0&amp;show_portrait=0&amp;color=00ADEF&amp;fullscreen=1"><param name="movie" value="http://vimeo.com/moogaloop.swf?clip_id=12121710&amp;server=vimeo.com&amp;show_title=0&amp;show_byline=0&amp;show_portrait=0&amp;color=00ADEF&amp;fullscreen=1"></param><param name="allowfullscreen" value="true" /><param name="allowscriptaccess" value="always" /><param name="movie" value="http://vimeo.com/moogaloop.swf?clip_id=12121710&amp;server=vimeo.com&amp;show_title=0&amp;show_byline=0&amp;show_portrait=0&amp;color=00ADEF&amp;fullscreen=1" /></object>

&raquo; <a href="http://vimeo.com/12121710">XAuth - an introduction</a>
&raquo; <a href="http://xauth.org">Offizielle XAuth Seite</a>

<strong>OExchange einfach erklärt</strong>
OExchange ist ein offenes Protokoll um eine beliebige URL mit einem beliebigen Service im Web zu teilen. Die Demo zeigt die Funktionsweise von OExchange und welche Vorteile sich in Kombination mit z.B. XAuth ergeben.

<object type="application/x-shockwave-flash" style="width:480px; height:290px" data="http://www.youtube.com/v/Be9ArGBUTco"><param name="movie" value="http://www.youtube.com/v/Be9ArGBUTco"></param><param name="allowFullScreen" value="true"></param><param name="allowscriptaccess" value="always"></param></object>

&raquo; <a href="http://www.oexchange.org/demo/">OExchange in action</a>
&raquo; <a href="http://www.oexchange.org/">Offizielle OExchange Seite</a>

<strong>Firefox Sync</strong>
Mozilla benennt das Labs-Projekt <em>Weave Sync</em> in <em>Firefox Sync</em> um und kündigt an, den Sync-Mechanismus in eine der nächsten Firefox Versionen fest zu integrieren. Im Zuge meiner Recherche bin ich außerdem noch auf einen Wiki-Artikel gestoßen, der erklärt wie man den <em>Firefox Sync</em> zukünftig auch mit OpenID oder OAuth koppeln könnte:

<blockquote>The user must have a way of proving to a third-party service that they really are who they claim, and for the Mozilla service to provide information back to the third-party service that access has been granted. The OpenID and OAuth protocols provide what we need here, and the OpenID/OAuth hybrid flow has been described.

Once this is done, the third party service will be able to establish a relationship with the Weave Sync service for a user, without the user disclosing his or her password.</blockquote>

&raquo; <a href="http://www.mozilla.com/en/firefox/sync/">Stay in Sync With Your Firefox</a>
&raquo; <a href="http://mozillalabs.com/blog/2010/06/firefox-sync-graduates-from-mozilla-labs/">Firefox Sync Graduates from Mozilla Labs</a>
&raquo; <a href="https://wiki.mozilla.org/Labs/Weave/Developer/SecureDataSharing">Secure Data Sharing</a>

<strong>RDFa 1.1 - Alles neu, alles anders</strong>
Dank HTML5 (ohne X) wurde RDFa noch einmal grundlegend überdacht. In der Version 1.1 werden die RDF-Vocabularies beispielsweise nicht mehr über Namespaces definiert. Früher:

<pre class="example">&lt;a <strong>xmlns:cc="http://creativecommons.org/ns#"</strong>
   rel="cc:license"
   href="http://creativecommons.org/licenses/by-nc-nd/3.0/"&gt;
&lt;/a&gt;.</pre>

Jetzt:

<pre class="example">&lt;a <strong>prefix="cc: http://creativecommons.org/ns#"</strong>
   rel="cc:license"
   href="http://creativecommons.org/licenses/by-nc-nd/3.0/"&gt;
&lt;/a&gt;.</pre>

Grund der Änderung: HTML kennt im Gegensatz zu XHTML keine Namespaces und RDFa soll sowohl in HTML5 als auch in XHTML5 integriert werden.

&raquo; <a href="http://www.w3.org/TR/rdfa-core/">RDFa Core 1.1</a>

<strong>RDFa checker</strong>
Toby Inkster hat einen sehr umfangreichen RDFa checker veröffentlicht:

<blockquote>It checks your web page for RDFa  and displays any data found there. It also compares your data against the published recommendations from major consumers/users of RDFa data, to see how well your data matches their requirements.</blockquote>

&raquo; <a href="http://check.rdfa.info/">check rdfa</a>