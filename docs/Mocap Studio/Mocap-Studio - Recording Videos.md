---
layout: default
title: Mocap-Studio - Video Recording
parent: Mocap Studio
nav_order: 4
description: "Guide to recording raw camera video using Mocap Studio, including enabling video mode, starting recordings, retrieving .h264 files from the server, and sharing recordings for support."
---

# AR51 Mocap Studio: Video Recording Guide
{: .no_toc }

Use Mocap-Studio to record the videos on the server.
{: .fs-6 .fw-300 }



---
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}


## Introduction
This tutorial demonstrates how to record video using AR51’s Mocap Studio. 
<br>
By default, AR51’s Mocap System **does not store video data** from the scene. 
<br>However, users have the option to enable video recording during their session.

When video recording is enabled, the raw camera footage is stored locally on AR51’s server. 
These recordings are valuable for debugging and troubleshooting any unexpected system behavior. If issues arise, recorded videos can help the AR51 team analyze and resolve them efficiently.

Note: The **FBX** file is saved locally on the machine running Mocap Studio, while recorded video files are always stored on **AR51’s server**.
{: .warning }

## Prerequisites
* Ensure that your system is operational.
* Ensure Mocap Studio is installed. 
If not, please refer to our setup guide before proceeding.


## Steps to Record Video
1. **Launch Mocap Studio**.
2. **Verify its connection to the server:** Check the top-left corner for two green indicator lights.

![1.connectivity.png](/assets/images/record_with_mocap_studio/1.connectivity.png)

3. **Enable Video Recording:** Before starting mocap data recording, click on the camera icon at the bottom of the interface. 
When activated, video recording will occur alongside mocap data.

![2.activating_video_mode.png](/assets/images/recording_a_video_with_mocap_studio/2.activating_video_mode.png)

4. **Start Recording:** Press the red record button at the bottom and enter a filename for your recording.

![3.click_record.png](/assets/images/recording_a_video_with_mocap_studio/3.click_record.png)

5. **Name your Recording:** Provide a descriptive name for your current recording.

![3.Provide_a_name.png](/assets/images/record_with_mocap_studio/3.Provide_a_name.png)

6. **Perform your desired activity**: Move around and perfom your desired action you wish to record
7. **Stop Recording:** Press the record button again to end the session.

![3.stop_record.png](/assets/images/recording_a_video_with_mocap_studio/3.stop_record.png)


### Storage and Retrieval
To access your video recordings:
1. **Log in** to the AR51 server.

![4.login.jpg](/assets/images/recording_a_video_with_mocap_studio/4.login.jpg)

2. Navigate to the **home folder** and open the **“Videos”** directory.

![5.find_videos_folder.png](/assets/images/recording_a_video_with_mocap_studio/5.find_videos_folder.png)

3. Locate your recording. It should have the name your provided in Mocap Studio with the addition of a timestamp.

![6.find_folder.png](/assets/images/recording_a_video_with_mocap_studio/6.find_folder.png)

4. In the recorded folder you should find .h264 videos along with the session meta data.
5. If you wish to view the recorded video you can open .h264 files using a program like VNC.
To do so, right click the file and select **"Open With VLC"**.

![7.open_with_vlc.png](/assets/images/recording_a_video_with_mocap_studio/7.open_with_vlc.png)

## Sharing Recorded Videos
1. Locate the most recent recording. 
2. Compress the folder.

![8.compress.png](/assets/images/recording_a_video_with_mocap_studio/8.compress.png)

3. Give the compressed file a name

![8.compress_name.png](/assets/images/recording_a_video_with_mocap_studio/8.compress_name.png)

4. Upload it to a cloud storage platform.
5. Share the link with the AR51 team for analysis and troubleshooting.


## Summary
By following these steps, you can efficiently record, access, and share video data using AR51’s Mocap Studio.

