---
layout: post
title: 'Announcing Photo Map'
post-id: announcing-photo-map
thumbnail: thumbnail.png
photoswipe: true
tags: 
  - Apps

marketing:
  - src: marketing-2.png
    maxres: 1125 × 2436
  - src: marketing-4.png
    maxres: 1125 × 2436
  - src: marketing-5.png
    maxres: 1125 × 2436
    
states1:
  - src: states-map.jpg
    maxres: 2000 × 1031
    caption: "My example map from the original States app prototype, built at HackMerced 2017."
    
states2:
  - src: states-select.png
    maxres: 1200 × 554
    caption: "The original States app prototype included a very similar flow where you could tap on a state and then pick from the photos you took inside that state."

explorer-pack:
  - src: explorer-pack.png
    maxres: 750 × 1027
    caption: "The top portion of the Explorer Pack upsell screen in Photo Map"

people-filter:
  - src: people-filter-1.png
    maxres: 1002 × 1840
    caption: "Different options for filtering your photos in a region"
  - src: people-filter-2.png
    maxres: 1002 × 1840
    caption: "My photos of People in California (automatically detected using computer vision)"

large-export:
  - src: large-export.jpg
    maxres: 4500 × 4500
    caption: "A Map Export straigt out of Photo Map. The original export was 13,000 ×  13,000 pixels (this one is scaled down a bit for the web)."
    
huge-export:
  - src: bmp-header.jpeg
    maxres: 1566 × 852
    caption: "A snippit of sample code for write out the header block of a BMP image. This took forever to get right, even though the meat of it was lifted straight off of a Stack Overflow post."
  - src: huge-export.jpeg
    maxres: 1436 × 1146
    caption: "An example of a HUGE map I was able to export. 32,000 × 22,0000 is ridiculously large!"
    
ipad:
  - src: ipad.png
    maxres: 2318 × 1712
    caption: "Photo Map running on iPad"
    
hero:
  - src: thumbnail.png
    maxres: 1500 × 844
    
    
---

{% include youtube-square.html url='https://www.youtube.com/embed/g_UxefWrT3o' %}

**Photo Map** is now [available to download](https://apps.apple.com/us/app/photo-map-us-europe-more/id1472276407#?platform=iphone) on the App Store! It's a brand new app that uses your photos to tell the story of the places you've visited. Your trip photos are found automatically and combined together on the map to create a beautiful composite of all the places you've been.

<!--break-->

<h3>Features</h3>

<div style="padding-bottom:10px;">
{% include photoswipe.html images=page.marketing %}
</div>

 - Photo Map automatically scans your Photo Library to find photos from each of your trips.
 - Choose your favorite photo from each place you've visited.
 - Export a customizable image of your map. (Perfect for sharing on social media!)
 - Photo Map includes maps of the United States, World Countries, Europe, Canada, Australia, Asia, Africa, and South America. 
 - There's hundreds of places to visit, and you're just getting started. Find the inspiration you need to book your next adventure!

<h4 style="padding-top:15px;">Origins</h4>

I had the original idea for Photo Map back in February 2017. I was inspired by a [cool arts and crafts project](http://cutcraftcreate.blogspot.com/2014/02/personalized-photo-map-for-our-paper.html) I had seen where you cut out photos in the shape of the US State where they were taken, and then pin them up on a big wall map. I made the very first prototype of this idea at [HackMerced](http://hackmerced.io) 207, a hackathon deep in the heart of California's Central Valley. Back then the app was just called ["States"](https://devpost.com/software/states), because it only had a map for the US. That original prototype was way less polished, but the main idea was there.

{% include photoswipe.html images=page.states1 max-height=250 class='shadow' %}

{% include photoswipe.html images=page.states2 max-height=225 class='shadow' %}

On the [Devpost submission](https://devpost.com/software/states) at the end of the hackathon, I said that *"I think it's an idea that's actually worth publishing. I might get around to it one day."* I had a few months of downtime after graduating from Georgia Tech in May, and it had been on my idea list for over two years, so I decided to finally revisit the idea.

<h3>Making Photo Map</h3>
Photo Map is the first new app I've made since I released [AR Planes](/blog/announcing-ar-planes) in February 2018. There's still nothing more fun and rewarding than creating a whole product from scratch and actually getting it across the finish line. I had no shortage of hard problems and interesting challenges while working on Photo Map.

<h4>Choosing a Business Model</h4>
Most of my past app releases have been paid-up-front, but I wanted to try something different for Photo Map. I decided to launch Photo Map with a freemium business model. All users get the United States map for free. To unlock the other eight maps (including the World Map, Europe, Canada, etc.), users have to buy the **"Explorer Pack"** for $3. To make the value proposition a little better, I also bundled most of the Export Map customizations options into the Explorer Pack.

The problem with freemium apps is that you have to draw a line somewhere between the "free" features and "paid" features. If you give away too much for free, you harm your app's revenue potential. If you lock too much behind a paywall, the user experience will be bad and you could come across as greedy. 

{% include photoswipe.html images=page.explorer-pack class='shadow' max-height=340 %}

There are lots of potential places where the line could be drawn in Photo Map, but I felt like the "Explorer Pack" is a good first try. It's not perfect by any means &mdash; there's no reason to buy the Explorer Pack if you've from the US and have never traveled abroad, and the free offering isn't very useful if you're from elsewhere and have never been to the US &mdash; BUT I think it's a good starting point. I'm very interested to see how the launch goes!

<h4>Filtering with Computer Vision</h4>
It can sometimes be hard to find the *perfect* photo when digging through hundreds of photos taken in a given place. Early on, I added a filtering system so you can view photos from a specific year, or only see photos you've marked as "favorites" in the iOS Photos app. During the Beta process, somebody on Twitter suggested using Apple's [Vision framework](https://developer.apple.com/documentation/vision/) to only show photos of people. I thought this suggestion was too cool to not try, but it turned out to be *way* harder than I expected!

{% include photoswipe.html images=page.people-filter %}

The [face detection API](https://developer.apple.com/documentation/vision/vndetectfacerectanglesrequest) is reasonably easy to use, but it takes quite a while to run the algorithm on each of the hundreds of photos taken in any given place. The problem is that the user can change the active filters at any time, even while there's a vision scan currently going on in the background. That means the app has to cancel the current in-progress scan and start a new one, possibly where the previous one left off. This was the first time I've ever really worked with cancellable, long-running background tasks, and there were a lot of multithreadding challenges that took some time to work through. The end result is pretty cool, and reasonably performant! (Although I have a feeling it's gonna be my top source of weird and hard-to-reproduce crash reports 😅)

<h4>Photo Exporting</h4>

When I was working on the Photo Exporting feature, I wanted users to be able to export a copy of their map that was large enough that they could zoom in to even the smallest regions (like Washington DC on the US Map, or Luxembourg on the World Map) and still see high-resolution copies of their photos. DC and Luxembourg are pretty tiny, so the generated map image would have to be something like 30,0000 to 50,000 pixels wide. ***That's really, really big.*** Almost just unreasonably large. But I still wanted it to be an option! 

{% include photoswipe.html images=page.large-export class='shadow' %}

The problem with generating really, really large images is that iPhones simply don't have enough RAM to hold the entire photo in memory at once. A 50,000 ×  50,000 pixel image has ***2.5 billion pixels*** and its in-memory bitmap image buffer would be ***10 gigabytes*** large. Definitely not happening.

The workaround for this problem is to generate the image in multiple slices (where each slice on its own can fit within the RAM constraints), and then combine the slices into one file on-disk. Images have specific file formats, though, so it isn't as simple as just cramming multiple PNG files into the same file. 

The breakthrough I had was that, unlike PNG files, BMP files are completely uncompressed &mdash; they're literally just "bitmap" files, which is the same image representation used when you render an image in-memory. This makes them really inefficient for large images, BUT it means that it's possible to write a single BMP file in multiple slices. I set up a system that manually wrote out the BMP file header, rendered a slice of the image, blitz'd the pixels into the file, and then rendered more slices until the image was finished. It took a looong time to get right, but I got it to actually work!

{% include photoswipe.html images=page.huge-export class='shadow' %}

Unfortunately, as cool as it is, ***a 3 gigabyte image isn't really all that practical.*** I was hoping that Apple's high-performance [Image I/O framework](https://developer.apple.com/documentation/imageio) would be able to convert the image from a BMP to a PNG (which would bring the file size down into more manageable territory). Unfortunately, Image I/O [still tries to load the entire image into memory before doing the conversion](https://twitter.com/calstephens98/status/1161501756205031425?s=20). That's the same barrier that made me try this on-disk-BMP nonsense in the first place, so it put a nail in the coffin on this experiment. If you have any ideas for a workaround, please [get in touch](/contact/)! For now, a measly 13,000 × 13,000 pixel option will have to do. *(That's the largest image buffer an iPhone X can reliable work with. Photo Map uses smaller buffer sizes on older devices.)*

<h4>iPad.... and Mac??</h4>

{% include photoswipe.html images=page.ipad %}

Photo Map fully supports iPad, and looks awesome on the larger screen size. The bottom tray moves over to the left, leaving plenty of space for you to see your map. That's one feature that actually *wasn't* too difficult, because I just used a great library called [FloatingPanel](https://github.com/SCENEE/FloatingPanel). Good artists copy, great artists use existing open source implementations.

I'm also really interested in bringing Photo Map to the Mac this fall. [Mac Catalyst](https://developer.apple.com/ipad-apps-for-mac/) looks really promising, and should make it a fairly easy process. I have a fair number of third-party libraries I would also have to port over, but I think it would be worth the effort! Maybe keep an eye out for a beta release in September 😉

One problem is that, the more platforms an app supports, the more likely people are to expect it to sync their data across all of their devices. Right now, Photo Map doesn't offer any cloud syncing functionality. I feel like, for the Mac app experience to make sense, it would have to sync with the iPhone app. I *conveniently* have an unused iCloud Drive-based photo syncing system (that I built for [Window](/blog/announcing-window-3) but [never shipped](/blog/window-acquired)) lying around. So I'm thinking about it!

<h4>Launch 🚀</h4>
I've been working on Photo Map since April, and it's been in beta since July. I'm super pumped to see how the launch goes! Only time will tell, but I'm optimistic. Download it and [let me know what you think](https://twitter.com/calstephens98)!!

<h3>Downloading Photo Map</h3>

Photo Map is now available to download on the [**App Store**](https://apps.apple.com/us/app/photo-map-us-europe-more/id1472276407#?platform=iphone) for iPhone and iPad!

{% include photoswipe.html images=page.hero max-height=500 %}

{% include appstore.html link='https://apps.apple.com/us/app/photo-map-us-europe-more/id1472276407#?platform=iphone' %}