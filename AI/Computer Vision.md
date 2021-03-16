## Optical flow

Pattern of apparent motion of image objects between two consecutive frames caused by the movement of object of camera. 
### Assumptions

* The pixel intensities of an object do not change between consecutive frames
* Neighbouring pixels have similar motion

## Edge detection 

### Canny Edge detection process 

* Apply a gaussian filter to smooth the image in order to remove the noise. 
* Apply non-maximum supression to get rif of spurious response to edge detection. 
* Track edge by histeresis (supressing all the other edges that are weak and not connected to strong edges)

## Corner detection 

A corner is a point whose local neighborhood stands in two dominant and different edge directions. 


## Histogram

A histogram is a visual representation of the distribution of a continuous feature. 


## Gradients

an image gradient is a directional change in the intensity or color in an image. 

## Morphological operators 

Set of kernels that can achieve a variety of effects, such as reducing noise. 
The effect is most easily seen on text data on images. 


## Blurring and smoothing 

A common operation for image processing is blurring or smoothing an image. 
Smoothing an image can help get rid of noise, or help an application focus on general details. 
It is often combined with edge detection. 
Edge detection algorithms detect too many edges when given a high resolution image without smoothing and blurring. 

## Thresholding 

Some applications only requires a binary image showing general shapes. 
Thresholding is fundamentally a very simple method of segmenting an image into different parts.
Thresholding will convert an image to consist of only two values, white of black. 

## Blending images

With opencv, it is done through the addWeighted function that uses both images and combines them. 
A simple formula is used ->
new_pixel = alfa * pixel_1 + beta * pixel_2 + gamma

## Grid Detection
Helps with the tracking of an object, if said object has a recognizable pattern. 
This is useful, because often cameras can create a distortino in an image, such as radial or tangential distortion. 

Grids are also used to calibrate cameras and track motion. 