# Welcome to gsted

gsted is a MATLAB function for object overlay.

![](https://github.com/gsted/gsted/blob/master/gsted.png)

[ZIP Archive](gsted.zip)

## The Motivation

We set out with the sole intention of creating a really good object overlay toolkit. 

It would use object properties along with predefined conditions (forward-facing subjects, a reasonable amount of resolution, etc.) to accurately place objects in a scene. We say scene because the original goal of the project was to produce a system that could work on a per-frame basis. Being so, it would reproduce the effect seen in platforms like Snapchat or those employed in some animation.

So, to address our initially proposed idea - it can still be seen in our work. This project was always going to be inspired by things like Photo Booth, but an opportunity presented itself in the form of tracking.js

The [tracking.js](https://trackingjs.com/tracking.js) library offers face detection that, if licensed, could have worked with our algorithms to enable execution at a given frame - that is, if we were able to build our code using JavaScript. 

That’s a venture for another day.

## Our Aproach

We had to approach solving some of the following challenges:

1. Mapping objects to a specific location in a master image
2. Scaling and orienting our objects based on their relative position: foreground, background, angle, etc.
3. A consequential challenge post-rotation of relocating the object centroid.

Creating the algorithm followed a fairly straightforward development cycle. We’ll share that breakdown in the next section.

## Implementation

1. Detection of unique rectangles in master image: a. Detect by searching for specific color value. 
2. Extraction of properties from these rectangles: a. Extraction of angle from horizontal. b. Extraction of length of the long axis of rectangle.
3. Transforming overlay images based on these properties: a. Tilting overlay image based on angle property. b. Resizing overlay image based on length of long axis.
4. Obtain burn point as position to burn overlay image onto master image: a. Extract burn point from master as center of extracted unique rectangle. b. Extract burn point from overlay image as colored dot place on this image.
5. Burn the overlay image onto the master image at this burn point
6. Repeat frame by frame in a video.


### Hats Pack 1

![](https://github.com/gsted/gsted/blob/master/Hats/hats.png)


## Challenges & Results

Text text text text text text text text.



