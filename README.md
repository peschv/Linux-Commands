# Linux-Commands
Useful Terminal commands for Ubuntu (so that I don't have to keep Googling it).
## Index
1. [Video](#video)
2. [Printer](#printer)
    1. [Display queue](#display-queue)
    2. [Display printer info](#display-printer-info)
    3. [Cancel queue](#cancel-queue)
3. [Networking](#networking)
    1. [Restart network manager](#restart-network-manager)
5. [Files](#files)
    1. [Find full path name of a file](#find-full-path-name-of-a-file)
    2. [Convert files to pdf](#convert-files-to-pdf)

## Video
#### Remove all audio from video file - [Source](https://unix.stackexchange.com/questions/6402/how-to-remove-an-audio-track-from-an-mp4-video-file)
`ffmpeg -i input_file.mp4 -vcodec copy -an output_file.mp4`
## Printer <a name="printer"></a>
#### Display queue
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
#### Restart network manager
`sudo service network-manager restart` [Source](https://linuxconfig.org/how-to-restart-network-on-ubuntu-18-04-bionic-beaver-linux)
## Files
#### Find full path name of a file
`readlink -f {filename.txt}` [Source](https://stackoverflow.com/questions/5265702/how-to-get-full-path-of-a-file)
#### Convert files to pdf 
This uses ImageMagick - download using `sudo apt install imagemagick`[Source](https://askubuntu.com/questions/303849/create-a-single-pdf-from-multiple-text-images-or-pdf-files)
`convert image1.jpg image2.png outputFileName.pdf`
If error (Permission Denied), modify policy.xml PDF rights from "none" to "read|write" per [these instructions](https://stackoverflow.com/questions/42928765/convertnot-authorized-aaaa-error-constitute-c-readimage-453/52661288#52661288).
