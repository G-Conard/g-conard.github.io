---
title: MicroDog - A Low-Cost Quadruped Robot
summary: To the need for inexpensive quadruped platforms that could be used by both researchers and robotics students, I developed a roughly $150 quadruped robot over the course of my honors thesis.
tags:
  - Lafayette
date: '2016-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart

# links:
#   - icon: twitter
#     icon_pack: fab
#     name: Follow
#     url: https://twitter.com/georgecushen
# url_code: ''
# url_pdf: ''
# url_slides: ''
# url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---

Starting as an independent study in the spring of my junior year (2020), this project morphed into my senior thesis titled "Stepping Up: Investigating Dynamic Stability in a Low-Cost Quadruped Robot." After noting a lack of inexpensive quadruped platforms that could be used by both researchers and robotics students, Professor Brown and I developed several iterations of a roughly $150 quadruped robot to meet this need. Standing at about 6 inches tall, this platform consists of twelve RC servos, a 7.4V battery pack for untethered walking, and several 3D-printed components. In addition, I designed the custom printed circuit board that serves as the robot's chassis, which features an integrated ATmega32u4, a Raspberry Pi Zero, a few IR sensors, an IMU, and a number of power and communication breakout pins and mounting holes to make this an expandable platform. 

On the software side, I focused primarily on developing a simplistic walking gait and implementing active compliance in the legs of MicroDog during my independent study. To do this, we designed compressible feet, each fitted with a Hall effect sensor to measure the amount that the foot was compressed. The "spring constant" of the foot was experimentally derived, allowing us to determine the force being applied to the bottom of the foot. 

<img src="images/Force-Sensing-Leg-PCB-Labeled.png" height=250 class="center">

Using springs again as a model for joint compliance, we could tune how much the foot position compensated in response to an applied force. 

[![Demonstrating Active Compliance on MicroDog](https://res.cloudinary.com/marcomontalbano/image/upload/v1613171639/video_to_markdown/images/youtube--vsHqT6bXOFw-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/vsHqT6bXOFw "Demonstrating Active Compliance on MicroDog")

For more details about my independent study, see my <a href="documents/Conard-Independent-Study-Paper.pdf" target="_blank">final report</a>.

This work set the foundation for my thesis project. My original goals are presented in my thesis proposal <a href="documents/Conard-Thesis-Proposal.pdf" target="_blank">paper</a> and <a href="documents/Conard-Thesis-Proposal-Presentation.pdf" target="_blank">presentation.</a>. During the Fall 2020 semester, I developed improved walking gaits, such as the example in the video below, and experimented with obstacle avoidance using IR sensors by having the robot avoid the edge of a table.  

[![MicroDog Walking](https://res.cloudinary.com/marcomontalbano/image/upload/v1613171808/video_to_markdown/images/youtube--5-5qfn_KVnA-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/5-5qfn_KVnA "MicroDog Walking")

After designing and constructing a fourth iteration of the robot to address some electrical issues, I spent the rest of the spring semester investigating methods of implementing disturbance recovery from a side load using the force sensors in the feet. 

[![MicroDog Disturbance Recovery](https://res.cloudinary.com/marcomontalbano/image/upload/v1633960871/video_to_markdown/images/youtube--MJ5eYOLgRrY-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/MJ5eYOLgRrY "MicroDog Disturbance Recovery")

This work has received some press coverage as well, first by IEEE in a fun article describing [how roboticists have been working from home](https://spectrum.ieee.org/automaton/robotics/home-robots/how-roboticists-and-robots-have-been-working-from-home) and again by [Lafayette News](https://news.lafayette.edu/2020/09/21/homegrown-robots/).

This work culminated in a final <a href="documents/GC_Thesis_FullDocument.pdf" target="_blank">thesis report</a> and defense presentation. While I have passed my thesis defense and the project is "finished", there is so much more that can be done with this platform. I hope to publish a paper in the near future about the work I have done on it thus far, and hopefully, future students at Lafayette can continue exploring what this robot can do, like stair climbing or uneven terrain navigation.
