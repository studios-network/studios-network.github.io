# Motive and MetaHumans Setup Guide

## Introduction
This guide provides a step-by-step process to integrate the data with Unreal Engine for MetaHumans animation using Motive.

## Step 1: Motive Setting:

1. Once you are done setting up Motive, the Rigid Body, and calibrating the cameras: 
2. *Configure Streaming Settings:*
   - Navigate to Edit > Settings > Streaming.
   <p align="center">
     <img src="../images/MC/edit.png" width="199" height="179" alt="Open Device"></p>
     

   - Change the “Local Interface” setting to the IP address beginning with “198.82.19”.
   <p align="center">
     <img src="../images/MC/ip.png" width="396" height="418" alt="Open Device"></p>


## Step 2: Integrating with Unreal Engine

1. *Open Unreal Engine:*
   - Start Unreal Engine and open a new MetaHuman Project.

2. *Enable Plugins:*
   - Go to Edit > Plugins.
   <p align="center">
     <img src="../images/MC/edit.png" width="391" height="347" alt="Open Device"></p>
     
   - Ensure that both “OptiTrack - Live Link” and “OptiTrack - Streaming Client” plugins are enabled.
   <p align="center">
     <img src="../images/MC/plugin.png" width="396" height="132" alt="Open Device"></p>
     
   - Restart Unreal Engine if prompted.

3. *Setup LiveLink Source:*
   - Go to Window > Virtual Production > Live Link to open the Live Link window.
   <p align="center">
     <img src="../images/MC/link.png" width="396" height="149" alt="Open Device"></p>
     
   - Click the + Source button and select OptiTrack Source.
   - Click on Create.
   <p align="center">
     <img src="../images/MC/source.png" width="396" height="212" alt="Open Device"></p>
     

4. *Verify Connection:*
   - Once connected, you should see assets from Motive appearing in Unreal Engine’s Live Link view, indicated by green circles.


## Step 3: Setting Up MetaHumans

1. *Create Animation Blueprint:*
   - Create an Animation Blueprint named ABP_(name of MetaHuman).
 <p align="center">
     <img src="../images/MC/anim.png" width="396" height="425" alt="Open Device"></p>

     
   - Set the skeleton to metahuman_base_skel and the parent class to OptiTrackAnimInstance.
   - Click on Create.
 <p align="center">
     <img src="../images/MC/base.png" width="396" height="633" alt="Open Device"></p>

2. *Configure Animation Blueprint:*
   - Double click on ABP_(name). If the AnimGraph isn’t visible, open it.
   - Add a LiveLinkPose node and connect it to the output pose node.
 <p align="center">
     <img src="../images/MC/pose.png" width="396" height="225" alt="Open Device"></p>

 <p align="center">
     <img src="../images/MC/connect.png" width="396" height="160" alt="Open Device"></p>

   - Select the LiveLinkPose node and change the retarget asset to OptiTrackLiveLinkRetarget.
 <p align="center">
     <img src="../images/MC/target.png" width="396" height="55" alt="Open Device"></p>
     
   - Compile and save the Blueprint.


3. *Adjust MetaHuman Settings:*
   - In the Content Browser, locate the MetaHumans folder and find your MetaHuman.
   - Open the BP_(name) file.
   - Click on LODSync in the components window and set Forced LOD to 0.

 <p align="center">
     <img src="../images/MC/zero.png" width="396" height="554" alt="Open Device"></p>
     
   - Select the body component and under the details panel, navigate to mesh/skeletal mesh asset.
 <p align="center">
     <img src="../images/MC/mesh.png" width="396" height="269" alt="Open Device"></p>
     
   - Set the Post Processing Anim Blueprint to the ABP_(name) created earlier.
 <p align="center">
     <img src="../images/MC/set.png" width="396" height="550" alt="Open Device"></p>

   - Drag and drop the main MetaHuman BP_(name) asset into your level and.
   - To test if it worked is if the MetaHuman stands in the Motive default T-Pose instead of the MetaHuman default A-Pose.
 <p align="center">
     <img src="../images/MC/final1.png" width="396" height="215" alt="Open Device"></p>

  
### Useful links:  
Check out the video below for more information:
  - [Unreal Engine](https://drive.google.com/drive/folders/1o1ylpUgmxOkTpjF2N5syR45N1CYYgru5)
