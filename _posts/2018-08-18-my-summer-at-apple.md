---
layout: post
title: My Summer at Apple
post-id: my-summer-at-apple
thumbnail: wwdc-friends.jpeg
photoswipe: true
tags: 
  - Work
  
header:
  - src: wwdc-friends.jpeg 
    maxres: 4032 × 3024
    caption: "WWDC with other Georgia Tech interns!"
    
xcodeproj:
  - src: xcode dot xcodeproj.png
    maxres: 2238 × 1322
    caption: "Xcode.app and Xcode.xcodeproj"
    
memgraph:
  - src: xcode-mgdb-dark.png
    maxres: 1578 × 1226
    caption: "A sample of the Memory Graph Debugger inspecting some Test app."
    
instruments-dot-app:
  - src: instruments.png
    maxres: 1190 × 1208
    caption: "Instruments dot app"
    
wwdc:
  - src: wwdc-badge.jpeg
    maxres: 4032 × 3024
    caption: "My Apple Engineer badge for WWDC!"
  - src: wwdc-solo.jpeg
    maxres: 3969 × 2964
    caption: "Obligatory shot"
    
cupertino-bike:
  - src: bike.jpeg
    maxres: 4032 × 3024
    caption: "My $99 Target Bike. Good deal!"
  - src: city center.jpeg
    maxres: 4032 × 3024
    caption: "A building in my office complex (Cupertino City Centrer)"
  - src: infinite loop.jpeg
    maxres: 4032 × 3024
    caption: "Infinite Loop (IL1)"
    
sf-bike:
  - src: caltrain.jpeg
    maxres: 4032 × 3024
    caption: "My $99 Target Bike. Good deal!"
  - src: golden gate.jpeg
    maxres: 4032 × 3024
    caption: "A building in my office complex (Cupertino City Centrer)"
  - src: sausalito.jpeg
    maxres: 4032 × 3024
    caption: "Infinite Loop (IL1)"
    
snaps:
  - src: snap1.jpeg
    maxres: 3024 × 4032
    caption: "A delicious iPhone App with dinner."
  - src: snap2.png
    maxres: 838 × 1660
    caption: "Daily commute"
  - src: snap3.jpeg
    maxres: 1125 × 2217
    caption: "Dinner in San Jose"
  - src: snap4.png
    maxres: 836 × 1654
    caption: "🅱️🅱️🅱️🅱️🅱️🅱️🅱️"
    
pilot:
  - src: pilot-1.jpeg
    maxres: 4032 × 3024
    caption: "Our mighty Cessna"
  - src: pilot-2.jpeg
    maxres: 4032 × 3024
    caption: "In the air over SF"
  - src: pilot-3.png
    maxres: 2279 × 1538
    caption: "Downtown SF from the air"
    
---

{% include photoswipe.html images=page.header %}

This summer I interned on the Developer Tools team at Apple! It was an amazing experience, and the sort of thing I had been dreaming about for years.<sup><a href="#[1]">[1]</a></sup> I got the chance to help improve the tools that we use every day, learn more about lower-level Apple technologies, and meet tons of other Apple engineers.

<!--break-->

<h4>Working on Xcode</h4>

{% include photoswipe.html images=page.xcodeproj max-height=300 %}

After a few days of onboarding and getting a copy of the mythical *Xcode.xcodeproj* <sup><a href="#[2]">[2]</a></sup>, I hit the ground running. Xcode is *by far* the largest single codebase I've ever worked with. Compared to relatively modern iOS codebases by [Airbnb](/blog/my-summer-at-airbnb.html) or [MailChimp](/blog/my-semester-at-mailchimp.html), Xcode is a behemoth of Cocoa artistry that draws its lineage from the original [1992](https://en.wikipedia.org/wiki/NeXTSTEP#cite_ref-14) NeXTSTEP Project Builder and Interface Builder. That's *atleast* a few years older than I am. It's hard to say how much, if any, of the original code is still floating around, but the [core concepts](https://www.youtube.com/watch?v=dl0CbKYUFTY) are still there. <sup><a href="#[3]">[3]</a></sup>

One of the small bits I got to work on was a new improvement to the Memory Graph Debugger. As it turns out, if you find something interesting in your app's memory graph, you can actually *export a .memgraph file*. This is super useful for filing comprehensive bug reports (like radars), since it contains the entire memory dump of your process. They also come will all sorts of great information about the process, like its version, uptime, total memory footprint, binary architecture, etc. <sup><a href="#[4]">[4]</a></sup>

Even though this information was included in memgraph files, it never actually got displayed anywhere in Xcode. I banged on this problem a bit during my first few weeks, and now all of this info is shown as a part of the Document Inspector! This feature first shipped in Xcode 10 beta 3. 🎉

{% include photoswipe.html images=page.memgraph max-height=800 %}

<h4>Working on Instruments</h4>

{% include photoswipe.html images=page.instruments-dot-app max-height=300 %}

I did a few other minor patches on Xcode, but otherwise most of the summer was spent working on Instruments. I was in the Developer Tools organization, but most specifically on the **Performance Tools** team. Their biggest focus is Instruments itself, but they work on all sorts of other cool stuff too. The team had big news at WWDC this year, where they got to unveal [Custom Instruments](https://developer.apple.com/videos/play/wwdc2018/410/)! It really changes the game in this department. Instruments is a great platform for profiling the performance of your own apps, and it gets better every year.

I spent most of the summer working on some cool prototypes related to Custom Instruments and data visualization. I can't go into much detail (as is the nature of unreleased projects), but I absolutely learned *so much*. I spent a lot of time working with AppKit and other visualization tools. I also got to actually apply some fun CS theory concepts that had otherwise been relegated to the classroom. Super fun!

<h4>Attending WWDC</h4>

{% include photoswipe.html images=page.wwdc %}

[WWDC](https://developer.apple.com/wwdc/) is every June, which is conveniently right in the middle of a summer internship. Apple Engineers (including interns!) can get week-long badges if they also spend time staffing the labs. I worked the Custom Instruments lab and the Open Swift Hours lab, and got to chat with engineers from around the world who were interested in adopting our new technologies. I also sat-in on a bunch of sessions, cheered on my team members during their talks, caught up with old friends, and made new ones! I [had been to WWDC before](https://twitter.com/calstephens98/status/1005484174357061632), but this one was the most fun *by far*.

<h4>Other fun stuff</h4>

I lived in Cupertino / the bay area again for three months, and I didn't just sit around at home on the weekends. I picked up a bike on my first day, so I spent a lot of time biking around Cupertino.

{% include photoswipe.html images=page.cupertino-bike %}

I took the train up to San Francisco a lot. Biking up to Sausalito was a great day-trip, so I did that a few times! I also got to go to [Corgi Con](https://twitter.com/calstephens98/status/1008188610401611776) this year (after missing out last year).

{% include photoswipe.html images=page.sf-bike %}

I spent a lot of time hanging out with my roommates [Mert](https://twitter.com/mertdumenci), [Anthony](https://twitter.com/AAgatiello), and Hunter. There was more than enough beer to go around 🍻

{% include photoswipe.html images=page.snaps %}

I took a pilot lesson with [@NachoSoto](https://twitter.com/NachoSoto)!! I've always wanted to get my pilot's license, so this was an awesome experience. We flew from [HWD](https://twitter.com/NachoSoto) over to SF and around the bay. I'm seriously thinking about doing more lessons and getting licensed after I graduate.

{% include photoswipe.html images=page.pilot %}

Overall an amazing summer! I have one more year at Georgia Tech, and then I'll come back to the Bay Area for good.

<h4>Footnotes</h4>

<div style="font-size: small; color:gray; margin-bottom:14px;">
<i>Obligatory note:</i> I no longer work at Apple and currently don't have plans to return. This post does not represent the thoughts, opinions, or experiences of anyone but myself, and doesn't contain any Apple Confidential information.
</div>

<div style="font-size: small; color:gray; margin-bottom:14px;">
<sup><a name="[1]">[1]</a></sup> In the Georgia Tech CS 1100 "Freshman Leap Seminar", we had to write a letter to ourselves 5 years in the future. We were supposed to mention our dreams over that timeframe, and I remember putting down "Work at Apple".
</div>

<div style="font-size: small; color:gray; margin-bottom:14px;">
<sup><a name="[2]">[2]</a></sup> That screenshot isn't the real Xcode.xcodeproj. <i>File > New Project > macOS > Cocoa App > "Xcode"</i>.
</div>

<div style="font-size: small; color:gray; margin-bottom:14px;">
<sup><a name="[3]">[3]</a></sup> I didn't go hunting for "the oldest living source code left in Xcode" or anything, but I did come across code older than I am when I was working on a patch for some other System framework.
</div>

<div style="font-size: small; color:gray; margin-bottom:14px;">
<sup><a name="[4]">[4]</a></sup> <i>.memgraph</i> files are just Binary Plists, so it's relatively easy to pop them open and see this information for yourself.
</div>
