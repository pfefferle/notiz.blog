---
ID: 4301
post_title: Twitter Cards
author: Matthias Pfefferle
post_date: 2012-06-22 15:49:55
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2012/06/22/twitter-cards/
published: true
---
Anfang der Woche hat Martin Weigert schon über <a href="http://netzwertig.com/2012/06/19/twitter-von-einer-simplen-plattform-zur-destination-fuer-multimediainhalte/">Twitters Pläne</a>, die eigenen Tweets mit noch mehr Medieninhalten zu erweitern, geschrieben:

<blockquote>Immer mehr Partnerseiten können zusätzliche multimediale Inhalte im Kontext von Tweets darstellen. Ganz eindeutig ist bisher nicht, wohin diese Reise für Twitter geht.</blockquote>

Aber ich habe mir nichts weiter dabei gedacht... Immerhin macht das Twitter ja schon seit einer ganzen Weile und ich meine mich zu erinnern, irgendwo gelesen zu haben, dass sie dazu <a href="http://oembed.com/">oEmbed</a> einsetzen... Also alles in bester "OpenWeb"-Ordnung :)

Aber, Geek der ich bin, hab ich mir gestern zufällig einen Quelltext angeschaut in dem ich auf folgendes entdeckt habe:

<pre><code>&lt;meta name="twitter:card" content="summary"&gt;
&lt;meta name="twitter:url" content="..."&gt;
&lt;meta name="twitter:title" content="..."&gt;</code></pre>

...und nach kurzem googlen bin ich auf die <a href="https://dev.twitter.com/docs/cards"><strong>Twitter Cards</strong></a> gestoßen, Twitters eigenes, kleines <a href="http://ogp.me/"><strong>Open Graph Protocol</strong></a>. Mit den <strong>Twitter Cards</strong> bekommen Seitenbetreiber ein Set an Meta-Tags an die Hand, und Twitter kann diese Informationen nutzen um die tweets mit den oben erwähnten Mediendaten anzureichern.

<img src="http://notiz.blog/wp-content/uploads/2012/06/twitter-card-web-summary.png" alt="Example Twitter Card" title="Example Twitter Card" width="522" height="272" class="size-full wp-image-4333" />

...und ich wollte mich gerade darüber aufregen, warum Twitter dazu eine eigene Meta-Sprache erfindet, da bin ich in der <a href="https://dev.twitter.com/docs/cards">Doku</a> ironischerweise auf folgendes gestoßen:

<blockquote>You'll notice that Twitter card tags look similar to OpenGraph tags, and that's because they are based on the same conventions as the Open Graph protocol. If you're already using OpenGraph to describe data on your page, it’s easy to generate a Twitter card without duplicating your tags and data. When the Twitter card processor looks for tags on your page, it first checks for the Twitter property, and if not present, falls back to the supported Open Graph property. This allows for both to be defined on the page independently, and minimizes the amount of duplicate markup required to describe your content and experience.</blockquote>

"Ok", dachte ich... vielleicht reichen die <em>Open Graph</em> Properties ja nicht aus um alle Informationen, die Twitter braucht, abzubilden. Also hab ich mir mal die Mühe gemacht sie zu vergleichen:

<table class="table table-striped">
    <thead>
      <tr>
        <th>Twitter Cards</th>
        <th>Open Graph Protocol</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><code>twitter:card</code></td>
        <td><code>og:type</code></td>
      </tr>
      <tr>
        <td><code>twitter:site</code></td>
        <td><code>og:site_name</code></td>
      </tr>
      <tr>
        <td><code>twitter:url</code></td>
        <td><code>og:url</code></td>
      </tr>
      <tr>
        <td><code>twitter:description</code></td>
        <td><code>og:description</code></td>
      </tr>
      <tr>
        <td><code>twitter:title</code></td>
        <td><code>og:title</code></td>
      </tr>
      <tr>
        <td><code>twitter:image</code></td>
        <td><code>og:image</code></td>
      </tr>
      <tr>
        <td><code>twitter:image:width</code></td>
        <td><code>og:image:width</code></td>
      </tr>
      <tr>
        <td><code>twitter:image:height</code></td>
        <td><code>og:image:height</code></td>
      </tr>
      <tr>
        <td><code>twitter:player</code> oder <code>twitter:player:stream</code></td>
        <td><code>og:video</code> oder <code>og:audio</code></td>
      </tr>
      <tr>
        <td><code>twitter:player:width</code></td>
        <td><code>og:video:width</code></td>
      </tr>
      <tr>
        <td><code>twitter:player:height</code></td>
        <td><code>og:video:height</code></td>
      </tr>
   </tbody>
 </table>

Es lässt sich also prinzipiell alles mit dem <em>Open Graph Protocol</em> abbilden, es fehlen lediglich die Felder <code>twitter:site:id</code> und <code>twitter:creator:id</code>. Aber wegen diesen zwei Feldern muss man doch nicht das ganze Format "kopieren". Es reicht doch ein kleiner Absatz, wie man den <em>Open Graph</em> mit den proprietären Werten erweitert... So wie das auch <a href="https://developers.facebook.com/docs/opengraphprotocol/">Facebook</a> praktiziert:

<pre><code>&lt;html xmlns="http://www.w3.org/1999/xhtml"
      xmlns:og="http://ogp.me/ns#"
      xmlns:fb="https://www.facebook.com/2008/fbml"&gt;
      <strong>xmlns:twitter="https://dev.twitter.com/docs/cards"&gt;</strong>
  &lt;head&gt;
    &lt;title&gt;The Rock (1996)&lt;/title&gt;
    &lt;meta property="og:title" content="The Rock"/&gt;
    &lt;meta property="fb:admins" content="USER_ID"/&gt;
    <strong>&lt;meta property="twitter:site:id" content="@USER_ID"/&gt;</strong>
    ...
  &lt;/head&gt;
  ...
&lt;/html&gt;
</code></pre>

Hoffentlich überlegt sich das Twitter noch einmal... Wenn nicht, wird dank dieser (und folgender) Redundanzen der <code>&lt;head /&gt;</code> einer Webseite in ein paar Jahren mehr Informationen beinhalten wie der <code>&lt;body /&gt;</code>.

...welch ein Over-<code>&lt;head&gt;</code> :)