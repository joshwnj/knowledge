# ffmpeg with concatdemuxer

Stitch together frames to make a video:

```
file '/path/to/dog.png'
duration 5
file '/path/to/cat.png'
duration 1
file '/path/to/rat.png'
duration 3
file '/path/to/tapeworm.png'
duration 2
file '/path/to/tapeworm.png'
```

https://ffmpeg.org/ffmpeg-formats.html#concat
https://trac.ffmpeg.org/wiki/Slideshow#Concatdemuxer

Thanks to [@zhewison](https://github.com/zhewison) for this nice tip :)
