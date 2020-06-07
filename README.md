# REDOCS18

Commandes ffmpeg
======

Generate H.264 video from x image files
------

```bash
ffmpeg.exe -start_number 0 -i <Images_name> -c:v libx264 -vf "fps=<FPS>,format=yuv420p" <output_video_name>
````

Generate H.264 video from 1 image files
------

```bash
ffmpeg -loop 1 -i <Image_name> -c:v libx264 -t <Time_sec> -vf "fps=<FPS>,format=yuv420p" <output_video_name>
```

Extract png frames from video
------

```bash
ffmpeg.exe -i <Video_file_name> img%04d.png -hide_banner
```

Extract one png frame from video
------

```bash
ffmpeg -ss <time> -i <video_name> -vframes 1 -q:v 2 <output_img_name>.png
```

<time> : time of wanted frame in video, for frame at 2sec : 00:00:02


Commandes insert rectangle watermark in a frame

======

Compilation du programme
------

g++ insert_watermark.cpp -I. stb_image.h stb_image_write.h -o insert_watermark.out


Execution du programme
------

./insert_watermark.out <target.png> <output.png> <pattern>


example of patern  : 0101100110011001

