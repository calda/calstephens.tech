---
layout: post
title: My Semester at MailChimp
post-id: my-semester-at-mailchimp
thumbnail: team.jpg
photoswipe: true
tags: 
  - Work
    
mobile-ad-editing:
  - src: demo-1.png
    maxres: 1125 × 2436
    caption: "The Ad Detail screen, which shows information about your ad. This used to be readonly on Mobile, but it's now fully editable on Mobile."
  - src: demo-2.png
    maxres: 1125 × 2436
    caption: "A hybrid screen reusing components from the desktop ad editing flow."
  - src: demo-3.png
    maxres: 1125 × 2436
    caption: "Publish Ad confirmation screen, with a fun animation in classic MailChimp style."
    
responsive:
  - src: web.png
    maxres: 2280 × 1524
    caption: "The Ad Editing flow on desktop web."
    
freddies:
  - src: freddies-1.jpg
    maxres: 1125 × 2217
  - src: freddies-2.jpg
    maxres: 1125 × 2217
  - src: freddies-3.jpg
    maxres: 1125 × 2217
  - src: freddies-4.jpg
    maxres: 1125 × 2217
    
previously:
  - src: 2016.jpg
    maxres: 1222 × 983
    caption: "MailChimp's 2016 intern class"
  - src: presentation-1.jpg
    maxres: 2118 × 1569
    caption: "My 2016 intern presentation"
    
---

This semester, I worked part-time on the mobile team at [MailChimp](htts://mailchimp.com) here in Atlanta. This was my second time at MailChimp (I interned on the same team in 2016), and I had even more fun this time around!

MailChimp used to focus exclusively on email, but they've been broadening their horizons quite a bit lately. You can now create online ads, landing pages, and even [*physical postcards*](https://mailchimp.com/features/postcards-beta/) through MailChimp! While I was there this Spring, I worked on a new flow for our [mobile app](https://mailchimp.com/features/mailchimp-mobile/) that lets users create and manage their Facebook ads right on their phone. 

<!--break-->

<h4>Mobile Ad Editing</h4>

MailChimp released [Facebook Ad Campaigns](https://mailchimp.com/features/facebook-ads/) in 2017, but the feature was mostly limited to the web. You could see them and review their performance on mobile, but you had to use the desktop site to create or edit an ad. I worked closely with the Ads team and one of our other mobile engineers to bring the full editing experience to mobile.

{% include photoswipe.html images=page.mobile-ad-editing class='shadow' %}

One of the interesting decisions that got made was to heavily reuse components from the existing web flow. On the Ad Detail screen, tapping any of the fields pops open a hybrid detail that uses responsive pieces from the original desktop interface. For example, if you take a look at the desktop Ad editor flow, you'll see the same exact Audience editor (just a bit rearranged): 

{% include photoswipe.html images=page.responsive class='shadow' %}

<p style="margin-bottom: 15px">Each of these details are rather complicated, so reusing the web components instead of rebuilding them from scratch was a big win on two fronts:</p>

 1. We reduced the need for new APIs endpoints. The web interface already worked as-expected, but a fully-native implementation would have required new public API endpoints.
 2. Rather than rebuilding the existing editor UI twice (once for iOS and once for Android), we had time to focus on other parts of the experience that were unique to mobile. 

Since the overall engineering effort was reduced quite a bit, we were able to get this project done a lot faster than otherwise possible! This feature was released in MailChimp Mobile 4.9, which came out in July 2018.
 
<h4>Freddies</h4>

I think MailChimp is the most fun (funnest?) place to work in Atlanta. Everyone is a joy to work with, and they have some of the best swag I've ever seen. Their [vinyl freddies](https://blog.mailchimp.com/behind-our-surprise-toy-giveaway/) are my favorite by far. Freddie is their mascot, and they have these vinyl figures that come in dozens of varieties. I collected ~10 in my six months at MailChimp, and they're my prized possessions. 
 
{% include photoswipe.html images=page.freddies class='more-bottom-padding' %}

<h4>Previously</h4>

I also worked at MailChimp in Summer 2016. That was my first real job, right after my freshman year at Georgia Tech. I worked on some cool stuff that summer, too &mdash; I built a prototype iOS app to help new users grow their email lists through social media, and made lots improvements to our ChimpKit Objective-C API.

{% include photoswipe.html images=page.previously %}

I really enjoyed working at MailChimp &mdash; both times! I made a lot of friends, and I'm glad I got to work on some cool stuff while I was there.
 
