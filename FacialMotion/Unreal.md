### Enabling the Plugin

1. Open Unreal Engine.
2. Go to `Edit > Plugins`.
   <p align="center">
     <img src="../images/unreal/edit.png" width="502" height="359" alt="Open Device">
   </p>
4. In the plugins window, select `Installed > Animation` and find *Faceware Live Link*.
   <p align="center">
     <img src="../images/unreal/window.png" width="1250" height="634" alt="Open Device">
   </p>
6. Enable the plugin and restart Unreal Engine if prompted.

### Connecting to Faceware Studio

1. In Unreal Engine, open `Window > Live Link`.
   - For Unreal Engine 5: `Window > Virtual Production > Live Link`. (check what is our version of unreal engine)
2. In the Live Link window, click `+Source` and select `Faceware Live Link`. Enter the IP address and port number to match your Faceware Studio input, and click **OK*.
3. In Faceware Studio, [set up your video stream](http://support.facewaretech.com/realtime-setup) and [calibrate your video](http://support.facewaretech.com/studio-calibration). Set the [Control Schema to "Standard"](http://support.facewaretech.com/studio-stream) and [start streaming to the client](http://support.facewaretech.com/studio-stream).
4. In Unreal, create a new animation blueprint: `Right-click in Content Browser > Animation > Animation Blueprint. Select your skeleton and click **OK`.
5. Open the blueprint and in the Event Graph, connect *Update Animation* to *Evaluate Live Link Frame*.
6. Set *animationValues* in the *Subject* dropdown and make sure *FacewareLiveLinkRole* is in the *Role* dropdown.
7. Drag from *Data Result* pin to create a *Break FTIAnimationBlueprintData* node.
8. Right click on *Animation Values*  on the new Break FTIAnimationBluePrintDate and select *Promote to Variable*.
9. Connect the *Exec* pin from *Evaluate Live Link Frame* to the *Set* node.

### Character Control Setup

1. In the *My Blueprint* panel, drag *Animation Values* into the AnimGraph and select *Get Animation Variables*.
2. Drag the pin from *Animation Values* and create a *Break FTIAnimationValueData* node.
3. For each shape, drag out from the pin and create a *Modify Curve* node.
4. Right-click on *Modify Curve*, add a curve pin, and select the control to drive with animation data.
5. Connect *Break FTIAnimationValueData* to the curve pin in *Modify Curve*.
6. Connect the final *Modify Curve* node to the *Output Pose* node.
7. Play your scene to animate your character with Faceware Studio data
