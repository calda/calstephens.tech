---
layout: post
title: "Blurb 2.0: Spanish, Chinese, and a New Look"
post-id: blurb-2-0-update
thumbnail: thumbnail.png
photoswipe: true
tags: 
  - Apps

screenshots:
  - src: marketing-1.png
    maxres: 1125 × 2436
  - src: marketing-2.png
    maxres: 1125 × 2436
  - src: marketing-3.png
    maxres: 1125 × 2436
    
icons:
  - src: icons.png
    maxres: 950 × 402

---

**Blurb** is a photo editor for iOS that lets you add customizable blurred backgrounds to your photos. I prototyped it at WWDC 2015 and published it on the App Store later that year. This new version is Blurb's first major update, and it brings along support for Spanish and Chinese, a new look, and tons of other small fixes.

{% include photoswipe.html images=page.screenshots max-height=450 %}

<!--break-->

<h4>Translation and Localization</h4>

I had never really considered localizing / translating my apps before. Blurb is small app with relatively few words to translate (only around 100), so it seemed like a good place to start. My friend [Nate](http://natethompson.io/) had started translating his open-source app [Shifty](http://shifty.natethompson.io) into a few other languages, so I was able to learn a good bit about the localization workflow from him. I originally expected it to be complicated, but it turned out to be pretty simple.

The gist of localizing an app is that every piece of text that eventually ends up on-screen needs to pass through the **NSLocalizedString** function. This function takes the input phrase, along with a comment for the translator that describes the context, and swaps it out with the translated version. The translations live in a Localizable.strings file that's basically just a big lookup table. Once the app it set up to use NSLocalizedString correctly, adding support for a new language is as easy as duplicating the Localizable.strings file and sending it off to a translator.

Since this was my first time localizing an app, and since Blurb is reasonably small, I just asked a few of my friends to contribute translations. My friend [Jake](http://jakewaldner.com/) added support for Spanish, and my friend [Kay](https://github.com/lumingyin) added support for Chinese (of the simplified variety). Hopefully now even more people will be able to use Blurb!

<h4>A New Look</h4>

{% include photoswipe.html images=page.icons max-height=200 %}

I designed the original icon in Photoshop several years ago. It was a decent icon at the time, but tastes have changed. It also suffers from some pretty bad gradient banding, so it was definitely time for a change. I designed the new icon in Sketch, flipped the colors around, and made the gradient more vibrant. The updated look made its way into the app as part of a new (and much needed) navigation bar, and it also informed the look of the updated App Store marketing materials. 

Blurb is available for iPhone and iPad. You can download it on the [App Store](https://itunes.apple.com/us/app/blurb-photo-editor/id1055797998?mt=8).

{% include appstore.html link='https://itunes.apple.com/us/app/blurb-photo-editor/id1055797998?mt=8' %}