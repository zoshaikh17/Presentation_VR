# Presentation_VR

## Overview
Low vision can affect anyone at any age and it includes different degrees of sight loss from having blind spots, poor night vision, and problems with glare to almost a complete 
loss of sight, and cannot normally be treated. Peripheral vision loss is one of the main visual field’s problems where patients can see through their central area only in a way
that makes their daily life activities such as driving and crossing the road very hard. 

This is how a person with peripheral vision loss can see.

![example](https://user-images.githubusercontent.com/55362861/92481480-07750580-f1ac-11ea-9dfa-f3a86e25a516.PNG)

Virtual reality (VR) and augmented reality (AR) are both technologies that have been used to provide computer-generated information for users. In virtual reality, user usually 
wears googles to see complete artificial scene and interact with its elements without the ability to distinguish between real and artificial ones. In augmented reality, user is 
still seeing real scene with some artificial elements augmented to it.

## How it works?
There were two solutions for assisting tunnel vision persons presented in the paper. The first one applies the augmented reality concepts and technologies to superimpose patient’s
defected vision by computer generated information to alert him for any movements in his peripheral area (where he can’t see). 
The second solution is to bring what the patient is missing and display it in his healthy area to see a complete virtual image. In both solutions, we are using real-time video
processing to analyses the video stream captured by an embedded camera inside the glasses frame.

### Solution 1
It consists of two main parts, eyeglasses and wristband. Glasses consist of a camera unit to detect the surrounding environment and send a real-time video to Microcontroller unit
to perform some pre-processing for the video stream, and transparent OLED for display purposes. Video streams then to pass to the main processing unit which is Nvidia Jetson TK1
board that is responsible for image processing tasks such as face detection and object tracking.  The final output is sent to the transparent organic light emitting diode (TOLED)
display unit.


### Solution 2
The second proposed solution is a complete virtual reality model that prevent the patient from seeing real scenes and replace the actual picture with computer generated one. The
idea is to use the healthy area and try to present the complete image (central +peripheral) in it. Two cameras are capturing a complete image to be viewed by patient’s eyes. The 
paper suggest using fisheye lenses to capture wider view and then correcting the images to a straight one (Rectilinear conversion). The figure below shows a comparison between
regular and fisheye lenses.

![Solution2a](https://user-images.githubusercontent.com/55362861/92490487-b61e4380-f1b6-11ea-926f-b28b1b023bd9.PNG)
![Solution2b](https://user-images.githubusercontent.com/55362861/92490488-b6b6da00-f1b6-11ea-8893-67f7a8ae22ef.PNG)

The final step is to minimize the corrected image and present it the patient’s healthy area (central vision), which gives the patient the ability to see the full picture of the 
surrounding area.

The below picture show the corrected image that is presented,

![corrected image](https://user-images.githubusercontent.com/55362861/92502912-1ec0ec80-f1c6-11ea-8d16-b5233e475775.PNG)








