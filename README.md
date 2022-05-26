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

### This work has been done as a project for the *Computer Vision and Image Processing* course, University of Bologna (UNIBO


# Dependencies
* Python 3.7.11
* SciPy 1.7.1
* NumPy 1.21.5
* Matplotlib 3.5.0
* Sklearn 1.0.2
* Json 2.0.9

# Usage
To test the program, run the whole notebook on the desired image. \
To switch the image, you can edit the following string on the very first cell of code. 
``` 
img_path = 'img/TESI00.BMP'
```
Then, results may be found in the `out` folder.
To edit the output folder, modify the second cell of code:
``` 
OUT_DIR = 'out/'
```
# Example
### Input image:
![Source Image](https://i.imgur.com/HVmzU5l.png)

### Output image:
![1](https://i.imgur.com/UWVRQI4.png)  

### Output text:
```
------------------------- 1 -------------------------
Class: A, Angle: 0.349 rad, Centre: [ 91 111]
Length: 152, Width: 53, Width at barycentre: 20
Hole 1: Centre = [ 43 128], Diameter = 26
------------------------- 2 -------------------------
Class: A, Angle: 0.726 rad, Centre: [140 134]
Length: 165, Width: 50, Width at barycentre: 19
Hole 1: Centre = [ 99 169], Diameter = 26
------------------------- 3 -------------------------
Class: B, Angle: 0.278 rad, Centre: [177 164]
Length: 112, Width: 38, Width at barycentre: 19
Hole 1: Centre = [133 176], Diameter = 24
Hole 2: Centre = [214 154], Diameter = 26
```

### Output json:
```
{
    "1": {
        "class": "A",
        "angle": 0.349,
        "centre": [
            91,
            111
        ],
        "length": 152,
        "width": 53,
        "widthB": 20,
        "holes": [
            {
                "centre": [
                    43,
                    128
                ],
                "diameter": 26
            }
        ]
    },
    "2": {
        "class": "A",
        "angle": 0.726,
        "centre": [
...
            }
        ]
    }
```