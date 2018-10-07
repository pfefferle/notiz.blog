---
ID: 13777
post_title: Interview mit Aaron Parecki
author: Matthias Pfefferle
post_excerpt: ""
layout: post
permalink: >
  https://notiz.blog/2015/07/23/interview-mit-aaron-parecki/
published: true
post_date: 2015-07-23 21:57:05
---
Für das <a href="http://screengui.de">SCREENGUIDE Magazin</a> (<a href="http://screengui.de/26">Ausgabe 26</a>) wurde <a href="https://aaronparecki.com">Aaron Parecki</a> zum Thema <em><a href="http://indiewebcamp.com">Indie Web (Camp)</a></em> interviewt. Das abgedruckte Interview ist aus Platzgründen und für ein besseres Verständnis aber leicht gekürzt und ins deutsche übersetzt worden.

Mit freundlicher Genehmigung von <a href="http://textformer.de">Nicolai Schwarz</a> (Projektleiter SCREENGUIDE Magazin) und Aaron Parecki, darf ich euch hier das Original präsentieren:

<strong>SCREENGUIDE: Hi Aaron, what are the reasons for founding IndieWeb respectively organizing the first IndieWebCamp?</strong>

[caption id="attachment_13813" align="alignright" width="200"]<img src="//notiz.blog/wp-content/uploads/2015/07/aaronpk-geoloqi.jpg" alt="Aaron Parecki, @aaronpk CTO bei Esri R&#38;D Center, Portland Mitgründer IndieWeb &#38; IndieWebCamp" width="200" height="302" class="size-full wp-image-13813" /> Aaron Parecki, @aaronpk<br />CTO bei Esri R&#38;D Center, Portland<br />Mitgründer IndieWeb &#38; IndieWebCamp[/caption]

Aaron Parecki: In 2010, <a href="http://tantek.com">Tantek Çelik</a> and I attended the "Federated Social Web Summit" in Portland, Oregon. After the event, we walked away feeling somewhat dissatisfied, and decided we wanted to take a slightly different approach. We wanted to focus on:

<ul>
<li>creators instead of talkers - prioritize and encourage people who create things (design, UX, or code) instead of just talking about it</li>
<li>use your own tools - if you are building something you expect other people to use, you should be using it yourself on your own website</li>
<li>own your data - own your content online by publishing it first on your own website, and afterwards copying it to silos like Twitter and Facebook</li>
</ul>

We took these and several other <a href="http://indiewebcamp.com/principles">principles</a>, joined forces with <a href="http://caseorganic.com">Amber Case</a> and  <a href="http://crystalbeasley.com">Crystal Beasley</a>, and organized the first IndieWebCamp unconference in 2011. The goal of the conference was to create a space for like-minded individuals to experiment with owning their content and identity on the Web.

<strong>SG: In 2011 there was one IndieWebCamp in Portland. For 2015 there are nine different Camps planned. Did you expect that kind of success?</strong>

AP: I never expected there would be IndieWebCamps in nine different cities so quickly! It's been a pleasant surprise to see so many people excited about it, and it's been fun to visit other cities to help organize the camps as well!

<strong>SG: Do you have any idea how many people have implemented IndieWeb-features on their website? (Maybe you have a number how many sites did log into indiewebcamp.com or how many are using Bridgy?)</strong>

AP: It's great to see new people show up in our IRC channel or make their first POSSE post from their website, and I'm constantly amazed at how many people show up every day! It's hard to get a good sense of how many people have implemented indieweb features, since by definition, there is no central directory or registry we can look at. However, there are over 170 people who have added their websites to our "IRC People" page which is used to display profile photos in our <a href="https://indieweb.org/irc/today">IRC logs</a>. If you look at the stats of Bridgy, a popular service that sends webmentions from activity on various silos like Twitter and Facebook, there are over 1.200 people signed up!

<strong>SG: What is so fascinating about the community?</strong>

AP: The best part about the community is how positive and productive everyone is! The community is extremely friendly, we often get visitors in our IRC channel who have some simple questions and lots of people jump to help them out. People start out by building their own web presence, either by writing their own custom software or installing someone else's software such as Wordpress or Known. Having everyone working on their own websites leaves a lot of room for experimentation and trying out multiple approaches to solving problems. We encourage a diversity of approaches and implementations. This makes the IndieWeb stronger and more resilient than any one approach or project.

<strong>SG: You wrote the software p3k for your own website aaronparecki.com. What does p3k do?</strong>

AP: <a href="http://p3k.io">p3k</a> is the name of the software that powers my website, <a href="http://aaronparecki.com">aaronparecki.com</a>. It allows me to create many different kinds of posts, everything from simple text notes and photos, as well as my bike rides and what I'm eating. All the posts are marked up with Microformats so they show up in <a href="http://indiewebcamp.com/reader">peoples' readers</a>. If you write a reply to one of my posts, you can send a webmention and your reply will show up as a comment. p3k also supports <a href="http://micropub.net">Micropub</a> which means I can post from many other apps.

While some people choose to develop their websites or CMSs entirely as open source, I've been taking a slightly different approach while building p3k for myself. Instead of building an open source CMS, and expecting people to use it the way I've built it, I instead develop small components and libraries that I use in my website, and I make those open source. For example, you can use the <a href="https://github.com/indieweb/php-comments">php-comments library</a> I've written to parse comments from external websites, or you can use the <a href="https://github.com/indieweb/date-formatter-php">date-formatter library</a> to render dates and date ranges in a human-readable format, so you'd see "December 9-12, 2015" instead of "2015-12-09 through 2015-12-12".

This approach allows me to make small pieces that are more likely able to be useful to others, and avoid the hassles of building a polished install and configuration process. In fact many of these libraries are in use by other indieweb sites currently!

<strong>SG: The IndieWeb focuses on owning your content. How do you use social media personally?</strong>

AP: I use social media similar to most people, to keep in touch with my friends. I post photos, notes and articles on my website, and syndicate them to silos like Twitter or Facebook. When I'm reading other peoples' websites or Twitter feeds, I reply to posts from my site, or "like" them from my site. For an example of what I mean by "liking" something from my site, you can see all the things I've "liked" here: <a href="http://aaronparecki.com/likes">aaronparecki.com/likes</a> I enjoy seeing photos my friends are sharing, so I follow people on Instagram or see photos they post on their own sites.

I don't normally read the full timelines of sites like Twitter or Facebook, since there is often too much content to keep up on. Instead, I typically read things by searching specific hashtags or terms. In fact I have a persistent Twitter search running all the time that sends results to several IRC channels I am in. I have searches running for projects I'm involved with, such as "indiewebcamp" or "webmention", as well as for my name or other more private search terms. This makes it easy for me to follow topics I care about without getting lost in the noise of all the other posts.

<strong>SG: What are currently the big (advanced) topics for the IndieWeb?</strong>

AP: This year is shaping up to be the year of the <a href="http://indiewebcamp.com/reader">Reader</a>. Now that there are quite a lot of people publishing content on their own sites, the missing piece is having one place where you can read the posts of everyone you're following, and reply to the posts from within the same interface. Facebook and Twitter have shown us that an integrated reading and commenting experience is what people really want, and this is something that previous readers such as Google Reader didn't do.

There has already been some great progress made on readers this year, and lots of interest from people using them! Once there are a few readers to choose from, it will be easy to avoid going to Facebook or Twitter to read things at all! The great part of the way these readers are being built is that you can use them to reply to the things you're reading, but the replies are actually sent from your own site! This is made possible by Micropub, so if your site has a Micropub endpoint, readers can use it to create posts on your site. For example, I wrote this reply inside a reader app, and my site even shows the app used to post it: <a href="http://aaron.pk/r4_i5">http://aaron.pk/r4_i5</a>

There are also many Micropub apps in the works right now, which will enable you to post to your site from a mobile app, desktop app, or other web apps. Why limit yourself to your built-in posting interface such as the Wordpress admin page, when you could be using more streamlined apps for posting photos or audio! Micropub is exciting because it enables a whole ecosystem of apps to be developed, so that people have many choices for how to post content to their own websites.