---
layout: post
title: "Recap: UB Hacking 2017"
post-id: recap-ub-hacking-2017
thumbnail: mario-sketchbook.png
photoswipe: true
tags: 
  - Hackathons

demo:
  - src: mario-sketchbook.png
    maxres: 873x571

friendship:
  - src: niagara-falls.jpg
    maxres: 4032x3021
---

Last weekend I was at UB Hacking 2017 in Buffalo, NY. It was a 24-hour hackathon at the University of Buffalo, and the trip was one of my favorites of the semester!

<h4>The Project</h4>

{% include photoswipe.html images=page.demo class='shadow' %}

We built an augmented reality Android app called **Mario Sketchbook**. The app itself is a pen-and-paper platformer. On paper, the user can draw a game world with their own desired objects and platforms. The app captures their hand-drawn world and adds Mario to it! Mario can run and jump around on the drawn shapes.

<!--break-->

The world capture system uses OpenCV to detect rectangular pieces of paper, perspective-correct the scene, and then identify the geometric contours of each platform. Once we know the geometry of the scene, we can insert Mario, apply physics, and perform collision detection.

We ran into some challenges along the way. The final version of the app uses a pseudo-AR approach to overlay a tilted image of the interactive game scene over the camera output. We did build a version of the app that actually re-skews the game scene onto the exact geometry of the paper (which would have been true AR), but faced performance bottlenecks that made the game unplayably slow.

<h4>Video Demo</h4>

{% include youtube.html url='https://www.youtube.com/embed/sckjbGo1e6I' %}

<h4>The Team</h4>

{% include photoswipe.html images=page.friendship class='shadow' %}

I went to UB Hacking with my friend [Jake](http://jakewaldner.com). We were roommates during our freshman and sophomore year, and we're still good friends. We travel together whenever we get the chance. After the hackathon, we spent a couple of days in Niagara Falls, Ontario. A little cold, but overall fun place!



