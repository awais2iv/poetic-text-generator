# 🎭 AI Poetic Text Generator 🎭  
_A Deep Learning and Evolutionary Algorithm-based Shakespearean Poetry Generator_

---

## 👥 Group Members

| Name                  | Student ID |
|-----------------------|------------|
| Muhammad Qasim Nauman | 221345     |
| Muhammad Awais        | 221453     |

---

## 📌 Project Summary

This project is an intelligent poetic text generator that uses a **pre-trained LSTM model** to generate Shakespearean-style poems, enhanced through a **Genetic Algorithm (GA)** for better diversity and structure. The final poem is also converted to speech using TTS libraries and served through a **React.js frontend** and **FastAPI backend**.

---

## 🧠 AI Techniques Used

### ✅ LSTM (Long Short-Term Memory)
- Trained on Shakespeare's text (character-level)
- Predicts next characters for poem generation

### ✅ Genetic Algorithm
- Evolves generated outputs for quality using a fitness function:
  - Vocabulary diversity
  - Line structure

### ✅ Text-to-Speech (TTS)
- Uses `gTTS` and/or `pyttsx3` to produce an `.mp3` audio version of generated poems

---

## 📁 Project Structure

poetic-text-generator/
├── backend/
│ ├── model/
│ │ ├── meta.txt
│ │ └── textgenerator.keras
│ ├── static/
│ │ └── output_*.mp3 # Generated audio files
│ ├── .gitignore
│ ├── generate.py # GA + LSTM logic
│ ├── Model.py # LSTM model loading + generation
│ └── requirements.txt
├── frontend/
│ └── [React app files]
├── README.md
