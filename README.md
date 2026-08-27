Student AI Mentor

A student-focused learning companion built with a static frontend and AI-powered text-to-speech tooling.

Project Overview

This repository includes two main parts:

app.py: A Streamlit-based Text-to-Speech app using ChatTTS.
backend/: A FastAPI backend exposing a /tts endpoint to generate WAV audio from text.
frontend/: A static HTML/CSS frontend for the Thinksy student AI mentor dashboard and learning tools.
Key Features

Text-to-speech generation using ChatTTS.
Static student portal UI with pages for:
Home/dashboard (index.html)
Text to Speech (tts.html)
Quiz generator (quiz.html)
Smart summarizer (summarizer.html)
Progress tracker (tracker.html)
Video notes converter (video.html)
FastAPI backend for serving generated audio files.
Repository Structure

app.py - Streamlit entry point for a TTS demo.
requirements.txt - Python dependencies for the root app.
backend/app.py - FastAPI app that exposes a /tts endpoint.
backend/backend.py - Backend implementation that loads ChatTTS and returns WAV responses.
backend/requirements.txt - Backend-specific dependencies.
frontend/ - Static website assets and page templates.
Installation

Clone or download the repository.

Install the root dependencies:

pip install -r requirements.txt
Install backend dependencies:
cd backend
pip install -r requirements.txt
Running the Streamlit TTS App

From the repository root:

streamlit run app.py
This launches a small TTS demo where you can enter text, generate speech, play audio, and download the result.

Running the Backend API

From the backend/ directory:

uvicorn app:app --reload
Then open:

http://127.0.0.1:8000/ — API status endpoint
http://127.0.0.1:8000/tts?text=Hello — generates a WAV audio file from the supplied text
Frontend Preview

Open any of the files in frontend/ in a browser to preview the static Thinksy interface.

frontend/index.html
frontend/tts.html
frontend/quiz.html
frontend/summarizer.html
frontend/tracker.html
frontend/video.html
Note: The static frontend pages are currently stand-alone interfaces. If you want them to call the FastAPI backend, you can wire the client-side JavaScript to the /tts API.
Notes

ChatTTS is a key dependency for both the root Streamlit app and the backend.
The frontend uses browser speech APIs for the TTS page and UI-only flows for other features.

