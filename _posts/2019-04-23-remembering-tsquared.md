---
layout: post
title: 'Remembering T-Squared'
post-id: remembering-tsquared
thumbnail: thumbnail.jpg
photoswipe: true
tags: 
  - Apps
  
tsquare:
  - src: desktop-web.png
    maxres: 1504 × 1004
    caption: "T-Square's standard desktop web interface."
  - src: mobile-web.png
    maxres: 750 × 1334
    caption: "T-Square's standard mobile web interface."  
    
tsquared:
  - src: login-undecorated.png
    maxres: 750 × 1334
    caption: "T-Squared's login screen"
  - src: courses-undecorated.png
    maxres: 750 × 1334
    caption: "T-Squared's course detail screen"
  - src: grades-undecorated.png
    maxres: 750 × 1334
    caption: "T-Square's grades screen"
    
rip:
  - src: goodbye.png
    maxres: 1048 × 614
    caption: "RIP T-Square: 2005 - 2019"
  - src: RIP.png
    maxres: 616 × 502
    caption: "RIP T-Squared: November 2015 - April 2019"

---

I graduate from [Georgia Tech](https://en.wikipedia.org/wiki/Georgia_Institute_of_Technology) next week, so I thought now would be a great time to revist one of the first projects I worked on as a student here.

### T-Square

When I started at Tech back in 2015, we used an online learning management system called [T-Square](https://t-square.gatech.edu/portal). It was the platform we used for all of our courses, and it included things like our assignments, grades, resources, and instructor announcements. T-Square was built in the early-2000s, and it looks the part. The mobile site is a particularly bad offender, with no visual styling to speak of. After dealing with it for my first [two weeks](https://github.com/calda/T-Squared/commit/5c0e0e7c5cc9ab749f72c840503132acbd08f558) of class, I decided I wanted to try and do something about it.

{% include photoswipe.html images=page.tsquare  max-height='400' class='shadow' %}

<!--break-->

### Creating T-Squared

I spent the majority of my first semester working on [T-Squared](https://github.com/calda), a native iOS client for the T-Square platform.

{% include photoswipe.html images=page.tsquared class='shadow' %}

T-Square doesn't have an official API, so T-Squared fetched all of its content by scraping the platform's mobile site. The app included all of the important information you'd expect &mdash; assignments, resources, and grades for all of your classes &mdash; but I also got to build some interesting features that didn't exist on T-Square itself. One of its biggest killer features was that it would calculate your total grade in a class (T-Square didn't do that for some reason, even though it had all of the data on-hand). It also let you add grade predictions so you could see how they would affect your overall course grade (a "what if" calculator).

Over the course of its lifetime, T-Square was downloaded over 12,000 times and used by students *over 2,000,000 times!* Back when it was in its prime, it wasn't uncommon to see people using it a few rows up in big lecture halls. 

### Phasing Out T-Square

But T-Square was evantually replaced with a new system called [Canvas](https://itunes.apple.com/us/app/canvas-student/id480883488?mt=8), and it was phased out completely after the Fall 2018 semester. I finally got around to de-listing T-Squared while I was writing this post (April 2019). It was a very important part of my early college life, so I'm definitely sad to see it go. Thanks for the memories!

{% include photoswipe.html images=page.rip class='shadow' %}

