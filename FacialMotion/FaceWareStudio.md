
### Intro to Faceware Studio

Faceware Studio is software for tracking facial performance and animating a digital character in real-time. It's ideal for live events, on-set previsualization, and live online streaming with animated characters.

### Basic Workflow

1. *Launch FaceWare Studio*:
   - Open Studio.
   - In the *Realtime Setup* panel, choose your video input:
     - *Live* for live video (headcam/webcam).
     - *Media* for prerecorded video or image sequence.
   <p align="center">
     <img src="../images/faceware/setup.png" width="502" height="232" alt="Open Device">
   </p>

2. *Calibrate Your Actor*:
   - In *Realtime Setup, select **Face Tracking Model*:
     - *Stationary Camera* or *Professional Headcam* based on your footage.
   <p align="center">
     <img src="../images/faceware/camera.png" width="495" height="627" alt="Open Device">
   </p>
   - *Calibrate Neutral Pose*:
     - Have the actor look straight with a neutral expression.
     - Press "Calibrate Neutral Pose". Tracking landmarks will appear and the preview character will animate.
   <p align="center">
     <img src="../images/faceware/calibrate.png" width="495" height="627" alt="Open Device">
   </p>

4. *Stream Animation Data*:
   - Open the *Streaming Panel* (View > Panels > Streaming Panel if closed).
   - Enter the port number matching your Live Client plugin.
   - Turn on *Stream to Client* to start streaming animation data.
