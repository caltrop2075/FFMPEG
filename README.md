# ffmpeg

automated ffmpeg stuff

see individual scripts for instructions

ffmpeg-hflip.sh
--------------------------------------------------------------------------------
video horizontal flipper
ffmpeg-hflip.sh -> ffmpeg.sh -> hflip video

put video in '$HOME/Downloads/hflip' add '*-R.*' before extension
then check the video...

2023-10-13 fully automated hflip

ffmpeg-[name].sh & ffmpeg.sh
are in $HOME/bin, not in $HOME/.local/bin, for ease of editing
ffmpeg is so FUCKED in scripts, loops don't work...
the minimal ffmpeg display - shows progress with no overwrite
ffmpeg -loglevel error -stats -n -i input.mkv output.mp4


ffmpeg-make.sh
--------------------------------------------------------------------------------
video converter
ffmpeg-make.sh -> ffmpeg-[dir].dat -> ffmpeg.sh -> converted video

put video in '$HOME/Downloads/[directory]'
directory name must start with capitol character, lower case will not process
add [directory] case conditions, what is most numerous or deisrable
nothing but the computer plays mkv & downloads are mixed: mkv, mp4, webm

ffmpeg-[name].sh & ffmpeg.sh
are in $HOME/bin, not in $HOME/.local/bin, for ease of editing
ffmpeg is so FUCKED in scripts, loops don't work...
the minimal ffmpeg display - shows progress with no overwrite
ffmpeg -loglevel error -stats -n -i input.mkv output.mp4

2023-10-13 made multi-functional & limited info
    no more ffmpeg PAGE of info, just the progress & errors
    creates 'ffmpeg-[dir].sh' for each directory to process       <<< obsolete
2023-10-14 scans downloads directories
    added delete ffmpeg-[dir].sh to ffmpeg-make.sh & ffmpeg.sh
    now fully automated except case conditions
2023-10-20 added script data files 'ffmpeg-[dir].dat'
    easier to delete without complicated filters
    easier to build 'ffmpeg.sh' with 'source ffmpeg-[dir].dat'
    also no mor chmod to a script
2023-10-25 fixed output glitch, '> $out' on wrong loop


ffmpeg.sh
--------------------------------------------------------------------------------
