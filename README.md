# motion-activated-window-focus

#### Scripts and snippets to support raising an RTSP stream into the foreground when motion is detected on said stream.

##### Determine PID and window ID for spawned RTSP playback window:
```bash
vlc $RTSP_STREAM_URL & export VID_PID=$!
export VID_WIN=`xdotool search --all --onlyvisible --pid $VID_PID --name vlc`
xdotool windowunmap $VID_WIN
```

##### Bring the RTSP playback window to the foreground:
```bash
xdotool windowmap $VID_WIN
```
