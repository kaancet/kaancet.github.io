---
layout: single
title: "A study of perceived motion, Part I"
categories: posts
tags: [motion, visualization, processing, pills, waves]
excerpt: ""
date: 2023-03-22
---


Motion is change. More specifically, change in __position__ with respect to __time__, but the perception of motion doesn't necessarily has to be due to actual change in an objects physical position. Optical illusions are the best examples of this, where a static image looks like there is some sort of movement.

<center>
    <img src="/assets/images/perceived_motion/optical_illusion.jpg" alt="optical illusion" width="500" height="500"/>
</center>

If you look closely you can see the rings around the pink circles have black and white portions and they rotate in each row and column. The rotation is the same for both the rows and the columns so each diagonal has the same rotation amount for the ring. Additionally there is a slight color difference in blocks of circles in the same diagonal axis. Together, these individual and local differences create the perception of a digaonal wave motion perpendicular to the diagonal axis of ring orientations and color differences.

Very cool, very sexy. This is due to your brain spazzing out because it tries to bridge the differences by predicting the missing information, which on this case does not exist. This how our brain operates when processing [sensory information](https://neurosciencenews.com/prediction-brain-21183/).

"Well, why is that information missing?" you might ask. Because that mushy fat tissue inside our cranium can't keep up with our ADHD riddled gaze jumping all over the visual space, so it processes some of the information and tries to fill in the blanks while you're not looking, pun intended. This way it conserves energy and also rapidly serves you information that is crucial for your survival, like the tiger camouflaged among the tall grass or the month in expiry date on your 6-month-old almond milk that you bought in an attempt to live a "healthier" life but forgot about it the next day.

Another way we perceive motion - that doesn't exploit our brains attempt to be efficient - occurs when we observe multiple individual object behaving in a semi-organized way, like a swarm. The best examples for this are the shapes and patterns that are created by migrating swallows.

<center>
    <video width="400" controls>
    <source src="/assets/images/perceived_motion/migration.mp4" type="video/mp4">
    Your browser does not support HTML video.
    </video>
</center>

Obviously there is motion here; individual birds are flying, which then creates these "blobs" of dark regions with higher bird concentrations that move around. But the movement of the flock is not organized or coreographed, it occurs as a result of each bird flying under a set of constraints, such as proximity to its neighbours, direction of flight of its neighbours and so on. These kind of [swarm behaviors](https://en.wikipedia.org/wiki/Swarm_behaviour) are already well studied.

For now I will only focus on the visual aspect of it, where simple motion of individuals give rise to a global perceived motion, without any local constraints on motion of indivduals but rather having a constant frequency difference between individuals, which is determined by $BLABLA$ in the equation below. For this purpose, I will create a grid of individual objects and try objects to generate a global motion. The oscillations are determined by the coordinates of the pill in the grid and we can increase the weight of each coordinate.

Below is a grid of our sexy little _pills_(_Why pills? Because I recently watched Dopesick and my subconcious is apparently very impressionable, that's why._), rotating in their own frequencies:

<figure class="half">
  <table style="border: 0px">
    <tr>
      <td style="border: 0px">
        <img src="/assets/images/perceived_motion/frames_rot.gif" alt="rotate_grid" width="450" height="450"/>
      </td>
    </tr>
  </table>
</figure>

Simply beautiful. If we just focus on individual pills on the element, we can see all they do is rotate in their own speed, which is dependent on their coordinates. This creates a neighbouring relationship between neighbouring pills, but that is kind of what we want because that's how swarm behavior emerges too.

You can see the wave traveling from the top left to the bottom right. The "wavelength" of this wave also changes as the pattern keeps evolvong. In addition, an alternative diagonal grid pattern occurs once in a while.

We can try changing other properties such as the size and color of the pills in the grid:

<figure class="half">
  <table style="border: 0px">
    <tr>
      <td style="border: 0px">
        <img src="/assets/images/perceived_motion/frames_size.gif" alt="rotate_grid" width="300" height="300"/>
      </td>
      <td style="border: 0px">
        <img src="/assets/images/perceived_motion/frames_color.gif" alt="rotate_grid" width="300" height="300"/>
      </td>
    </tr>
  </table>
</figure>

For the size oscillation the waves are much more clearer, which then morphs into an array of upward _moving_ "impulses" in each column. The color oscillation on the other hand only makes it so we see a global upward moving wave on the grid.

Well, why stop there we can do all of the above in 3D, and add some camera movement to have some sick "drone-shots" of our 3D grid:

<figure class="half">
  <table style="border: 0px">
    <tr>
      <td style="border: 0px">
        <img src="/assets/images/perceived_motion/frames_3d_size.gif" alt="rotate_grid" width="300" height="300"/>
      </td>
      <td style="border: 0px">
        <img src="/assets/images/perceived_motion/frames_3d_color.gif" alt="rotate_grid" width="300" height="300"/>
      </td>
    </tr>
  </table>
</figure>

The movement of the camera makes it quite hard to perceive a global motion from the individual oscillations because even if we fixate on one location, as our vantage point changes the visual information that needs to be predicted also changes, making it very unlikely to have coherent global motion perception. That being said, the 3D color grid look pretty fucking cool.

I planned this to be a two part series, where in the second part I will simulate some swarm behavior on processing. Hopefully it wouldn't be another 5 years...
