# Spatial Audio (Multichannel) Guide

## *Introduction*
To create spatial audio experiences, specific software must be utilized that allows for multichannel routing and ambisonic playback.

### Note: Please be sure to check your levels before outputting audio from the computer. It is best to start with the sound off completely to avoid blasting your ears. Slowly increase the sound level.

## Step 1: Setup Dante Virtual Soundcard:  
1. Open Dante Virtual Soundcard and switch to "ASIO" interface.
   - If "WDM" is selected, press "Stop" at the bottom right of the window and change the interface to "ASIO" as shown here and press "Start".
   <p align="center">
     <img src="../images/sa/asio.PNG" width="396" height="287" alt="Open Device">
   </p>
   
   -  ASIO is used in pro-audio software, and will allow for multichannel routing.
 
  
## Step 2: Choose the Software:
### a. Reaper: is for multichannel audio routing, mixing, and basic audio effects.

1. *Launch Reaper*  
   - Import the sample Reaper template provided.  (where)

2. *Configure Output Device*  
   - Go to Options > Preferences.
   <p align="center">
     <img src="../images/sa/reaper.png" width="396" height="430" alt="Open Device">
   </p>
   
   - Set output range to Dante tx 1 to Dante tx 5 and sample rate to 48000 Hz.
   - Ensure that the settings match the ones shown in the picture below. 
   - Click "Apply" and "OK".
   <p align="center">
     <img src="../images/sa/set.PNG" width="396" height="285" alt="Open Device">
   </p>
   

3. *Routing Matrix*  
   - Go to View > Routing Matrix to access the "Routing Matrix" tab .
   <p align="center">
     <img src="../images/sa/matrix.png" width="396" height="182" alt="Open Device">
   </p>
   
   -  Use the routing matrix to direct where audio from specific tracks are output.
     <p align="center">
     <img src="../images/sa/tab.png" width="396" height="469" alt="Open Device">
   </p>
   

### b. MaxMSP: is for custom audio processing, interactive sound installations, and advanced audio effects not easily achieved in a DAW.
1. *Launch MaxMSP*  
   - Open the sample MaxMSP patch provided. (where)

2. *Configure Output Device*  
   - Go to “Options” > “Audio Status”.
     <p align="center">
     <img src="../images/sa/audio.png" width="300" height="300" alt="Open Device">
   </p>
   
   - Select "ad_asio Dante Virtual Soundcard (x64)" as the driver.
     <p align="center">
     <img src="../images/sa/name.png" width="396" height="212" alt="Open Device">
   </p>
   
   - Use “Open I/O Mapping” for routing configuration.
     <p align="center">
     <img src="../images/sa/open.png" width="363" height="521" alt="Open Device">
   </p>
   
   - Close the Audio Status window and begin patching.

[Click here to learn more about MaxMSP](https://cycling74.com/tutorials?page=1)
