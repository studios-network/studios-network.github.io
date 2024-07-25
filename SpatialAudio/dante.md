# Dante Guide

## *Introduction*  
The Dante Protocol uses ethernet to communicate between audio devices on a shared network. 

## Step 1: Dante Virtual Soundcard: 
1. *Launch Dante Virtual Soundcard* (image) 

   - Configure the following properties:  
     - *Audio Interface*: Select the appropriate driver (WDM or ASIO) (See Computer Audio and Spatial Audio sections for more information).  
     - *Audio Channels*: Set to 8x8 minimum, 16x16 recommended, which is formatted as (Ch. Input x Ch. Output).  
     - *Latency*: Set to 6 ms.  
     - *Network Interface*: Choose "Dante Audio Network".  
   - If properties are grayed out and there is a “stop” button, the Virtual Sound Card is active.  (image)

## Step 2: Dante Controller: 
2. *Launch Dante Contoller* (image) 

   - “aries400733” is the name given to the running instance of Dante Virtual Soundcard.
   - “unD32-10cd8a” is the networked break-out box being used to send audio from the computer over ethernet to the speakers
via analog. (image)

3. *Routing Matrix*  
   - The routing matrix shows where audio is being received and transmitted.  
   - Use “+” at intersections to see the routing connections (called “subscriptions”)..  
   - Confirm successful connections with green check marks. If the intersecting boxes are empty, click on them to
make the connections as shown below.

4. *More Information*  
   - For additional details, consult:  
     - [Dante Virtual Soundcard](https://dev.audinate.com/GA/dvs/userguide/webhelp/content/front_page.htm)  
     - [Dante Controller](https://dev.audinate.com/GA/dante-controller/userguide/webhelp/content/front_page.htm)
