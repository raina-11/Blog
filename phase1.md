## Phase 1

I have gone through the previous year's code and tested it on some videos. I have seen the videos manually and found some of the anchors are accurately identified and some of them are misinterpreted. So there is some problem in clustering itself, so as discussed with the mentor we decided to explore multiple options in order to segment the videos. So In the beginning I’m trying some shot boundary methods.

### I have tried 2 methods for the Shot Boundary Detection:

**Method 1:** Simple algorithm based on the frame difference

This calculates the difference between frames, because the larger the difference is, the more possible the frame is to be the boundary shot of a video.
 
* Calculate all the differences between the frames
* Detect the possible frame
* Optimise the possible frame

**Method 2:** Based on ECR technique

* This method consists in changing the edges of objects in the frames across a border.
* The entering edge pixel is the edge pixel that is present in current frame E and is farther away than r in next frame E’. 
* The existing edge pixel is the edge pixel that is present in the next frame E’ and is farther away than r in current frame E.
* An entering edge pixel is a pixel which is determined to be an edge pixel in frame n, but which neither was an edge pixel in frame Fn−1 nor had an edge pixel in its vicinity in frame Fn−1. 
* Conversely, an exciting edge pixel is a pixel which was determined to be an edge pixel in frame Fn−1 but which neither is nor has an edge pixel in its vicinity in frame Fn.


