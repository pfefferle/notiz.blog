---
ID: 1135
post_title: 'PortableContacts &#8211; Hacks'
author: Matthias Pfefferle
post_date: 2008-09-11 16:23:43
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/09/11/portablecontacts-hacks/
published: true
aktt_tweeted:
  - "1"
---
<a href="http://radar.oreilly.com/davidr">David Recordon</a> stellt auf <a href="http://radar.oreilly.com">O'Reilly - Radar</a> zwei der spannendsten Ergebnisse des gestrigen <a href="http://upcoming.yahoo.com/event/1078491/">PortableContacts Hackathon (bei Six Apart)</a> vor:

<blockquote>Joseph Smarr and <a href="http://kevinmarks.com/">Kevin Marks</a> of Google hacked together a web transformer that integrates Microformats, vCard, and the Portable Contacts API.  Given Kevin's homepage which is full of Microformats, they've built an API that extracts his profile information from hCard, uses a public API from Technorati to transform it to vCard, and then exposes it as a Portable Contacts API endpoint.  Not only does this work on Kevin's own page, but his Twitter profile as well which contains basic profile information such as name, homepage, and a short bio.</blockquote>

Ein schönes Beispiel was man mit semantisch ausgezeichneten Informationen machen kann und dass Microformats eben auch (ohne viel Aufwand und mit ein bisschen Transformation) in <em>höherwertige</em> APIs integriert werden können... also keine hCard wurde umsonst geschrieben :)

<blockquote><a href="http://brianellin.com/">Brian Ellin</a> of JanRain has successfully combined OpenID, XRDS-Simple, OAuth, and the Portable Contacts API to start showing how each of these building blocks should come together.  Upon visiting his demo site he logs in using his OpenID.  From there, the site discovers that Plaxo hosts his address book and requests access to it via OAuth.  Finishing the flow, his demo site uses the Portable Contacts API to access information about his contacts directly from Plaxo.  End to end, login with an OpenID and finish by giving the site access to your address book without having to fork over your password.</blockquote>

Dazu brauche ich nicht mehr sagen, als: Implementieren! Sofort und überall ;)