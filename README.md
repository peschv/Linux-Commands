# Linux-Commands
Useful Terminal commands for Ubuntu (so that I don't have to keep Googling it).
## Index
1. [Video](#video)
    1. [Remove all audio from video file](#remove-all-audio-from-video-file)
3. [Printer](#printer)
    1. [Display queue](#display-queue)
    2. [Display printer info](#display-printer-info)
    3. [Cancel queue](#cancel-queue)
4. [Networking](#networking)
    1. [Restart network manager](#restart-network-manager)
5. [Files](#files)
    1. [Find full path name of a file](#find-full-path-name-of-a-file)
    2. [Convert files to pdf](#convert-files-to-pdf)
    3. [Merge pdf files](#merge-pdf-files)
6. [Scripts](#scripts)
    1. [Watch what script does](#watch-what-script-does)

## Video
#### Remove all audio from video file
`cd` into relevant folder containing the input file <br>
`ffmpeg -i input_file.mp4 -vcodec copy -an output_file.mp4` [Source](https://unix.stackexchange.com/questions/6402/how-to-remove-an-audio-track-from-an-mp4-video-file)
## Printer
#### Display queue
`lpstat -R` [Source](https://www.computerhope.com/unix/ulpstat.htm) <br> 
or <br>
`lpstat -o`
#### Display printer info
`lpstat -t`
#### Cancel queue
Note: printerID or printerJobID is obtained from lpstat command.
[Source](https://askubuntu.com/questions/350334/how-do-i-clear-a-print-queue-in-ubuntu)
##### -- cancel all jobs
`cancel -a printer_ID`
##### -- cancel single job
`cancel printer_job_ID`
## Networking
#### Restart network manager
`sudo service network-manager restart` [Source](https://linuxconfig.org/how-to-restart-network-on-ubuntu-18-04-bionic-beaver-linux)
## Files
#### Find full path name of a file
`readlink -f filename.txt` [Source](https://stackoverflow.com/questions/5265702/how-to-get-full-path-of-a-file)
#### Convert files to pdf 
`convert image1.jpg image2.png output_filename.pdf` [Source](https://askubuntu.com/questions/303849/create-a-single-pdf-from-multiple-text-images-or-pdf-files) <br>
Note: this uses ImageMagick. May need to download first:
`sudo apt install imagemagick`<br>
If converting to pdf results in a permission denied error, modify policy.xml PDF rights from "none" to "read|write" per [these instructions](https://stackoverflow.com/questions/42928765/convertnot-authorized-aaaa-error-constitute-c-readimage-453/52661288#52661288).
#### Merge pdf files
`pdfunite file1.pdf file2.pdf file3.pdf merged_file.pdf` [Source](https://stackoverflow.com/questions/2507766/merge-convert-multiple-pdf-files-into-one-pdf)
## Scripts
#### Watch what script does
`bash -x script_name.sh` [Source](https://tldp.org/LDP/Bash-Beginners-Guide/html/sect_02_03.html) <br>
This runs the script in debug mode.
