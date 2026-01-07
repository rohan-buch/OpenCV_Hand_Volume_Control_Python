# OpenCV_Hand_Volume_Control_Python
This is my first OpenCV project following a tutorial from [Sanyu Projects World](https://www.youtube.com/watch?v=nPzde1YG4ko&list=PLKikgSZ8GZYd7EXmKZSLwITvoCm0KFI5B&index=2).

# Dependencies

+ OpenCV
+ mediapipe
+ pyautogui

# How it works

After recognizing hand landmarks, each landmark is given an id. Ids 4 and 8 correspond to the tips of the thumb and pointer figner respectively. As per the Hands() function, the program is limited to two hands in the frame however is meant to only operate on one hand in view.

After recognizing the location of each point on the hand, the x and y positions are noted as per the frame length and width. These coordinates are used to measure the distances between the thumb and pointer finger using the following formula:

dist = ((x2-x1)**2 + (y2-y1)**2)**0.5//4

And a line is drawn between the two. When the distance is greater than 5 cm, the volume will increase (using pyautogui function) and when less than 5 cm, the volumme will decrease.

# Purpose

The purpose of this project is to introduce me into OpenCV as I am interested in software/hardware integration and I plan on using it in an upcoming Hackathon. This was a good introduction to OpenCV and broke a lot of barriers I thought would come with learning something like this.
