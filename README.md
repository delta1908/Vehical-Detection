# Vehical-Detection


# File Structure
├── Frames 

├── model.ipynb 

├── README.md 

# Commands

**Setup:**
```
pip install opencv-python
pip install matplotlib
pip install numpy
```
# Input Format

**Unique Frame:**

path

x1 y1 x2 y2

frame_number

**Entire Video:**

path

x1 y1 x2 y2

**Once "bounded function" is called it creates a new image file in the same directory with final contours.**

# Approach
Counting number of vehicles to the left of line in an image.



FrameCapture Function is used for extracting all the frames from a video and puts it in a folder called Frames.

col_frames holds the image matrix of all the frames obtained from the image.

after applying thresholding, dialation we are able to diffrenciate between two consecutive frames.

Now that the moving objects have more solid highlighted regions we move on to count the contours in the image.

I first get all the contours in the image then add some conditions to get only the required ones(isLeft(x1,y1,x2,y2,x,y)), where isLeft function basically checks if a point lies to the left of a line.

For custom input run the last cell and enter the correct file path where the video is present, enter the 4 coordinates(space seperated) for the line and the frame number.
