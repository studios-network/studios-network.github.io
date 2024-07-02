# Recording with Faceware Studio


## Introduction
This guide will help you set up and record high-quality video using Faceware Studio, and use the recorded data to animate a character.

## Hardware Setup

1. [Click on this link to initiate the setup process for the necessary hardware for recording.](https://www.youtube.com/watch?v=kcALXTq6QIU)
2. Use the following image as a reference to get an overview of connections and components involved in the setup:
   <p align="center">
     <img src="images/setup_overview.png" width="600" height="400" alt="Hardware Setup Overview"></p>

## Steps to Record a Video Using Mark IV
1. *Launch Faceware Shepherd*:
   - Login using the username/password given on the key.
2. *Activate the Camera*:
   - Once all connections are established, power on the camera.
3. *Power Up the Teradek Bolt*:
   - Turn on the Teradek Bolt device.
4. *Begin Recording*:
   - If the Teradek Bolt displays "sending video" or if Faceware Shepherd shows "status ready", you're set to record.

## Importing and Processing Video in Faceware Studio

1. *Importing Video*:
   - Import the recorded video into Faceware Studio by following these steps:
     - Open Faceware Studio.
     - Go to File > Import and select your video file.
     <p align="center">
       <img src="images/faceware/import_video.png" width="400" height="300" alt="Import Video"></p>

2. *Tracking and Calibration*:
   - Initiate tracking and calibration within Faceware Studio:
     - Go to the Tracking tab.
     - Select your imported video.
     - Click on "Start Tracking" to begin the calibration process.
     <p align="center">
       <img src="images/faceware/tracking.png" width="500" height="350" alt="Tracking and Calibration"></p>

3. *Animation Streaming*:
   - To stream animation data from Faceware Studio to your character, follow these steps:
     - Ensure your character rig is set up in the animation software.
     - Go to the Streaming tab in Faceware Studio.
     - Click "Start Streaming" to begin sending animation data.
     <p align="center">
       <img src="images/faceware/streaming.png" width="500" height="350" alt="Animation Streaming"></p>

4. *Live Link Plugin*:
   - Faceware provides a live link plugin to seamlessly stream data from Faceware Studio into Unreal Engine:
     - Install the Live Link plugin in Unreal Engine.
     - In Faceware Studio, enable the Live Link plugin under Settings > Plugins.
     - Connect Faceware Studio to Unreal Engine using the Live Link plugin.
     <p align="center">
       <img src="images/faceware/live_link.png" width="500" height="350" alt="Live Link Plugin"></p>

5. *Using MetaHuman*:
   - If you opt to use MetaHuman instead of a custom character, follow these steps:
     - Open the MetaHuman Creator in Unreal Engine.
     - Import the animation data from Faceware Studio.
     - Apply the animation data to your MetaHuman character.
     - For detailed steps, refer to the "Epic MetaHuman Setup" section on this page.
     <p align="center">
       <img src="images/faceware/metahuman.png" width="500" height="350" alt="Using MetaHuman"></p>



## Troubleshooting Data Streaming Issues

If the data streaming seems unreliable:

1. Ensure the "Streaming to Client" toggle is activated in Faceware Studio.
2. Verify that the Live Link setup is operational under Window > Virtual Production > Live Link in Unreal Engine.
   <p align="center">
     <img src="images/faceware/troubleshooting.png" width="400" height="300" alt="Troubleshooting Data Streaming Issues"></p>

Faceware also offers live client plugins for Unity and MotionBuilder.

## Additional Information

- *Live Streaming*:
  - If you intend to live stream, ensure that AJA U-TAP is correctly configured and connected.
- *Faceware Software*:
  - Faceware provides four different software applications, each serving a unique purpose:
