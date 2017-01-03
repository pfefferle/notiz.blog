---
ID: 681
post_title: Writing Blog-Comments using an hCard
author: Matthias Pfefferle
post_date: 2008-01-04 12:23:50
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2008/01/04/wp-hcard-commenting/
published: true
---
I wrote a small Plugin that allows your users to easily fill out the comment forms of your WordPress Blog using an <a href="http://microformats.org/wiki/hCard">hCard</a>. I got this Idea from SignUp pages like <a href="https://www.bragster.com/signup">bragster.com</a> or <a href="http://getsatisfaction.com/people/new">getsatisfaction.com</a>.

After the installation, you get a small (import hCard) link behind your URL field in the comment form (if not, use <code>&lt;?php hcard_commenting_link() ?&gt;</code>).

<img class="aligncenter" src='http://notiz.blog/wp-content/uploads/2008/01/hcard-commenting-step1.jpg' alt='hCard Commenting Step 1' />

If you want to write a comment using this festure, you simply have to fill out the "Website" field with an URL to one of your hCards and to klick the "import hCard" link.

<img class="aligncenter" src='http://notiz.blog/wp-content/uploads/2008/01/hcard-commenting-step2.jpg' alt='hCard Commenting Step 2' />

...and thats it.

<img class="aligncenter" src='http://notiz.blog/wp-content/uploads/2008/01/hcard-commenting-step3.jpg' alt='hCard Commenting Step 3' />

To try out this plugin, you can use my comment form.

One of the next steps would be some kind of avatar feature using the hCard <code>photo</code> (thanks to <a href="http://suda.co.uk">Brian Suda</a> for the idea).

<p class="download">You can download this version on the WordPress Plugin area: <a href="http://wordpress.org/extend/plugins/hcard-commenting/">http://wordpress.org/extend/plugins/hcard-commenting/</a></p>