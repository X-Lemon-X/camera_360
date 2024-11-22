# CXmara hanfdling
# list all video devices
```bash
v4l2-ctl --list-devices
```
# list all video formats
```bash
v4l2-ctl --list-formats-ext
```
# list all video controls
```bash
v4l2-ctl -d /dev/video0 --list-ctrls
```

# play video
```bash
ffplay -f v4l2 -input_format mjpeg -framerate 30 -video_size 3840x2160 -fflags nobuffer -vf "vflip" /dev/video0
```