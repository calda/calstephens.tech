---
layout: page
title: "Photo Map Frequently Asked Questions"
permalink: /photo-map-faq.html
hide: false
---

## Photo Map Frequently Asked Questions

{% include section.html name="Table of Contents" %}
 - {% include link.html name="Does Photo Map upload my photos to the internet?" %}
 - {% include link.html name="Why can't Photo Map find photos from my trip?" %}
 - {% include link.html name="Why doesn't Photo Map include a map for my country?" %}
 - {% include link.html name="Can I import my photos from Google Photos?" %}

{% include section.html name="Does Photo Map upload my photos to the internet?" %}
No! When Photo Map imports your photos, they're stored privately inside the Photo Map app, and never shared or uploaded to the internet. You can learn more by reviewing Photo Map's [Privacy Policy](https://calstephens.tech/photo-map-privacy-policy).

{% include section.html name="Why can't Photo Map find photos from my trip?" %}
Photo Map uses the Location Data associated with the photos in your Photo Library.
 - Do your existing photos include Location Data? [How to see places where your iPhone photos were taken](https://www.idownloadblog.com/2015/02/11/how-to-see-places-where-your-iphone-photos-were-taken/)
 - If not, enable Location Services for the Camera app. [Cult of Mac Guide](https://www.cultofmac.com/266849/see-took-photos-iphone-ios-tips/)
 - Photo Map's region boundaries are approximate, so photos taken near international or regional borders may not be matched correctly.
 
If Photo Map is unable to automatically find your photos, you can manually select any photo from your Photo Library. Tap on the region, tap on the **More Options (...)** button at the top-right corner of the sliding panel, and then tap **Choose Photo from Library**.

{% include section.html name="Why doesn't Photo Map include a map for my country?" %}
Photo Map uses high-resolution [GeoJSON shapefiles](https://geojson.org) to store how different regions are shaped, and to filter photo coordinates by region. It's pretty easy to add new maps once I have high-resolution shapefiles. If you have shapefiles for your country and would like to see them added to Photo Map, [get in touch](/contact/)!

{% include section.html name="Can I import my photos from Google Photos?" %}
I've gotten a lot of requests to add support for Google Photos, but unfortunately developers are [not allowed](https://stackoverflow.com/a/52775596) to access Photo location data through the Google Photos API.