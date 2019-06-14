![Screenshot](https://i.imgur.com/0CzFSNS.png)

# batch-convert
Convert a source directory of media to a target directory, with detailed ongoing progress to the terminal
- the shell script may be easily populated with directory names to allow copying media to a predefined directory structure, which will be duplicated on the target directory when run
- the log may also be sent to logfiles in a log directory, if selected
- enter "./batch-convert -h" to see all options

systst@systst-HP-ENVY-TS-15-Notebook-PC:~$ ./batch-convert -h

Usage: ./batch-convert [options [parameters]]

Options:
 -sd|--source, source directory I.E. -sd /media/systst/source-directory
 -td|--target, target directory I.E. -td /media/systst/target-directory
 -ad|--archive, archive directory (in case of problems e.g. power failure) I.E. -ad /media/systst/archive-directory
 -ld|--logs, logs directory (allow you to scan previous jobs) I.E. -ld /media/systst/logs-directory
 -e|--extension, target media extension (default is mkv) I.E. -e mkv
 -c|--codec, output video codec to use (default is h264) I.E. -c hevc
 -f|--fps, output frames per second to use (default is to calculate from input) I.E. -f 30
 -ac|--audiocodec, output audio codec to use (default is ac3, this overrides --basictranscode) I.E. -ac vorbis
 -ab|--audiobitrate, output bitrate to use (default is 128k, this overrides --basictranscode) I.E. -ab 320k
 -l|--logging, log to terminal AND to a separate log file (default is to terminal only) I.E. -l
 -b|--basictranscode, use basic transcoding I.E. -b
 -n|--nosubtitles, do NOT use subtitles (default is to transfer subtitles from source to target) I.E. -n
 -d|--debug, debug script (this adds a lot of output, but can be useful in troubleshooting problem media) I.E. -d
 -h|--help, Print help (this dialog) I.E. -h

./batch-convert converts a source directory of media to a target directory 
   using a target output format and codec
   and storing the source media to an archive directory, in case there are problems
   input media is probed to determine fps and duration (some source media can be near impossible to probe)

![Screenshot](https://i.imgur.com/RcrySfK.png)

![Screenshot](https://i.imgur.com/U4K0iL3.png)
