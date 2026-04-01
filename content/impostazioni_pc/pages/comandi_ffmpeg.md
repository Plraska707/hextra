---
title: Comandi ffmpeg
type: docs
weight: 10
---

# Lista di comandi utili per ffmpeg:

## Tagliare video

### Qualità migliore:
``` bash
ffmpeg -i video.mp4 -ss hh:mm:ss -to hh:mm:ss -async 1 cut.mp4`
```

### Più rapido:
``` bash
ffmpeg -i video.mp4 -ss hh:mm:ss -to hh:mm:ss -c:v copy -c:a copy output.mp4`
```

## Tagliare due parti di un video e unirle
``` bash
ffmpeg -i vs_code_jupyter.webm -filter_complex \
"[0:v]trim=duration=8[a]; \
 [0:v]trim=start=23,setpts=PTS-STARTPTS[b]; \
 [a][b]concat[out1]" -map [out1] out.webm
 ```

## Blur singolo:
``` bash
ffmpeg -i origine.webm -filter_complex "[0:v]crop=270:430:50:170,boxblur=10:enable='between(t,2,5)'[fg]; [0:v][fg]overlay=50:170[v]" -map "[v]" -c:v libvpx-vp9 -c:a libopus output.webm  
```

## Blur doppio:
``` bash
ffmpeg -i input.webm -filter_complex "[0:v]crop=270:430:50:170,boxblur=10:enable='between(t,28,30.5)'[blur1]; [0:v]crop=650:438:639:76,boxblur=10:enable='between(t,65,75)'[blur2]; [0:v][blur1]overlay=50:170:enable='between(t,28,30.5)'[v0]; [v0][blur2]overlay=639:76:enable='between(t,65,75)'[v]" -map "[v]" -c:v libvpx-vp9 -c:a libopus output.webm
```