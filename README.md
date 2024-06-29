# Audio Transcription with PyDub and Speech Recognition

This Python script demonstrates how to cut an audio file, chunk it into smaller segments, and transcribe those segments using the PyDub library for audio manipulation and the SpeechRecognition library for speech-to-text conversion.

## Prerequisites

- Python 3.x
- Install the required libraries using `pip install pydub SpeechRecognition`

## Usage

1. Replace `"Recording.wav"` with the actual path to your input WAV file.
2. Run the script.
3. The audio will be cut from 15 minutes to 35 minutes and saved as `"CutAudio.wav"`.
4. The audio will be chunked into smaller segments (default length: 1 minute).
5. Each chunk will be transcribed using Google's speech recognition service.
6. The full transcription will be printed to the console and saved in `"transcription.txt"`.

## Example

```python
from pydub import AudioSegment
import speech_recognition as sr
import os

# Function to cut the audio from 5 mins to 20 mins
# ...

# Function to chunk audio into smaller segments
# ...

# Function to transcribe audio chunks
# ...

# File paths
input_wav_file = "Recording.wav"
output_wav_file = "CutAudio.wav"

# Cut the audio from 5 mins to 20 mins
cut_audio(input_wav_file, output_wav_file, start_min=15, end_min=35)

# Chunk the audio
chunks = chunk_audio(output_wav_file)

# Transcribe the audio chunks
transcription = transcribe_audio_chunks(chunks)
print("Transcription: " + transcription)

# Optionally, save the transcription to a file
with open("transcription.txt", "w") as file:
    file.write(transcription)
```

Remember to adjust the file paths and customize the script according to your specific requirements.
