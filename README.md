# Body_Movement_Tracking
#فرقد_عدنان #farkadadnan #farkad_adnan

The   is a camera-based body movement tracking system that uses motion silhouettes to estimate the amount a person moves from a video of the person engaged in a task.
A software based system for tracking movement over time

Authors: Farqad Adnan

Contact: farkad.hpfa95@gmail.com

This software was developed using Microsoft Visual C# 2010 on a Windows 10 64-bit machine.

System requirements
The program was tested on the 64-bit version of Windows 10. It should work on Windows 10 32-bit. It may work on older or newer Windows devices, but this has not been tested.

Microsoft .NET Framework 4.0. The program will prompt you to install this the first time you run it if necessary, and will take you to the [Microsoft .NET Download Page]

You may need to install [Visual C++ 2010 Redistributable Package] (https://www.microsoft.com/download/en/details.aspx?displayLang=en&id=5555)

You may need to install new video codecs so that the software can decode/encode video files. Installing a program like [ffdshow] can

Possible installation problems
If you download the zip file, open the program, and run the demo, but the program crashes when trying to process the demo video file, you may not have proper video codecs installed. Try installing a program like [ffdshow], which installs several related codecs.


To select one AVI video file for processing, click "Select Input File". To select a directory for AVI video files for processing, click "Select input directory". To select a live cam feed to process, tap Capture From Camera.

You must specify a location to save the output files from the program. The program will automatically generate the motion time series and the midpoint of the motion time series. For example, if you choose to process a file called "video.avi", the program will create a file called "video-M.txt" with the motion time string, and a file called "video-C.txt" with the centroid time series. If you choose to save a video of animated silhouette frames, this file will be saved to "video-out.avi". If you choose to save the face region time series to a file, the output will be saved in 'video-ftxt'. If you are processing video from a live cam feed, you will have the option to choose if and where you want to save the recorded video.

Algorithm settings
Motion history image duration
The default value is 1000. The "memory" of the motion history image is in milliseconds, that is, the number of frames taken into account when determining the pixel density of the current motion history image. If the frame rate is 30 frames per second, setting this value to "1000" means that 30 frames will be used.
bi-threshold
BINARY_THRESHOLD: The default value is 30. After the silhouette mask is created from the latest video frame, the silhouette is selected to give a binary image. This value is the threshold.
Haar Object Detection Settings
Scale factor: default 1.1. How quickly the object detection scale increases with each pass over the image. Higher means faster, fewer passes, and you might miss things. Less means slower and more passes. The default OpenCv is 1.1 (10% increment on each pass).
MIN NEIGHBORS: Default 2. Slash level to eliminate or keep groups of rectangles (found objects) based on the number of initial finds in the group. Combines groups greater than this value and discards groups with less value. If the detector misses many things.
