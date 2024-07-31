# Motive and Unreal Setup Guide

## Introduction
This guide will help you set up and integrate Motive and Unreal Engine for motion capture and animation projects.

## Step 1: Initial Setup in Motive

1. Launch Motive.
   - Upon launch, you may notice all cameras in a straight line, indicating they are not calibrated. (image)

2. Calibration of Cameras:
   - For a thorough explanation on how to calibrate the cameras, see this video.[Optitrack Calibration](https://drive.google.com/file/d/1HZ_CApepS6SpNlUBTgoetyYuwgrFyXnU/view)
Calibrate the cameras in the following situations:
- After a system restart
- When blue rings on the cameras turn off (indicating disconnection)
- Following any modifications to the truss setup
- If you sense irregularities in camera performance


### Camera Orientation
After calibration, orient the cameras:
1. *Switch to Grayscale Mode:* Right-click on each camera in Motive and change the mode to Grayscale for a clearer view.
2. *Adjust Orientation:* Right-click again and select "Orientation" to adjust the camera angles, ideally in 90-degree increments. Note that Motive allows adjustments in 5-degree increments.
3. *Return to Object Mode:* Once oriented, switch the cameras back to Object mode.

## Step 3: Using Unreal Engine

### Floor Auto-Adjustment
In Unreal, the floor auto-adjusts, so ensure all participants are standing during the setup.

### Additional Considerations
- Mask out unnecessary objects or markers, particularly those towards the ceiling, as this will simplify the setup process.

## Conclusion
This guide provides a framework for setting up Motive and Unreal Engine, complementing existing video tutorials. For any unresolved questions, please refer to the videos or contact Atlas Vernier.

For more detailed steps on post-setup processes like calibration and recording, refer to the respective sections in the linked tutorials.
