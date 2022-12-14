---
layout: project
type: project
image: img/manoa-market/white-logo.png
title: "Manoa Market"
date: 2022
published: true
labels:
  - Marketplace
  - React
  - Meteor
summary: "My team developed a web app marketplace where University of Hawaii - Manoa students can buy/sell/trade their items."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

Micromouse is an event where small robot “mice” solve a 16 x 16 maze.  Events are held worldwide.  The maze is made up of a 16 by 16 gird of cells, each 180 mm square with walls 50 mm high.  The mice are completely autonomous robots that must find their way from a predetermined starting position to the central area of the maze unaided.  The mouse will need to keep track of where it is, discover walls as it explores, map out the maze and detect when it has reached the center.  having reached the center, the mouse will typically perform additional searches of the maze until it has found the most optimal route from the start to the center.  Once the most optimal route has been determined, the mouse will run that route in the shortest possible time.

For this project, we were a team of two, so most responsibilities were split between us.  It being an introductory project course, and with the knowledge and resources we had on hand, we developed a top-down sensor mouse.  I soldered together the mouse, integrating the wheels and sensors with the board we used.  We re-calibrated how much to each wheel we would pulse, to make it go forward, or backwards.  The turns in the maze are where we had to troubleshoot the most.  As we were beginners our then implementation was trial and error, until we got the right amount to pulse the wheels to make a perfect turn for the dimensions of our mouse.  We didn't have an algorithm set but if we were to do it again we would change the sensor type to front facing sensors and implment a floodfill algorithm for the mouse.


You can learn more at the [UH Micromouse News Announcement](https://manoa.hawaii.edu/news/article.php?aId=2857).
