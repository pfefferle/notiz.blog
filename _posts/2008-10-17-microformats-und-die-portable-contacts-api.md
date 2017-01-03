---
ID: 1209
post_title: >
  Microformats und die Portable Contacts
  API
author: Matthias Pfefferle
post_date: 2008-10-17 19:13:48
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/10/17/microformats-und-die-portable-contacts-api/
published: true
aktt_tweeted:
  - "1"
---
Dass sich das <a href="http://portablecontacts.net/draft-spec.html#structure">Portable Contacts Schema</a> trotz der Aussage:

<blockquote cite="http://portablecontacts.net/draft-spec.html#anchor5">Third, we're reusing existing standards wherever possible, including vCard, OpenSocial, XRDS-Simple, OAuth, etc.</blockquote>

von dem des <a href="http://microformats.org/wiki/jcard">v/hCard Schema</a> unterscheidet, habe ich ja schon <a href="http://notiz.blog/2008/08/08/portable-contacts-schicker-als-ich-dachte/#portable-microformats">vor einigen Wochen erläutert</a>:

<blockquote>Schade dass die vCard nicht zu 100% übernommen wurde… sonst hätte man ohne größere Änderungen auch die JSON-Serialisierte hCard (jCard) in den Prozess integrieren können. Spannend wäre es vor allem für Services wie Twitter, die das Freundesnetzwerk sowieso mit hCards auszeichnen.</blockquote>

Aber das schöne an Standards ist, dass sie sich ohne großen Aufwand in andere transformieren lassen. <a href="http://lab.madgex.com/">Magdex</a> (die Firma hinter <a href="http://lab.madgex.com/ufxtract/">UfXtract</a> und <a href="">OAuth.net</a>) bietet eine <a href="http://lab.madgex.com/portablecontacts/">Reihe dieser Transformatoren</a> um z.B. <a href="http://lab.madgex.com/portablecontacts/hcardtopoco.aspx">hCards</a>, <a href="http://lab.madgex.com/portablecontacts/hcardxfntopoco.aspx">hCards + XFN</a> oder <a href="http://lab.madgex.com/portablecontacts/hresumetopoco.aspx">hResumes</a> in das <em>Portable Contacts</em> - Format zu bringen.

...jetzt das ganze nur noch mit <a href="http://portablecontacts.net/draft-spec.html#anchor10">OAuth</a> schützen und fertig ist die <em>Portable Contacts</em> API :)

(<a href="http://www.glennjones.net/Post/838/MicroformatstoPortableContactsAPIconverters.htm">via</a>)