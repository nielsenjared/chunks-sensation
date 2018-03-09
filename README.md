# Chunks of Sensation

Randomly selected video experiments.

## avconv Scripts 

avconv -i myvideo.mp4 -acodec libvorbis -aq 5 -ac 2 -qmax 25 -threads 2 myvideo.webm

avconv -i quickfox.mkv -c:v libtheora -qscale:v 10 -c:a libvorbis -qscale:a 7 quickfox.ogv

avconv -i quickfox.mkv -c:v libtheora -qscale:v 7 -an quickfox.ogv

avconv -i [input_file] -vcodec copy -an [output_file]

-an disables audio
https://libav.org/avconv.html#Audio-Options

-framerate _rate_

-filter:v "setpts=0.5*PTS"
https://trac.ffmpeg.org/wiki/How%20to%20speed%20up%20/%20slow%20down%20a%20video

avconv -framerate 15 -f image2 -i %04d.JPG -c:v libtheora -qscale:v 7 -s:v hd1080 -crf 1 out.ogg

avconv -i MVI_5976.MOV -ss 00:00:09 -t 00:00:50 -c:v libtheora -s:v hd1080 -qscale:v 7 -an out.ogg

avconv -i MVI_5976.MOV -framerate 60 -ss 00:00:09 -t 00:00:50 -c:v libtheora -s:v hd1080 -qscale:v 7 -an out.ogg
