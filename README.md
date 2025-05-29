#  AI Poetic Text Generator   
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

##  AI Techniques Used

### LSTM (Long Short-Term Memory)
- Trained on Shakespeare's text (character-level)
- Predicts next characters for poem generation

###  Genetic Algorithm
- Evolves generated outputs for quality using a fitness function:
  - Vocabulary diversity
  - Line structure

###  Text-to-Speech (TTS)
- Uses `gTTS` and/or `pyttsx3` to produce an `.mp3` audio version of generated poems

---
 ### Justification for Techniques Used
In our project, Poetic Text Generator, we aimed to combine creativity and artificial intelligence to generate meaningful, stylistic poetry inspired by Shakespearean language. To achieve this, we carefully chose the techniques that would allow us to balance coherence, style, and innovation. Here's why we picked the tools and methods we used:

1. LSTM (Long Short-Term Memory) for Poem Generation
We chose LSTM networks because they’re great at handling sequences—like text—where previous context matters. Unlike regular neural networks, LSTMs can remember important information from earlier in the sequence, which helps in generating poetry that flows naturally rather than just spitting out random words.

We trained the model on Shakespeare’s work so it could learn the structure, vocabulary, and flow typical of that writing style. While newer models like Transformers (e.g., GPT) exist, they require way more resources and time to train properly. For our project’s scope and timeline, LSTM gave us the perfect balance of quality and manageability.

2. Genetic Algorithm to Improve Quality
Even though LSTM can generate pretty good poetry, it sometimes produces lines that feel off or repetitive. To solve this, we added a Genetic Algorithm to act like a filter. It picks the best outputs and evolves them over time using a fitness function we designed.

The fitness score is based on how varied and structured the poem is—things like line length, vocabulary richness, and rhythm. This makes sure the output feels more like actual poetry and less like random gibberish.


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

### Install dependencies using:

pip install -r requirements.txt

### Major Libraries:

tensorflow
fastapi
uvicorn
gtts
pyttsx3
numpy
