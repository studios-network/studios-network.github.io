# Dante Guide

## *Introduction*  
The Dante Protocol uses ethernet to communicate between audio devices on a shared network. Dante relies on two applications to enable effective routing across devices: Dante Virtual Soundcard and Dante Controller.

## Step 1: Dante Virtual Soundcard: 
1. *Launch Dante Virtual Soundcard*


   - Configure the following properties:  
     - *Audio Interface*: Select the appropriate driver (WDM or ASIO) (See Computer Audio and Spatial Audio sections for more information).  
     - *Audio Channels*: Set to 8x8 minimum, 16x16 recommended, which is formatted as (Ch. Input x Ch. Output).  
     - *Latency*: Set to 6 ms.  
     - *Network Interface*: Choose "Dante Audio Network".
     - Click on "Start" once everything is set.  
   - If properties are grayed out and there is a “stop” button, the Virtual Sound Card is active.
   <p align="center">
     <img src="../images/sa/dvs1.PNG" width="396" height="287" alt="Open Device">
   </p>

## Step 2: Dante Controller: 
1. *Launch Dante Contoller*

   - “aries400733” is the name given to the running instance of Dante Virtual Soundcard.
   - “unD32-10cd8a” is the networked break-out box being used to send audio from the computer over ethernet to the speakers
via analog.
   <p align="center">
     <img src="../images/sa/dc.PNG" width="396" height="278" alt="Open Device">
   </p>

2. *Routing Matrix*  
   - The routing matrix shows where audio is being received and transmitted.  
   - Use “+” at intersections to see the routing connections (called “subscriptions”).
   - Notice that the Dante Virtual Soundcard instance is transmitting to 16 aries400733 receiver channels. This was defined when the Dante Virtual Soundcard was initiated.  
   - Confirm successful connections with green check marks. If the intersecting boxes are empty, click on them to
make the connections as shown below.
   <p align="center">
     <img src="../images/sa/16.PNG" width="396" height="448" alt="Open Device">
   </p>

### Useful links:  

   - [Dante Virtual Soundcard](https://dev.audinate.com/GA/dvs/userguide/webhelp/content/front_page.htm)  
   - [Dante Controller](https://dev.audinate.com/GA/dante-controller/userguide/webhelp/content/front_page.htm)


## Next Step:
You can choose to work with either: 
   - [Computer Audio (Stereo) Guide](stereo.md)
   - [Spatial Audio (Multichannel) Guide](multi.md)
