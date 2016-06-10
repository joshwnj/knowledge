# [](#ffmpeg)ffmpeg

## [](#rotate-a-video-90-degrees)rotate a video 90 degrees

    ffmpeg -i in.mov -vf "transpose=1" out.mov

## [](#resize-a-gif)resize a gif

Resize `in.gif` to be 320 px wide and maintain aspect ratio.

    ffmpeg -i in.gif -vf scale=320:-1 out.gif
