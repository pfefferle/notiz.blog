---
ID: 728
post_title: Googles Social Graph API
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/02/04/googles-social-graph-api/
published: true
post_date: 2008-02-04 00:18:55
---
Wie schon <a href="http://mrtopf.de/blog/web20/google-offnet-den-social-graph/">mehrfach</a> <a href="http://www.notsorelevant.com/2008-02-03/one-more-step-to-open-the-social-graph/">berichtet</a> wurde, hat Google mit der <em><a href="http://code.google.com/apis/socialgraph/">Social Graph <abbr title="Application Programming Interface">API</abbr></a></em> einen großen Schritt in Richtung <a href="http://dataportability.org">DataPortability</a> gemacht. Die <em>Social Graph <abbr title="Application Programming Interface">API</abbr></em> ist eine weiterer Coup von <a href="http://bradfitz.com/">Brad Fitzpatrick</a> (<a href="http://livejournal.com">Live Journal</a>, memcached und <a href="http://openid.net">OpenID</a>) und bietet eine einfache <abbr title="Application Programming Interface">API</abbr> um "public connections" die man zu genüge im Netz erstellt hat zu interpretieren um wiederverwendbar zu machen.

<blockquote>With the Social Graph API, developers can now utilize public connections their users have already created in other web services. It makes information about public connections between people easily available and useful.</blockquote>

<img src='https://notiz.blog/wp-content/uploads/2008/02/the-web.jpg' alt='Social Graph API' style='float: left; margin-right: 10px; border: none;' /> Die Google <abbr title="Application Programming Interface">API</abbr> setzt hauptsätzlich auf das <a href="http://microformats.org">Microformat</a> <abbr title="Xhtml Friends Network"><a href="http://gmpg.org/xfn/11">XFN</a></abbr> (<abbr title="Version">V</abbr> 1.1) zum darstellen des Sozialen Netzes. 

<em>XHTML Friends Network</em> benutzt das <code>rel</code> Attribut von Links um Verbindungen zwischen Personen darzustellen. <code>&lt;a rel="me" /&gt;</code> kennzeichnet z.B. eine weitere Webseite des Verlinkenden. Weitere Formate (bei Google <a href="http://code.google.com/apis/socialgraph/docs/edges.html">Edge Types</a>) sind das auf RDF basierende <abbr title="Friend of a Friend"><a href="http://www.foaf-project.org/">FoaF</a></abbr> und OpenID delegation Links <code>&lt;link rel="openid.delegate" /&gt;</code>.

Die <abbr title="Application Programming Interface">API</abbr> ist recht simple und lässt sich komplett über URL Key/Value Paare konfigurieren...

<code>http://socialgraph.apis.google.com/lookup?&lt;parameter 1&gt;&amp;&lt;parameter 2&gt;&amp;&lt;parameter n&gt;</code>

...und stellt die Ergebnisse in <abbr title="JavaScript Object Notation">JSON</abbr> dar.

<h4>Social Graph API Client</h4>
<a href="http://redmonk.net">Steve Ivy</a> einer der Gründer des <a href="http://diso-project.org/"><abbr title="Distributed Social Network">DiSo</abbr> Projekts</a> hat eine <em>Social Graph <abbr title="Application Programming Interface">API</abbr></em> Client Klasse in PHP geschrieben und im <a href="http://diso.googlecode.com/svn/php/sgapi/">DiSo SVN</a> zur Verfügung gestellt.

<blockquote>I wrote a quick and dirty client in PHP that cosumes the JSON and returns it in a data structure. <a href="http://groups.google.com/group/diso-project/browse_thread/thread/41e6436cf6d97f26">#</a></blockquote>

<!--more-->
Eine kleine Einführung in die <em>Social Graph <abbr title="Application Programming Interface">API</abbr></em> vom Autor selbst:

https://www.youtube.com/watch?v=LabCylbapuM