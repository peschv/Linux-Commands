# Linux-Commands
Useful Terminal commands for Ubuntu (so that I don't have to keep Googling it).
## Index
1. [Video](#video)
2. [Printer](#printer)
    1. [Cancel queue](#cancel-queue)
3. [Networking](#networking)
4. [Search](#search)

## Video
#### Remove all audio from video file - [Source](https://unix.stackexchange.com/questions/6402/how-to-remove-an-audio-track-from-an-mp4-video-file)
`ffmpeg -i input_file.mp4 -vcodec copy -an output_file.mp4`
## Printer <a name="printer"></a>
#### Show queue - [Source](https://www.computerhope.com/unix/ulpstat.htm)
`lpstat -R` <br>
or <br>
`lpstat -o`
#### Display printer info
`lpstat -t`
#### Cancel queue
Note: printerID or printerJobID is obtained from lpstat command.
[Source](https://askubuntu.com/questions/350334/how-do-i-clear-a-print-queue-in-ubuntu)
##### -- cancel all jobs
`cancel -a {printerID}`
##### -- cancel single job
`cancel {printerJobID}`
## Networking
#### Restart network manager - [Source](https://linuxconfig.org/how-to-restart-network-on-ubuntu-18-04-bionic-beaver-linux)
`sudo service network-manager restart`
## Search
#### Find full path of file name - [Source](https://stackoverflow.com/questions/5265702/how-to-get-full-path-of-a-file)
`readlink -f {filename.txt}`
