# Visual Inspection of Motorcycle Connecting Rods
### Abstract
Blob analysis is the set of processes that aims to extract specific features from scene objects, usually referred to as *blobs*. 
\
This project aims the extraction of many features from a set of images where many rods are found within. In particular, for each blob the following features are required:

* Classification/type of the rod (there are only 2 types).
* Position and Orientation (modulo π).
* Length (*L*), Width (*W*).
* Width at the barycenter (*Wb*).
* For each hole, position of the centre and diameter size.

Also, many changes may affect the images:
* Images may contain other objects (i.e. screws and washers) that need not to be analysed by the system (such kind of objects are often referred to in computer vision as “distractors”)
* Rods can have contact points but do not overlap one to another.  
* The inspection area may be dirty due to the presence of scattered iron powder.

### This work has been done as a project for the *Computer Vision and Image Processing* course, University of Bologna (UNIBO)

# Dependencies
* NumPy(1.19.3)
* OpenCV(4.5.3)

# Example
### Input Image:
![Source Image](https://i.imgur.com/wE8LIvB.png)

### Output Images:
![1](https://i.imgur.com/Rme2Go4.png)  
![2](https://i.imgur.com/SlB47Gx.png)
![3](https://i.imgur.com/rkMN665.png)
