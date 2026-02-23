# 📘 NotebookLM Clone

## 🔍 Overview

NotebookLM Clone is an AI-powered document understanding and audio generation application.  
It allows users to upload documents (PDF, PPT, etc.), process them into vector embeddings, and interact with the content using advanced Large Language Models (LLMs).

The system retrieves relevant context from the uploaded documents and generates intelligent, context-aware responses. It can also convert responses into natural-sounding audio.

---

## ✨ What This Project Does

- 📄 Extracts and processes content from uploaded documents
- 🧠 Converts text into embeddings using Sentence Transformers
- 🔎 Stores and searches embeddings using FAISS
- 🤖 Generates contextual answers using Groq-hosted LLMs
- 🔊 Converts generated responses into audio using Edge-TTS
- 🌐 Provides an interactive interface using Gradio

---

## ⚙️ How It Works (High-Level)

1. Documents are uploaded and parsed.
2. Text is split into chunks.
3. Each chunk is converted into embeddings.
4. Embeddings are stored in a FAISS vector database.
5. User queries are embedded and matched against stored vectors.
6. The most relevant content is sent to a Groq LLM.
7. The response is generated and optionally converted to audio.

---

## 🎯 Purpose

This project demonstrates how to build a Retrieval-Augmented Generation (RAG) system that combines:

- Vector Search
- Large Language Models
- Document Processing
- Text-to-Speech
- Interactive Web UI

It serves as a simplified educational clone of Google's NotebookLM concept.
An AI-powered document understanding and audio generation system built using:
- Groq LLMs  
- FAISS Vector Search  
- Sentence Transformers  
- Gradio UI  
- Edge-TTS  
- FFmpeg  
---

# Groq Setup

## Create a Groq Account

1. Open your browser.
2. Go to: https://console.groq.com
3. Click **Sign Up** (or Sign In if you already have an account).
4. Complete account verification if required.

---

## Generate a Groq API Key

1. After logging in, go to the Groq Console dashboard.
2. Click on your profile icon (top right corner).
3. Navigate to **API Keys**.
4. Click **Create API Key**.
5. Copy the generated key immediately.

⚠️ Keep this key private. Do NOT share or commit it to GitHub.

---

## Add Your Groq API Key to a `.env` File (Required)

In the root folder of the project (same folder as `app.py`), create a file named:

    .env

Open the `.env` file and add:

    GROQ_API_KEY=your_actual_api_key_here

Save the file.

⚠️ Important:
- Do NOT add quotes around the API key.
- Do NOT commit the `.env` file to GitHub.
- Make sure `.env` is included in your `.gitignore` file.
---


# 🛠️ Setup & Installation (Windows – Python 3.10 Recommended)
## 1. Navigate to Project Directory

    cd path\to\notebooklm_clone

Example:

    cd C:\Users\YourName\Desktop\notebooklm_clone

---

## 2. Create Python 3.10 Virtual Environment

    py -3.10 -m venv venv

---

## 3. Activate Virtual Environment

    venv\Scripts\activate

You should now see:

    (venv)

---

## 4. Install Project Dependencies

    pip install -r requirements.txt

---

## 5. Install Additional Required Packages

    pip install gradio==3.50.2 huggingface_hub==0.20.3
    pip install --upgrade edge-tts

---

## 6. Install FFmpeg (System Dependency)

Check if installed:

    ffmpeg -version

If not installed:

1. Download from: https://www.gyan.dev/ffmpeg/builds/  
2. Extract the files  
3. Add the `bin` folder to your System PATH  

---

## 7. (Optional) Upgrade pip

    python -m pip install --upgrade pip

---

# ▶️ Run the Application

    python app.py

You should see:

    Running on local URL: http://127.0.0.1:7860

Open the URL in your browser.

---
