---
layout: post
title: 'Inflation Calculator now available in 14 languages'
post-id: inflation-calculator-4-0
thumbnail: thumbnail.png
photoswipe: true
tags: 
  - Apps

header:
  - src: arabic.png
    maxres: 782 × 1536
    caption: "Inflation Calculator is now available in Arabic"
  - src: spanish.png
    maxres: 782 × 1536
    caption: "Inflation Calculator is now available in Spanish"
  - src: chinese.png
    maxres: 782 × 1536
    caption: "Inflation Calculator is now available in Chinese"
    
appstore:
  - src: appstore.png
    maxres: 1015 × 720
    caption: "Inflation Calculator's App Store marketing material"
    
heros:
  - src: frenchhero.png
    maxres: 677 × 720
    caption: "Inflation Calculator's French App Store hero image"
  - src: koreanhero.png
    maxres: 825 × 720
    caption: "Inflation Calculator's Korean App Store hero image"
    
    
---

**Inflation Calculator 4.0** is [now available](https://apps.apple.com/app/inflation-calculator/id926713392) on the App Store. Along with data for 2020, this update adds support for 13 new languages including Spanish, French, Chinese, Hindi, Arabic, and more!

<div style="padding-top:20px; padding-bottom:20px;">
{% include photoswipe.html images=page.header max-height=400 %}
</div>

<!--break-->

Inflation Calculator was originally released in 2014 for the US Dollar. I added support for 21 more international currencies back in 2017, but the app was still only available in English. It hasn't taken off internationally (over 90% of downloads since then have been in English-speaking countries) but hopefully this update will help turn things around. Inflation Calculator now supports the local currency *and the native language* of **billions** more users around the world.

<div style="padding-top:20px; padding-bottom:20px;">
{% include photoswipe.html images=page.appstore max-height=440 %}
</div>

Localizing the app itself was actually fairly straightforward. It's a pretty small app and the main screen has almost no text on it. Localized App Store screenshots are always pretty involved, though, because the combinatorics always explode pretty quickly. Four screenshots each for three devices (iPhone X, iPhone 8, and Apple Watch) per 19 language/region variants (e.g. different Spanish screenshots for Spain and for Mexico) is ***228*** screenshots! I had to plug-and-chug for the better part of two days to make all of them, but I'm really happy with how they turned out. A lot of developers solve this problem by using an automated tool like [fastlane](https://docs.fastlane.tools/getting-started/ios/screenshots/#put-your-screenshots-into-device-frames), but I tend to believe it's impossible to beat the quality you get by doing them by-hand with design tools like [Sketch](https://www.sketch.com) and [Rotato](https://www.rotato.xyz). Only time will tell if the work pays off 🤞🏻

<div style="padding-top:20px; padding-bottom:20px;">
{% include photoswipe.html images=page.heros max-height=300 %}
</div>

{% include appstore.html link='https://apps.apple.com/app/inflation-calculator/id926713392' %}
