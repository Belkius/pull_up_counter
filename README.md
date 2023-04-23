# Rep Counter

This is a simple application that uses TensorFlow's [MoveNet](https://blog.tensorflow.org/2021/05/next-generation-pose-detection-with-movenet-and-tensorflowjs.html) model to count repetitions of pull-up exercises in real-time using a webcam.

## Demo
[Pull Up Counter Demo](https://belkius.com/repcounter)

## Installation
To use this application locally, you need to install the required packages. This application uses React, @tensorflow-models/pose-detection, and @tensorflow/tfjs-core. Run the following command to install the packages: `npm install`

## Usage
Run the following command to start the application: `npm start`

The application will start in your default browser at **http://localhost:3000/**. Click on the **Start** button to start detecting pull-ups. The camera feed will be displayed in real-time, and the number of reps will be displayed at the top of the screen. The application will stop detecting pull-ups when you click on the **Stop** button.

## Code Overview
The application is built using **React** and uses **@tensorflow-models/pose-detection** to detect pull-up exercises in real-time. The **RepCounter** component contains the main logic of the application. It uses the **useRef** and **useState** hooks to handle the camera feed and to update the state of the application.

The **startDetection** function is responsible for setting up the MoveNet model and for detecting the pull-ups. It uses **setInterval** to call the detection function every 100ms.

The **detectDownPosition** and **detectUpPosition** functions are used to detect the start and end of each pull-up exercise. They check the angle of the elbows to determine if the exercise is in the correct position. The **getAngle** function is used to calculate the angle between two points.

The **drawKeypoints** and **drawSkeleton** functions are used to draw the keypoints and the skeleton of the detected pose.
