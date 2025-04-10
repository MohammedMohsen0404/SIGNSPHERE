# SIGNSPHERE: Real-Time Sign Language Avatar for Football Commentary



<p align="center">
  <img src="https://github.com/user-attachments/assets/2a7c48ee-ec5c-4dbb-b32b-3e12cd5cdb02" height="300"/>
</p>

## Project Overview

SIGNSPHERE is designed to enhance the experience of hearing-impaired individuals watching football matches. Using AI-powered technology, we convert live football commentary into sign language through a dynamic avatar. The system captures the audio commentary, transcribes it in real-time, translates it to sign language, and displays the translation using a 3D avatar.

The goal is to provide an inclusive viewing experience that enables people with hearing disabilities to enjoy football matches in real-time, with the same level of engagement as hearing viewers.

## Features

- **Real-Time Speech-to-Text Conversion**: The system uses OpenAI's Whisper to transcribe live commentary into text.
- **Text-to-Sign Language Translation**: The transcribed text is converted into sign language using Mistral and appropriate linguistic models.
- **3D Avatar Representation**: A dynamic 3D avatar displays the sign language translation to provide an immersive experience.
- **Low Latency Processing**: The system processes commentary and translates it into sign language in near real-time.
- **Customizable Settings**: Users can adjust the avatar's size, speed, and position to match their preferences.

## Technologies Used

1. **OpenAI Whisper**: For real-time speech-to-text conversion.
2. **Mistral**: To convert text into sign language text, simplifying the language by removing unnecessary words.
3. **Groq Framework**: To access and integrate large language models (LLMs) with Python for efficient processing.
4. **Web Search**: For retrieving relevant sign language videos from online platforms like [Signing Savvy](https://www.signingsavvy.com) and [Signals](https://www.signals.com).
5. **3D Animation Tools**: Used to render the sign language translations with a dynamic avatar.

## Data Used

We are experimenting with two approaches to identify the most effective method for real-time sign language translation:

1. **Ready Videos from Websites**: Pre-recorded sign language videos sourced from websites like Signing Savvy and Signals. These provide high-quality translations but introduce latency due to the need to search and match appropriate clips in real-time.
2. **Text to Key Points from Open Source Datasets**: We extract key points from open-source datasets and transcribe them into sign language. This approach is more flexible for real-time use but lacks the polished visual appeal of pre-recorded videos.

### Comparison
- **Ready Videos**: Provide high-quality sign language representations but have **latency** in fetching and synchronizing clips.
- **Text to Key Points**: Works in real-time with **minimal latency**, but the output may not be as visually refined as video-based sign language.


## Challenges

- **Limitations on Video Uploads**: Restrictions set by external websites (like Signing Savvy) for downloading videos may limit the ability to find suitable sign language clips.
- **Video Production Latency**: There is a delay in collecting and synchronizing videos with live commentary, which can cause latency in real-time processing.
- **Real-Time Delivery**: Ensuring fast and accurate output for live events is crucial to provide a seamless experience for users.

## Installation

### Prerequisites
- Python 3.x
- OpenAI API key for Whisper
- Mistral model for text-to-sign conversion
- Groq framework for efficient model integration

### Steps to Set Up

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/SIGNSPHERE.git
   cd SIGNSPHERE
