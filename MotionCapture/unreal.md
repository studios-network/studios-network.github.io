# Motive and MetaHumans Setup Guide

## Introduction
This guide provides a step-by-step process to integrate the data with Unreal Engine for MetaHumans animation using Motive.

## Step 1: Motive Setting:

1. Once you are done setting up Motive, the Rigid Body, and calibrating the cameras: 
2. *Configure Streaming Settings:*
   - Navigate to Edit > Settings > Streaming. (image)
   - Or Layout > Streaming.
   - Change the “Local Interface” setting to the IP address beginning with “198.82.19”. (change?)


## Step 2: Integrating with Unreal Engine

2. *Open Unreal Engine:*
   - Start Unreal Engine and open a new Project.

3. *Enable Plugins:*
   - Go to Edit > Plugins. (image)
   - Ensure that both “OptiTrack - Live Link” and “OptiTrack - Streaming Client” plugins are enabled. (image) (check two or three plugins)
   - Restart Unreal Engine if prompted.

4. *Setup LiveLink Source:*
   - Go to Window > Live Link to open the Live Link window. (image)
   - Click the + Source button and select OptiTrack Source. (image)
   - Click Create. (image)

6. *Verify Connection:*
   - Once connected, you should see assets from Motive appearing in Unreal Engine’s Live Link view, indicated by green circles. (image)

## Step 3: Setting Up MetaHumans

1. *Download MetaHumans:*
   - In Unreal Engine, go to the Window tab and open Quixel Bridge.
   - Sign in and navigate to the MetaHumans tab.
   - Select and download the desired MetaHuman character, adding it to your project. (image)

2. *Enable Missing Plugins:*
   - If prompted with pop-ups about missing plugins, enable all recommended plugins. (image)
   - Restart Unreal Engine after enabling these plugins.

3. *Create Animation Blueprint:*
   - Create an Animation Blueprint named ABP_(name of MetaHuman). (image)
   - Set the skeleton to metahuman_base_skel and the parent class to OptiTrackAnimInstance.
   - Click Create. 

4. *Configure Animation Blueprint:*
   - Open ABP_(name). If the AnimGraph isn’t visible, open it.
   - Add a LiveLinkPose node and connect it to the output pose node.
   - Select the LiveLinkPose node and change the retarget asset to OptiTrackLiveLinkRetarget.
   - Compile and save the Blueprint.

5. *Adjust MetaHuman Settings:*
   - In the Content Browser, locate the MetaHumans folder and find your MetaHuman.
   - Open the BP_(name) file.
   - Click on LODSync in the components window and set Forced LOD to 0.
   - Select the body component and under the details panel, navigate to mesh/skeletal mesh asset.
   - Set the Post Processing Anim Blueprint to the ABP_(name) created earlier.

  
### Useful links:  
Check out the video below for more information:
  - [Unreal Engine](https://drive.google.com/drive/folders/1o1ylpUgmxOkTpjF2N5syR45N1CYYgru5)
