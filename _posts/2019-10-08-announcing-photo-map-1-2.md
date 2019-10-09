---
layout: post
title: 'Announcing Photo Map 1.2: Over 80 new maps, and more!'
post-id: announcing-photo-map-1-2
thumbnail: thumbnail.png
photoswipe: true
tags: 
  - Apps

header:
  - src: maps.png
    maxres: 776 × 1524
    caption: "The new layout for Photo Map's Map List"
  - src: countries.png
    maxres: 776 × 1524
    caption: "Some of the new countries maps available in Photo Map 1.2"
  - src: states.png
    maxres: 776 × 1524
    caption: "Maps for all 50 of the US States are now available in Photo Map 1.2!"

countries:
  - src: all-countries.png
    maxres: 1366 × 977
    caption: "All of the countries available in Photo Map 1.2"
    
states:
  - src: all-states.png
    maxres: 1366 × 977
    caption: "Maps for all 50 of the US States are now available in Photo Map 1.2!"
    
search:
  - src: maps.png
    maxres: 776 × 1524
    caption: "The new layout for Photo Map's Map List"
  - src: custom-sorting.png
    maxres: 776 × 1524
    caption: "The Map List is now highly customizable"
  - src: search.png
    maxres: 776 × 1524
    caption: "Photo Map's new Search Flow"
    
explorer-pack:
  - src: china.png
    maxres: 776 × 1524
    caption: "Users in China now get the Asia map for free"
  - src: brazil.png
    maxres: 776 × 1524
    caption: "Users in Brail now get the South America map for free"
    
ios13:
  - src: dark-us.png
    maxres: 776 × 1524
    caption: "The United States map in Dark Mode"
  - src: dark-context-menu.png
    maxres: 776 × 1524
    caption: "A context menu on top of the Europe map"
  - src: dark-about.png
    maxres: 776 × 1524
    caption: "The About screen, using iOS 13's design language"
    
hero:
  - src: thumbnail.png
    maxres: 1500 × 844
    
    
---

**Photo Map 1.2** is now [available to download](https://apps.apple.com/us/app/photo-map-us-europe-more/id1472276407#?platform=iphone) on the App Store! This is a packed update that includes over 80 new maps, great new features, and a rethought business model based on feedback from the [launch](/blog/announcing-photo-map) back in August.

<div style="padding-top:20px; padding-bottom:20px;">
{% include photoswipe.html images=page.header max-height=400 %}
</div>

<!--break-->

<h3>Maps for 31 new countries</h3>

{% include photoswipe.html images=page.countries max-height=450 %}

When I [launched Photo Map](/blog/announcing-photo-map), it only included maps for three countires: the United States, Canada, and Australia. I picked them because they're fairly large countires with large sub-regions. After all, US States are about the size of [whole European countries](https://twentytwowords.com/map-of-u-s-states-transposed-onto-similar-european-countries-to-give-a-sense-of-size/). Photo Map really struck a chord with a lot of users from around the world, though, who wanted to be able to use it with their own home country. 

I was linked to a [GitHub repo](https://github.com/deldersveld/topojson) with TopoJSON files for the sub-regions of <i>dozens</i> of World Countries. I just had to slice and dice the data with [Mapshaper](https://mapshaper.org) to turn it into the GeoJSON format that Photo Map uses. Thanks to these great tools, Photo Map now has maps for <i><b>34 countries</b></i> from around the world. This includes highlights like China, Brazil, India, Mexico, France, and Germany, but there are plenty of others for you to enjoy as well.

<h3>Maps for the 50 US States</h3>

{% include photoswipe.html images=page.states max-height=450 %}

I was soliciting country requests on Twitter, and my friend [Logan](https://twitter.com/loganjmcelroy) cheekily requested support for the Counties of Georgia. The [TopoJSON repo](https://github.com/deldersveld/topojson) I was using happened to also have [counties data](https://github.com/deldersveld/topojson/tree/master/countries/us-states) for all 50 of the US States, so I couldn't resist. All content is good content! *(The hardest part with this was actually trying to choose a unique emoji for each of the 50 states. It wasn't easy!)*

<blockquote class="twitter-tweet tw-align-center"><p lang="en" dir="ltr">You should add county maps for people who DONT travel that much. Let me see my photos in Richmond county, Clarke county, Dekalb county, you know, the good stuff</p>&mdash; L🕸G🕷N M🦇E🔪R💀Y (@loganjmcelroy) <a href="https://twitter.com/loganjmcelroy/status/1176937787829800960?ref_src=twsrc%5Etfw">September 25, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
<br>

<h3>Redesigned Map List with Search</h3>

<div style="padding-top:20px; padding-bottom:20px;">
{% include photoswipe.html images=page.search max-height=400 %}
</div>

Photo Map 1.0 only included 8 maps, so the Map List could afford to be fairly simple. Photo Map 1.2 now includes ***over 90 maps***, so the old layout wasn't cutting it anymore. I reworked the Map List to use a two-column layout and group the maps into categories (currently *"Continents"*, *"Countries"*, and *"US States"*). You can set Favorite maps that always appear at the top, and you can pick between several different options for sorting the growing list of maps. If you want to pull up a specific map, you can also now search for it by name.

<h3>Updates to the Explorer Pack</h3>

In Photo Map 1.0, all users got the United States map for free. This was definitely not the greatest strategy for non-US users, who were basically unable to use Photo Map at all if they hadn't been to the US before. I've re-worked it a bit in Photo Map 1.2, and now users get a free map that's more tailored to their home country.

<div style="padding-top:20px; padding-bottom:20px;">
{% include photoswipe.html images=page.explorer-pack max-height=400 %}
</div>

Users from the US will continue to get the United States map for free, but users from other countries will now get their *home continent* for free. Photo Map also highlights some specific Explorer Pack maps that the user may find interesting, such as the map for their home country, their most-visited continent, etc. I'm hoping that these new changes will help make the app feel less US-centric (a common complaint on the App Store reviews) while also helping to increase conversion for the Explorer Pack.

<h3>Great iOS 13 Support</h3>

<div style="padding-top:20px; padding-bottom:20px;">
{% include photoswipe.html images=page.ios13 max-height=400 %}
</div>

Photo Map also now has great support for the new features introduced in iOS 13. Photo Map 1.1 added support for Dark Mode and Context Menus throughout the app, and takes advantage of the system's new design language. 

<h3>Downloading Photo Map</h3>

Photo Map is available to download on the [**App Store**](https://apps.apple.com/us/app/photo-map-us-europe-more/id1472276407#?platform=iphone) for iPhone and iPad!

{% include youtube-square.html url='https://www.youtube.com/embed/g_UxefWrT3o' %}