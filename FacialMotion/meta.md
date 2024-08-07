# MetaHuman Setup Using Unreal Engine

## Step 1: Requirements
- *Faceware Studio*: [Download](https://facewaretech.odoo.com/downloads)
- *Faceware/Glassbox MetaHuman blueprint/motion logic sample*: [Download](https://drive.google.com/file/d/1mS2UF9Bkcqes2kkuUyGAx-W6g2Weo627/view?usp=sharing)
- *Live Client Plugin from Glassbox*: [Download](https://glassboxtech.com/products/live-client)
- *Epic’s MetaHuman sample scene*: [Download](https://www.unrealengine.com/marketplace/en-US/learn/metahumans)
- *Sample Facial Performance Video (Optional)*: [Download](https://drive.google.com/file/d/1i1HiXf0FIingfU-QQX4WmiqM0oBh9FZS/view?usp=sharing)

> *Note*: Use a clean project for best results.

## Step 2: *Prepare Your Project*
   - Unzip `FW_Metahuman_MotionLogic_Sample.zip` to a directory.
   - Create a new MetaHuman project and open the project directory.
   <p align="center">
     <img src="../images/unreal/ready.png" width="502" height="232" alt="Open Device"></p>


   - Drag the `MotionLogic` folder that you unzipped into the content folder of your project.
   <p align="center">
     <img src="../images/unreal/ready.png" width="502" height="232" alt="Open Device">
   </p>
   
## Step 3: *Setup MetaHuman Blueprint*
   - Locate your MetaHuman blueprint in Content/MetaHumans/[Blueprint File].
   - Right-click and select `Create Child Blueprint Class` and name it.
   <p align="center">
     <img src="../images/unreal/ready.png" width="502" height="232" alt="Open Device"></p>

     
   - Drag the new child blueprint into the scene.
   - Double-click the child blueprint, click `Add Component`, and add `Faceware Live`.
   <p align="center">
     <img src="../images/unreal/ready.png" width="502" height="232" alt="Open Device">
   </p>

## Step 4: *Configure Animation Components*
   - Select the Face component and set Anim Class to `ABP_FW_Metahuman_Face_C`.
   <p align="center">
     <img src="../images/unreal/ready.png" width="502" height="232" alt="Open Device">
   </p>
     
## Step 5: *Connect to Faceware Studio*
   - By default, LiveClient connects to Faceware Studio on 127.0.0.1:802.
   - Click on `Edit > Plugins` and make sure `Live Client for Unreal` is enabled.
   <p align="center">
     <img src="../images/unreal/ready.png" width="502" height="232" alt="Open Device">
   </p>

## Step 6: *Prepare Faceware Studio*
   - Ensure a video source is playing (live camera or pre-recorded video).
   - Calibrate on a neutral frame.
   - Open the Streaming Panel, set Control Schema to `Standard`, and turn on `Stream to Client`.
   <p align="center">
     <img src="../images/unreal/ready.png" width="502" height="232" alt="Open Device">
   </p>

## Step 7: *Animate Your MetaHuman*
   - In Unreal Engine, press Play and enable `Simulate` to see your MetaHuman animating.
   <p align="center">
     <img src="../images/unreal/ready.png" width="502" height="232" alt="Open Device"></p>

     
   - Use the Animation Tuning and Motion Effects panels for adjustments.
   - Explore the animation blueprints in the Motion Logic folder for additional customization.
