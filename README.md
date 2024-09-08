# my alter ego
Collection of my audio journal, hosting and transcription


## Goals
- Provide a space to collect all of the audio tidbits I collect
- Allow for tagging of said bits by topic
- Parse the text of these recordings for transcription or other purposes
- In X years, look back and chuckle :)

## Vision
A simple 3 page site:
1. Upload a recording and add tags etc
2. View my entire life in recordings
   - Provide a time based heatmap homepage that is a box for everyday in my life, think [like the github calendar]((https://cal-heatmap.com/)
1. Tag searching and recording context searching, or date range
   - maybe elastisearch through the text?, tag matching
1. Status Page
     - Sync Status and naming conflicts
     - Recent imports
     - Total hours recorded, num recordings etc,
1. each recording has an individual page to ad context and view the transcript
  

## Implementation
- SQLITE for storing paths to files and their tags
- File storage laid out in specific folder structure
- [openai whisper](https://github.com/openai/whisper)? to get transcripts 
- uses syncthing to have a 6month or so queue of recordings, these are scanned, and hashed based on contents(to deal with name conflicts), copy files
- Python Flask Gunicorn Docker Compose to serve and build the app
- Locally running only

## Development Plan
1. build database schema, in Python
2. Add simple data
3. Build simple frontend that has a page to individually look at recorings
   - Add Calendar based visual
   - Plays audio
4. Write syncing script
5. Implement whisper
6. Implement tagging search
7. Implement content search
8. Honestly can't plan this far...
