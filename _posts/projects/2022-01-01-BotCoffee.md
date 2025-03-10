---
layout: project
permalink: /:title/
category: projects

meta:
  keywords: "Jekyll, Pineapple"

project:
  title: "BotChoco"
  type: "Jekyll"
  url: "https://github.com/shantao/BotChoco"
  logo: "/assets/images/projects/redpineapple/logo.png"
  tech: "HTML, CSS, Boostrap, Sass, JavaScript, jQuery, Jekyll"

images:
  - image:
    url: "/assets/images/projects/redpineapple/devices.jpg"
    alt: "Red Pineapple website on tablet, mobile and desktop"
  - image:
    url: "/assets/images/projects/redpineapple/desktop.jpg"
    alt: "Red Pineapple website on a desktop device"
  - image:
    url: "/assets/images/projects/redpineapple/mobile.jpg"
    alt: "Red Pineapple website on a mobile device"
---

X6 speed 

## Technologies
Ros, Python, OpenCV, Manipulation

## Project
<p>In this project, a Franka Emika Panda robot arm was programmed to autonomously make a cup of hot chocolate.</p>


<p>Given a kettle, a cup, a stirrer and a scoop with chocolate powder, the robot is able to turn on the kettle, pour the chocolate powder into the cup, pour the hot water into the cup, and stir to make the hot chocolate fully dissolved.</p>

<p>In this project, my major role was to implement computer vision pipeline with other teammates that accurately detects the location of each object in the work space, design and fabricate physical supports for robot to interact with objetcs, create a obstacle generation function to allow robot avoid collision with other objects in the work space.</p>

<p>In the conputer vision pipeline, a RGB video stream is provided by an Intel Realsense D435i camera. The video allows the objects to be located in the work space by the related AprilTags. The camera frame is linked with robot base frame. The relationship is provided by calibration through an AprilTag temporary attached to the end effector. This allows the camera frame and detected object frame linked with robot frames. Two AprilTags are used to represent the objects' location. One tag is for the kettle and another one is for the jig which is used to set cup, scoop, and stirrer. Because of the jig, the frames for cup, scoop, and stirrer can be converted from a single AprilTag without  In this case, all the objects are linked with robot frame through the the conputer vision pipeline which can be easily accessed by robot control package.</p>

<p>Before making coffee, if the camera is moved, a calibration is required to rebuild the transformation frame between camera and robot. When the program is started, the computer vision pipeline provides the object frame infomation to robot and update the infomation if the object is not located at the original location. </p>

<p>The obstacle adding function can provide possible collision space for the robot. This allow the robot to positively avoid collision with objects in the working space during path planning.</p>

<p>The final results show the program is able to successfully make hot chocolate with high rates of success. Future work may involve adding machine learning object detection and kettle status detection.</p>
