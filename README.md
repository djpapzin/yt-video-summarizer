# YouTube Video Summarizer

This project uses modern AI techniques to automatically generate text summaries of YouTube videos.

## Overview

The program takes a YouTube video URL as input, downloads the video in the desired quality, transcribes the audio using Whisper, summarizes the transcription using LangChain, and outputs a text summary.

## Features

- Lets user specify video resolution for download 
- Downloads YouTube videos using yt-dlp
- Transcribes audio using Whisper STT model
- Summarizes long text using GPT-3.5 via LangChain
- Wraps summary text to 100 characters per line  
- Provides downloadable transcripts and summaries

## Usage

1. Install dependencies

    ```
    pip install -r requirements.txt
    ```

2. Set API keys as environment variables in `.env` file

3. Run `main.py`

    ```
    python main.py
    ```

4. Enter a YouTube video URL when prompted

5. Select desired video quality 

6. View and download the generated transcript and summary

## Implementation Details

- `download_mp4_from_youtube()` - Downloads video in MP4 format
- `whisper.transcribe()` - Converts video to text 
- `LangChain` - Uses GPT-3.5 model to summarize text
- `textwrap.fill()` - Wraps summary text nicely

## Requirements

See `requirements.txt`. Main libraries used:

- yt-dlp
- Whisper
- LangChain
- textwrap3

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)