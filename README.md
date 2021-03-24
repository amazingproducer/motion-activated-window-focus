# motion-activated-window-focus

#### Scripts to support raising an RTSP stream into the foreground when motion is detected on said stream.
*A work in progress*

##### start_video_notifier
Starts and immediately hides a video playback window of the designated rtsp stream.

##### vlcrc
Configuration file for the video playback window. Removes key bindings, sets video zoom value, and applies the *minimal* control set. 

##### show_window
Brings video playback window to the foreground. Called by motion detection system at the beginning of a motion event.

##### hide_window
Hides video playback window from view. Called by motion detection system at the end of a motion event.