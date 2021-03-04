# motion-activated-window-focus

#### Scripts and snippets to support raising an RTSP stream into the foreground when motion is detected on said stream.

##### Determine PID and window ID for spawned RTSP playback window:
```bash
# Spawn the stream player and capture its PID
vlc $RTSP_STREAM_URL & export VID_PID=$!
# Wait for the window to be created before trying to set a variable against it
sleep 2
# Ascertain the relevant window's ID
export VID_WIN=`xdotool search --all --onlyvisible --pid $VID_PID --name vlc | head -1`
```

##### Hide the RTSP playback window:
```bash
xdotool windowunmap $VID_WIN
```

##### Bring the RTSP playback window to the foreground:
```bash
xdotool windowmap $VID_WIN
```
