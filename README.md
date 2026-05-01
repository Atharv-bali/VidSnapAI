## Static Files (/static)

This directory contains all the assets that need to be served directly to the frontend.
Examples include:

Generated audio files
Processed media assets
Public resources used by the application

## User Uploads (/user_uploads)

This folder stores raw video files uploaded by users.

These files act as the input for processing, and are later:

Combined
Transformed
Converted into final reel videos

## text_to_audio.py

This module is responsible for:

Converting user-provided text into high-quality audio
Using ElevenLabs API for realistic voice synthesis
Saving the generated audio into the /static directory

Essentially, it acts as the Text-to-Speech (TTS) engine of the system.

## generate.py

This script handles the core media processing pipeline.

It:

Takes input video clips (from /user_uploads)
Uses generated audio (from /static)
Executes FFmpeg commands to:
Merge clips
Resize to vertical format (1080×1920)
Add background audio
Generate final reel videos

Output is stored in the Reel Generator output directory

## main.py

This is the entry point of the application.

It orchestrates the full workflow:

Accepts user input (text + videos)
Calls text_to_audio.py → converts text into audio
Calls generate.py → creates the final reel using FFmpeg
