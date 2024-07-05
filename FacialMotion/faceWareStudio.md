# Recording with Faceware Studio


## Introduction
This guide will help you set up and record high-quality video using Faceware Studio, and use the recorded data to animate a character.

## Step 1: Hardware Setup

1. [Click on this link to initiate the setup process for the necessary hardware for recording.](https://www.youtube.com/watch?v=kcALXTq6QIU)
2. Use the following image as a reference to get an overview of connections and components involved in the setup:
   <p align="center">
     <img src="../images/setup_overview.png" width="600" height="400" alt="Hardware Setup Overview"></p>

## Step 2: Record a Video Using Mark IV
1. *Launch Faceware Shepherd*:
   - Login using the username/password given on the key.
2. *Activate the Camera*:
   - Once all connections are established, power on the camera.
3. *Power Up the Teradek Bolt*:
   - Turn on the Teradek Bolt device.
4. *Begin Recording*:
   - If the Teradek Bolt displays "sending video" or if Faceware Shepherd shows "status ready", you're set to record.

## Step 3: Importing and Processing Video in Faceware Studio

1. *Importing Video*:
   - Import the recorded video into Faceware Studio by following these steps:
     - Open Faceware Studio.
     - Go to `File > Import` and select your video file.
     <p align="center">
       <img src="../images/faceware/import_video.png" width="400" height="300" alt="Import Video"></p>

2. *Tracking and Calibration*:
   - Initiate tracking and calibration within Faceware Studio:
     - Go to the Tracking tab.
     - Select your imported video.
     - Click on `Start Tracking` to begin the calibration process.
     <p align="center">
       <img src="../images/faceware/tracking.png" width="500" height="350" alt="Tracking and Calibration"></p>

3. *Animation Streaming*:
   - To stream animation data from Faceware Studio to your character, follow these steps:
     - Ensure your character rig is set up in the animation software.
     - Go to the Streaming tab in Faceware Studio.
     - Click `Start Streaming` to begin sending animation data.
     <p align="center">
       <img src="../images/faceware/streaming.png" width="500" height="350" alt="Animation Streaming"></p>

## Next Steps
1. *Live Link Plugin*:
   - Faceware provides a live link plugin to seamlessly stream data from Faceware Studio into Unreal Engine. [Click here for more information](Unreal.md)

2. *Using MetaHuman*:
   - If you opt to use MetaHuman instead of a custom character, [click here.](metaHuman.md)
