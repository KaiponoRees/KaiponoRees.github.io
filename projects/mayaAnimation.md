---
layout: project
type: project
image: img/mayaanimation2.png
title: "ICS-369 Final Maya Animation Project"
date: 2026-05-05
published: true
labels:
  - Python
  - Maya
summary: "My final ICS-369 project with Maya using an animated cauldron with fire, smoke, bubbles, changing liquid colors, and an explosive finale."
---
<video width="1000" controls>
  <source src="../videos/mayaAnimation.mp4" type="video/mp4">
  Your browser does not support the video.
</video>

## Project Overview

At first, I was unsure how to bring my laboratory concept to life in Maya. I imagined a dramatic scene with bubbling potions, fire, and smoke, but turning that vision into reality proved more complex than I expected. As I progressed, I began connecting the different steps needed to create the scene, especially when building the particle systems for the fire, smoke, bubbling liquid, and spiral effects.

For this assignment, I created a 240-frame Maya animation centered around a magical cauldron. 
I used Python to build custom particle systems, emitters, forces, collision effects, lighting, shaders, and keyframes. 
These tools controlled how the particles moved, changed color, grew, and faded throughout the animation. 
I also imported multiple Maya scene files to create the cauldron and laboratory environment.The final animation featured fire and smoke rising around the cauldron, bubbles forming inside the liquid, and a colorful magical spiral appearing above it. 

Each effect used randomized movement, size, color, and opacity to make the scene look more natural and dynamic. 
Near the end of the animation, the cauldron created a large particle explosion as the final effect. Understanding how these effects interacted through forces, emitters, and collisions became one of the main focuses of the project. I also had to make sure that all of the effects worked well with the objects I modeled and brought into the scene.

## Creating the Laboratory

My main focus for the project was creating a laboratory scene with multiple particle effects interacting with each other. I created a fire emitter using a sphere collider, rising smoke, and a separate bubble emitter for the bubbling liquid. I adjusted gravity and velocity to make the particles appear more realistic and used changes in color, size, and opacity to improve the effects over time.

Once the main code portion of the scene was complete, I started to design multiple unique potions with different shapes and colors and added crates to help fill the environment. Each of these elements helped bring the scene together and create the laboratory environment I wanted.

## Challenges I Faced

The biggest challenge for me was getting the particles to behave the way I wanted. Creating the particles themselves was not too difficult, but controlling their movement was. For example, making the fire wrap around the cauldron instead of simply traveling straight upward took a lot of trial and error with colliders, forces, and velocity settings.

Another challenge was making everything work together. Each emitter, force, and function affected other parts of the scene, so changing one thing could sometimes cause another effect to stop working correctly. When I began adding my objects and animations, I also had to make sure the timing of the camera movements and particle emitters worked together.

Importing the objects I created was also more difficult than I expected. Some objects did not look the same once they were brought into the final scene, so I had to go back and adjust their scaling, positioning, and sometimes their materials. Lighting created another challenge because certain objects looked completely different depending on how the light interacted with them.

Lastly, rendering was one of the biggest challenges of the entire project. The render times were extremely long, sometimes taking days, and I experienced multiple crashes throughout the process. Every time something failed, I had to restart parts of the rendering process, which made it even more time-consuming. Finding a balance between maintaining good visual quality, managing render times, and completing the project before the deadline was challenging.

## What I Would Do Differently

If I were to do this project again, I would try to stick more closely to the plan I created in the beginning. Changing different parts of the project as I went and fixing problems along the way took much more time than I expected. I would also organize my code better from the beginning so that making changes later would be easier.

Another thing I would do differently is spend more time understanding and testing the animation earlier instead of waiting until the end. I would test smaller parts of the scene individually before combining everything. This would make it easier to identify problems early rather than trying to figure out what went wrong after everything was already connected.

I would also begin testing my rendering settings much earlier. Waiting until the end to fully render the project caused problems because of the long render times and crashes.

## If I Had More Time

If I had more time, I would add more realism and detail to the scene. I would experiment with more advanced forces, such as vortex and turbulence, to make the particle movement appear more natural. I would also improve the interaction between the flames and smoke to make the scene feel more dynamic.

Overall, I would focus on refining the animations and particle effects to make everything appear smoother and more realistic. Even with the challenges I experienced throughout the process, I am extremely happy with how the final project turned out.
