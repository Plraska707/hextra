---
title: Tagliare video
type: docs
weight: 7
---


Ci sono due metodi, uno più veloce e uno con qualità migliore:

- Qualità migliore:

`ffmpeg -i video.mp4 -ss hh:mm:ss -to hh:mm:ss -async 1 cut.mp4`

- Più veloce:

`ffmpeg -i video.mp4 -ss hh:mm:ss -to hh:mm:ss -c:v copy -c:a copy output.mp4`