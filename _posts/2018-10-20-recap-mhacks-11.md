---
layout: post
title: 'Recap: MHacks 11'
post-id: recap-mhacks-11
thumbnail: thumbnail.jpg
photoswipe: true
tags: 
  - Hackathons
  
diagram:
  - src: diagram.png
    maxres: 1371 × 872
    caption: "A diagram of the Recorder Hero system"

music:
  - src: sheet-music.jpg
    maxres: 732 × 555
    caption: "A sample of sheet music for Hot Cross Buns"
  - src: recorder-chart.jpg
    maxres: 269 × 350
    caption: "Example of 'recorder fingerings'"

gameplay-1:
  - src: main-menu.png
    maxres: 1168 × 1612
    caption: "Recorder Hero's Main Menu, with six song choices and three difficulty levels."
  - src: hot-cross-buns.png
    maxres: 1168 × 1612
    caption: "The first few notes of Hot Cross Buns &mdash; a Recorder staple for generations."
    
gameplay-2:
  - src: pirates-hard.png
    maxres: 1168 × 1612
    caption: "'Pirates of the Carribbean Theme' on Hard"
  - src: mario-hard.png
    maxres: 1168 × 1612
    caption: "'Super Mario Theme' on Hard"

gif:
  - src: gif.gif
    maxres: 1062 × 592
    caption: "A short .gif clip of Recorder Hero gameplay"
    
friendship:
  - src: detroit1.jpeg
    maxres: 1600 × 2130
    caption: "'The Spirit Of Detroit'"
  - src: detroit2.jpg
    maxres: 2000 × 1500
    caption: "The Detroit skyline from Windsor, Ontario, Canada (on the other side of the Detroit river)"
    
---

This weekend I was at MHacks 11 in Ann Arbor, Michigan. We had an awesome time building a game called **Recorder Hero**, and got to use some cool technologies that I've been wanting to try out for a long time!

<h4>The Project</h4>

{% include youtube.html url='https://www.youtube.com/embed/7yrLTQhz80M' %}

**Recorder Hero** is like [Guitar Hero](https://youtu.be/zdkdvTQP1Us?t=13), but for the Recorder. You know -- that instrument that [every kid in America](https://www.atlasobscura.com/articles/why-every-kid-in-america-learns-to-play-the-recorder) learned to play in elementary school. The game has a playlist of hit songs, ranging from *Hot Cross Buns* to *Party Rock Anthem*, that you can learn to play on a handheld digital recorder (your iPhone).

<!--break-->

<h4>Architecture</h4>

{% include photoswipe.html images=page.diagram max-height=425 %}

Recorder Hero, as a complete system, runs on two devices at once. The handheld digital recorder is an iPhone app with on-screen buttons that mirror the layout of an actual recorder. Meanwhile, the Gameplay interface is a Python app that loads up a serialized sheet music representation, renders the track timeline, and plays the recorder notes. 

One of the big challenges of a complex multi-device setup like this is, of course, getting the devices to talk to eachother. One potential implementation could do this wirelessly &mdash; either by setting up a local Bluetooth connection, or by putting a web-server in the middle. Hackathon Wi-Fi is notoriously spotty, though, and we've gotten burned before by trying to rely on a stable connection for our hacks. Latency is also a big issue for a game like this, because the user experience would really deteriorate if there was a networking delay.

Instead, we opted to communicate over USB via a lighting cable plugged in to the laptop and the iPhone. There's a wonderful Objective-C library called [PeerTalk](https://rsms.me/peertalk/) that makes it really easy to set up a TCP server that communicates over USB between an iOS app and a companion macOS app. Using that library, the iOS app sends a one-hot-encoded bitstring of the pressed buttons (the simulated recorder holes) to a macOS helper app running on the connected laptop.

The only problem, though, is that PeerTalk only gets the data onto a macOS app. The gameplay interface is running in a Python app, so we needed another communication layer. To solve this problem, we set up a pretty rudimentary one-way Socket between the macOS helper app and the Python app. The macOS app uses this Socket to forward any messages it receives to the Python app. With all of those pieces in place, we have a real, wired, handheld digital recorder with almost no latency. Pretty cool!

<h4>Gameplay</h4>

After spending the first half of the hackathon working on the input architecture, we got to spend the second half building out the actual gameplay experience. 

{% include photoswipe.html images=page.gameplay-1 %}

The biggest piece of a game like Recorder Hero is the music itself. We scoured the internet for Recorder sheet music that's simple enough to play without much experience, but recognizable enough that you could still jam out to it. A recorder doesn't have a very wide range (and can't play sharp or flat notes, either), so that limits the songs that you can play. We settled on a playlist of six songs including recorder classics like *Hot Cross Buns*, pop hits like *Party Rock Anthem*, and classical score like the *Pirates of the Caribbean theme*. 

{% include photoswipe.html images=page.music %}

We set up a mapping between recorder button combinations and musical notes, complete with audio files generated from a [recorder synth](https://www.youtube.com/watch?v=-OtqhPpZ_MY). One interesting problem that we ran in to is that the iPhone can only detect five touches at a time. This is a limitation of the hardware itself, so it's not something that can be hacked around with some clever software. Unfortunately, that meant there would be some notes that couldn't be correctly represented by our digital recorder (lower C requires seven fingers, for example). There are also some note combinations that are only distinguished by either covering or not covering the back hole (which our digital recorder doesn't have), so we have to come up with our own button combinations for those notes.

{% include photoswipe.html images=page.gameplay-2 %}

After we had the game up an running, we ran into some practical limitations. Songs with small ranges like *Hot Cross Buns* and *Party Rock Anthem* were fairly easy to play, but songs with wide ranges turned out to be unreasonably difficult. We tried to stay as true to a real recorder button layout as possible, but button combinations for notes in the top octave get really complicated really quickly. It may be possible to switch between these quickly when holding an actual recorder with physical holes to guide your fingers, but it was pretty impractical on a smooth slab of glass.

{% include photoswipe.html images=page.gif %}

The game as a whole, though, is very fun! Most of the songs can be played accurately with some practice. And, for the most part, you're learning real recorder skills! [Video Demo](https://www.youtube.com/watch?v=7yrLTQhz80M)

<h4>The Team</h4>

{% include photoswipe.html images=page.friendship %}

I went to MHacks with my friend [Jake](http://jakewaldner.com). This was our fourth hackathon together! Others included [DerbyHacks 2017](https://devpost.com/software/telephone-pictionary) in Louisville, [UB Hacking 2017](/blog/recap-ub-hacking-2017.html) in Buffalo, and [MinneHack 2018](/blog/minnehack-2018.html) in Minneapolis. On this trip, we also got to spend time in Downtown Detroit and Windsor, Ontario (across the river).