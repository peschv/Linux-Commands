# Linux-Commands
Useful Terminal commands for Ubuntu.

## Video
#### Remove all audio from video file - [Source](https://unix.stackexchange.com/questions/6402/how-to-remove-an-audio-track-from-an-mp4-video-file)
`ffmpeg -i input_file.mp4 -vcodec copy -an output_file.mp4`
## Printer
#### Show queue - [Source](https://www.computerhope.com/unix/ulpstat.htm)
`lpstat -R` <br>
or <br>
`lpstat -o`
#### Display printer info
`lpstat -t`
#### Cancel queue - [Source](https://askubuntu.com/questions/350334/how-do-i-clear-a-print-queue-in-ubuntu)
Note: printerID or printerJobID is obtained from lpstat command.
##### -- cancel all jobs
`cancel -a {printerID}`
##### -- cancel single job
`cancel {printerJobID}`
