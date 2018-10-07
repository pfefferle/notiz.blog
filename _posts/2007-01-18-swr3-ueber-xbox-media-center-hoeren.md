---
ID: 293
post_title: SWR3 über XboxMediaCenter hören
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2007/01/18/swr3-ueber-xbox-media-center-hoeren/
published: true
post_date: 2007-01-18 22:06:52
---
<!-- wp:paragraph -->
<p>Wenn ihr Webradios, wie z.B. SWR1 oder SWR3 über euer <a href="http://www.xboxmediacenter.com/">XboxMediaCenter</a> hören wollt, kopiert einfach einen der folgenden Texte in eine Datei mit der entsprechenden Endung:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>PLS</strong>
</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">[playlist]
PlaylistName=SWR Radios
File1=
rtsp://213.254.239.61/farm/*/encoder/swr/swr1/live_rp.rm
Title1=SWR 1 RP :: Eins gehört gehört.
Length1=-1
File2=
rtsp://195.52.221.172/farm/*/encoder/swr3/livestream.rm
Title2=SWR 3 :: Mehr Hits. Mehr Kicks. Einfach SWR3
Length2=-1
NumberOfItems=2
Version=2</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>(Bsp.: swr.pls)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>M3U</strong>
</p>
<!-- /wp:paragraph -->

<!-- wp:preformatted -->
<pre class="wp-block-preformatted">#EXTM3U
#EXTINF:-1,SWR3 Webradio
rtsp://195.52.221.172/farm/*/encoder/swr3/livestream.rm
#EXTINF:-1,SWR1 RP Webradio
rtsp://213.254.239.61/farm/*/encoder/swr/swr1/live_rp.rm</pre>
<!-- /wp:preformatted -->

<!-- wp:paragraph -->
<p>(Bsp.: swr.m3u)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Dann das ganze per FTP in euren "Playlist" Ordner und fertig.</p>
<!-- /wp:paragraph -->