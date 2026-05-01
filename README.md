## Need of static
Files that needs to be shown on site, will be served in static folder

## User uploads
Inside this, the user uploaded video will be saved which needs to get converted

## text_to_audio.py
This folder takes in the text and carefully converts it to audio, and stores it inside static folder.

## generate.py
This uses the ffmpeg command to convert the text to audio and generate the reels which will be stored inside reel generator

## main.py
This uses the text_to_audio to convert the text to audio using eleven lab keys and generate_process.py generates the reel by using the ffmpeg command.
