# Determining the speed of an object from images

## Objective
To determine the distance travelled and speed of a car from two images of it driving, using MATLAB

## Solution
My code reads in two images from the user, along with the length of the car and the time at the two frames. 

It uses this information to first convert the color images to be binary images, with only the pixels of the car being white based on looking for the correct color for the car. It then finds the centroid of both cars which it uses to find the change in distance between the frames in terms of pixels. It also finds the length of the car in pixels based off the distance between the leftmost and rightmost white pixels. This length in pixels can be used with the given length of the car in feet to find the proper factor to use to convert from pixels to feet. This factor is then used to preform necessary conversions and speed is calculated using a simple formula with the given time between frames.

Outputted is the given images and information from the user, followed by the binarized images with the centroids of both cars displayed with a blue star. Finally the calculated distance travelled and speed are outputted.

## Limitations/Growth Potential
Because I did this as an assignment for a computer vision class in college, I had limited time and needed to be satisfied with only completing what was required. With that being said, the code could be improved in the following ways:
- Improved accuracy by taking more frames into account
  - Taking a video from input and extracting more frames would allow more data and a resonable change to the calculation of speed would result in more accuracy
  - using a video would also allow the time at each frame to not be inputted from the user, and rather calculated.
- More universal detection of object with a change of criteria
  - If I instead looked for the wheels via a Hough Transform for circles, I could look for any color car, though this could have issues if many cars are in frame
  - Could be adapted to find the speed of various other objects with a change to the object detection criteria.

## Example Input and Output
![](/SpeedOfCarOutput.jpg)
