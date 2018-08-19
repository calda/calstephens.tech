---
layout: post
title: "Recap: Hack the North 2017"
post-id: recap-hack-the-north-2017
thumbnail: photo-booth.jpeg
photoswipe: true
tags: 
  - Hackathons

ar-planes:
  - src: ar-planes.png
    maxres: 1500x750

friendship:
  - src: photo-booth.jpeg
    maxres: 1844x1240
  - src: demo-2.jpeg
    maxres: 1296x864
  - src: medals.jpeg
    maxres: 1000x667
---

Last weekend I was in Waterloo, Ontario for Hack the North 2017, the largest hackathon in Canada. [Justin Trudeau]() showed up, so you know it's a big deal! I love traveling to hackathons, meeting new people, and working on cool projects, so it was a fantastic weekend!

<h4>The Project</h4>

{% include photoswipe.html images=page.ar-planes %}

<!--break-->

We built an app called [AR Planes](https://www.youtube.com/dnYHQ-7wlag) that lets you visualize and discover the planes flying around you. It uses ARKit to show all of the planes nearby in augmented reality. You can tap on a plane to find out additional information, like the airline, origin airport, and final destination.

None of my team had experience with augmented reality before, so it was a big learning experience for us. We had to build out a system that ingests [all of the planes in the sky](https://opensky-network.org/api/states/all) every second, finds the nearby planes, and then maps the longitude/latitude/altitude information to actual points within the augmented reality scene.

That gave us the 3D planes in the sky, but getting human-readable metadata about the flight itself (airline, destination airport, etc.) was a different story. There doesn't seem to be freely available API that suits these purposes, so we resorted to scraping [flightaware.com](https://flightaware.com) for the information we needed. Once we had that, we could render the information as a card overlay in the scene.

Once it all came together at the end of the hackathon, it worked great! We placed Top 14 (out of 220 teams!) and got to [present our hack](https://youtu.be/txA5FvB-1as?t=2191) at the closing ceremonies.

<h4>The Team</h4>

{% include photoswipe.html images=page.friendship %}

AR Planes wouldn't have been possible without such a great team! I worked with my friend [Mantas](https://mantasmatelis.com/), who I met while I was working at Airbnb this summer, and our new friend [Olivia](https://github.com/oliviabrown9), who we met on the first night of the hackathon. It's always a treat to work with such skilled people and be able to trust that they'll deliver some great work.

Next up is HackGT in October!




