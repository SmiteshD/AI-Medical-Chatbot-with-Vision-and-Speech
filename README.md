# 🏥 AI Medical Chatbot with Vision and Speech

A multimodal AI-powered chatbot that simulates a real-world doctor consultation by analyzing **patient speech** and **medical images** to provide concise medical advice. Built using **Groq's 
OpenAI Whisper & LLaMA-4-Scout**, **ElevenLabs TTS**, and deployed with **Gradio** for an interactive experience.

## 🖼️ Demo

> *(Add a screenshot of the Gradio interface if possible here)*

## ✨ Features

- 🎤 **Voice Input**: User can describe their symptoms through speech, transcribed using Groq's OpenAI Whisper (large-v3).
- 🩻 **Image Understanding**: Uploads like X-rays or photo scans are processed with LLaMA-4-Scout for visual diagnosis.
- 🧠 **Contextual Diagnosis**: Combines voice and image inputs to generate doctor-like responses.
- 🔊 **Voice Output**: Responses are converted to natural speech using ElevenLabs' Aria voice model.
- 🖼️ **Interactive UI**: Built with Gradio to allow real-time audio/image input and output.

## 🧰 Tech Stack

- **LLM & Vision Model**: Groq - LLaMA-4-Scout (17B Instruct)
- **Speech Recognition**: Groq - OpenAI Whisper Large V3
- **Text-to-Speech**: ElevenLabs API (Aria, Turbo v2)
- **UI/Frontend**: Gradio
- **Audio Processing**: PyAudio, FFmpeg, Pydub, SpeechRecognition
- **Language**: Python 3

## 🚀 How It Works

1. 🎙️ Patient speaks into the mic and uploads a medical image (e.g. X-ray).
2. 🧠 Speech is transcribed using Groq's Whisper model.
3. 🖼️ The image and query are sent to Groq's LLaMA-4-Scout model for analysis.
4. 🗣️ A realistic response is generated and voiced out via ElevenLabs TTS.
5. 📋 The transcript and medical advice are shown, with audio playback.

## 📦 Installation

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/ai-medical-chatbot.git
   cd ai-medical-chatbot
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up your `.env` file:
   ```
   GROQ_API_KEY="your_groq_api_key"
   ELEVENLABS_API_KEY="your_elevenlabs_api_key"
   ```

4. Run the app:
   ```bash
   python ui.py
   ```

5. Visit `http://127.0.0.1:7860` in your browser.

## Installing FFmpeg

1. Visit the official FFmpeg download page: [An Internal Link](https://ffmpeg.org/download.html)
2. Navigate to the Windows builds section and download the latest static build.
3. Extract and Set Up FFmpeg:
   - Extract the downloaded ZIP file to a folder (e.g., C:\ffmpeg).
   - Add the bin directory to your system's PATH:
   - Search for "Environment Variables" in the Start menu.
   - Click on "Edit the system environment variables."
   - In the System Properties window, click on "Environment Variables."
   - Under "System variables," select the "Path" variable and click "Edit."
   - Click "New" and add the path to the bin directory (e.g., C:\ffmpeg\bin).
   - Click "OK" to apply the changes.


## ⚠️ Disclaimer

This chatbot is for **educational and demonstration purposes only**. It is **not a substitute** for professional medical advice, diagnosis, or treatment.
