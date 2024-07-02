**Adobe Premiere**
1. Open Adobe Premiere to synchronize your audio and video files. (image)
	>For more information refer to this link: [[AdobePremiereDemo.mp4](https://drive.google.com/file/d/1SWDYjDCX9tPOOgktKO-BIUdQUT021DJS/view?usp=share_link) or [Embedding audio in Depthkit assets](https://docs.depthkit.tv/docs/embedding-audio)]
2. To sync your audio and video files in Adobe Premiere Pro, follow these steps:
	-   Import both your audio and video files into your project panel.
	-   Drag both files onto your timeline.
	-   Select both the audio and video clips by holding down the shift key and clicking on each clip.
	-   Right-click on one of the selected clips and choose "Synchronize" from the context menu.
	-   In the Synchronize dialog box, make sure that "Audio" is selected as the synchronization point.
	-   Click "OK" to synchronize your clips.
	-   Check the synced clips by playing the timeline to make sure that the audio and video are in sync. (image for each)

3. You can encode your video files using FFmpeg by following this tutorial: [[Image Sequence encoding](https://docs.depthkit.tv/docs/asset-encoding)]. 
4. Open the command prompt and type these commands:

	**For Video Encoding:**
	> ffmpeg -i [C:\Users\nehasurana\Desktop\location of your video file] -c:v libx264 -x264-params mvrange=511 -c:a  aac -b:a 320k -shortest -vf scale='min(4096,iw)':'min(ih,4096)':force_divisible_by=2:out_color_matrix=bt709:out_range=full,setsar=1:1 -colorspace bt709 -color_primaries bt709 -color_trc bt709 -color_range pc -b:v 5M -pix_fmt yuv420p [ name of your final output file].mp4

	**For Image Sequence Encoding :**
    

	> ffmpeg -r 30 -f image2 -start_number 0 -i [ location of your first image sequence padded by “%06d”.png e.g: D:\Volcap_4030_Final\Exports\welcome3x2\TAKE_Welcome02_27_11_58_41_Export_04_03_13_20_49%06d.png] -c:v libx264 -x264-params mvrange=511 -c:a  aac -b:a 320k -shortest -vf scale='min(4096,iw)':'min(ih,4096)':force_divisible_by=2:out_color_matrix=bt709:out_range=full,setsar=1:1 -colorspace bt709 -color_primaries bt709 -color_trc bt709 -color_range pc -b:v 5M -pix_fmt yuv420p [ name of your output file].mp4
