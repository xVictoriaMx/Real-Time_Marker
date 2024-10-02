## **Real-Time Marker Detector and Tracer**

## **Overview**

The Real-Time Marker Detector and Tracer is a computer vision application that captures video input from a webcam to detect colored markers in real-time. Once a marker is detected, the program traces its movement on the screen, using the marker's color as the ink for drawing.

This project utilizes OpenCV for capturing video input, processing images, and detecting specific colors. The user can define different marker colors to be tracked, and the program will trace the movement of those markers, displaying the drawing on the screen in real-time.

## **Features**
 - Real-time detection of markers with specified colors
 - Dynamic tracing of marker movement on the screen
 - Adjustable color ranges for detecting different marker types
 - Efficient drawing with multiple markers using different colors

## **Prerequisites**
 - OpenCV 4.x or above
 - C++ 11 or above
 - A webcam or any video capture device

## **Core Logic and Functions**

To use Project Title, follow these steps:

1. **Video Capture:** The program starts by capturing video input from a webcam using OpenCV's VideoCapture class.
2. **Color Detection:** The function findColor(Mat img) converts the frame into HSV format and checks for specific colors. For each color, it creates a binary mask and calls getContours(Mat imgDilation) to find the contours of the detected marker.
3. **Contour Detection:** The function getContours(Mat imgDilation) analyzes the binary image to detect contours of a specific size, which correspond to the detected marker. It then finds the bounding rectangle around the marker and returns the center point.
4. **Drawing on Canvas:** The function drawOnCanvas() takes the points stored in upPoints and draws lines connecting the consecutive points. Each marker has a specific color from the defaultColorVals vector, and the program uses this color to draw the lines.



## **License**

MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

## **Authors and Acknowledgment**

Real-Time Marker Detector and Tracer was created by **[Victoria M](https://github.com/xVictoriaMx)**.
