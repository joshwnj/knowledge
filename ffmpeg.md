# ffmpeg

## rotate a video 90 degrees

    ffmpeg -i in.mov -vf "transpose=1" out.mov

## resize a gif

Resize `in.gif` to be 320 px wide and maintain aspect ratio.

    ffmpeg -i in.gif -vf scale=320:-1 out.gif

## concat gifs

Note: might need to convert gifs to another format first, and then convert
them back again at the end.

    ffmpeg -f concat -i files.txt -codec copy all.mov

## make a video from frames

- [with concatdemuxer](_notes/2017-06/30-071.md)
