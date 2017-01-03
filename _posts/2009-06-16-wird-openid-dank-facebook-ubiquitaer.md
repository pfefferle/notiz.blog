---
ID: 1675
post_title: Wird OpenID dank Facebook ubiquitär?
author: Matthias Pfefferle
post_date: 2009-06-16 22:28:41
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2009/06/16/wird-openid-dank-facebook-ubiquitaer/
published: true
---
Ich habe es endlich geschafft! Ich habe den automatischen Facebook OpenID-Login erfolgreich getestet :)

Ursprünglich hab ich den Auto-Login mit Google probiert, das wollte aber nicht so ganz funktionieren (ähnliche Problematik wie bei <a href="http://notsorelevant.com/2009-06-08/facebook-is-a-relying-party-but/">Carsten</a>), also hab ich es (nachdem mich <a href="http://joss.blogs.lincoln.ac.uk/2009/06/16/facebooks-transparent-use-of-openid/">Joss Winn mit seinem Blog-Post</a> nochmal an das neue Facebook-Feature erinnert hat) noch mal mit einem anderen OpenID-Provider getestet und siehe da, mit <a href="http://www.myopenid.com/">myOpenID</a> funktioniert es.

Um OpenID für Facebook zu aktivieren, muss man in den <a href="https://register.facebook.com/editaccount.php">Einstellungen</a> seinen Account mit einer OpenID verknüpfen (am Besten man probiert es mit myOpenID). 

<img src="http://notiz.blog/wp-content/uploads/2009/06/facebook-openid.png" alt="Facebooks OpenID Settings" width="480" height="142" class="aligncenter" />

Um es zu testen, muss man sich einfach bei Facebook (bloß nicht bei myOpenID, sonst funktionierts natürlich nicht) abmelden und wieder auf "<a href="http://facebook.com">http://facebook.com</a>" gehen und schwups... wird man wieder angemeldet... ganz automatisch... ohne etwas zu tun...

Das klingt ironisch? Ist es auch ein wenig... Facebook scheint sich vor dem Abmelden den <a href="http://simonwillison.net/2009/Jun/13/thefacebookdebacle/">OpenID-Provider in einem Cookie zu merken</a> um, beim erneuten aufrufen der Facebook-Seite, den hinterlegten OpenID-Provider zur automatischen Anmeldung zu verwenden.

Das hört sich ja erstmal nicht schlecht an, aber... das ganze System funktioniert leider nur, wenn das oben erwähnte Cookie vorhanden ist. An jedem neuen PC muss man sich also zuerst bei seinem OpenID-Provider, dann (auf klassische Weise) bei Facebook anmelden um dann, nach einer Abmeldung das Cookie zu erhalten.

Als Erweiterung zu einem klassischen OpenID-Login ist Facebooks Auto-Login sicherlich keine schlechte Idee, die derzeitige Lösung ist aber leider eher verwirrend und keine wirkliche Erleichterung für den klassischen Facebook-Nutzer. Allerdings steht Facebook ja noch am Anfang der Implementation. Es werden sicherlich noch einige Features (<a href="http://www.insidefacebook.com/2009/05/18/facebook-launches-openid-support-users-can-now-login-with-a-gmail-account/">zumal Facebook die OpenID-Registrierung ja schon angekündigt hat</a>) folgen und kreativ ist die bisherige Idee allemal.

Mal gespannt, wie die fertige Implementierung aussieht!

...und bis zur <a href="http://de.wikipedia.org/wiki/Ubiquitous_Computing">allgegenwärtigen OpenID</a> wirds wohl noch ein wenig dauern :)