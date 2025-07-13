# 🗣️ Kumaoni AI Voice Chatbot (LLM + RAG + TTS + STT)[In Progress]

This project is a culturally grounded AI assistant that understands and responds in the **Kumaoni language**. It supports both **text and voice interaction**, using a combination of **LLM fine-tuning**, **RAG (Retrieval-Augmented Generation)**, and **TTS/STT models** to enable real-time dialogue.

> 🎯 Designed to preserve regional language through conversational AI — powered entirely on open-source tools.

---

## 🌟 Features

- 🧠 **LLM-based response generation** using fine-tuned GPT-2 or Phi-2 with Kumaoni text corpus
- 📚 **RAG architecture**: retrieves relevant information from a FAISS vector store
- 🎙️ **Voice input support**: speech-to-text with Whisper
- 🔊 **Voice output**: real-time TTS replies using Coqui or Google TTS
- 🌐 **Bilingual interface**: supports Kumaoni, English, and Romanized Kumaoni input
- 💻 **Streamlit-based frontend** with voice/text input toggle
- 🔁 **Self-learning capability** planned for future

---

## 🛠 Tech Stack

| Component        | Tool/Framework          |
|------------------|--------------------------|
| Language Model   | GPT-2 / Phi-2 (LoRA fine-tuned) |
| Data Retrieval   | FAISS (Vector Store) + RAG |
| STT              | Whisper (open-source)   |
| TTS              | Coqui TTS / gTTS        |
| UI               | Streamlit               |
| Dataset          | Custom bilingual: English–Kumaoni–Romanized |
| Deployment       | Kaggle (training), Hugging Face / Streamlit Cloud (deployment) |

---

## 📂 Project Structure

kumaoni-voice-chatbot/

│

├── data/ # Bilingual dataset with audio

│ └── kumaoni_dataset.json # 2000+ entries (Unicode + Roman + Audio)

│

├── rag/ # RAG setup and FAISS integration

│ └── embed_store.py

│ └── retriever.py

│

├── llm/ # Fine-tuning scripts

│ └── train_lora.py

│ └── generate_response.py

│

├── tts_stt/ # Voice interface

│ └── whisper_stt.py

│ └── coqui_tts.py

│

├── app/ # Streamlit interface

│ └── main_app.py

│

├── requirements.txt

└── README.md


---

## 🚀 How to Run (once ready)

1. Clone the repo:
   ```bash
   git clone https://github.com/Sourabsb/kumaoni-voice-chatbot
   cd kumaoni-voice-chatbot
```
2. (Optional) Setup virtual environment:
```bash
python -m venv env
source env/bin/activate  # or `env\Scripts\activate` on Windows
```
3. Install dependencies:
```bash
pip install -r requirements.txt
```
4. Launch the app:
```bash
streamlit run app/main_app.py
```
# 📈 Status

✅ Dataset created: 2000+ bilingual entries with speaker gender and audio

🚧 Model training & integration in progress

🎯 Goal: Voice-based assistant demo by August 2025

## 🧠 Credits

Dataset built by Sourab Singh Bora

Inspired by real-world needs for regional AI access

Open-source tools: GPT-2, Whisper, Coqui, FAISS, Streamlit

## 🔗 License
This project is released under the MIT License.
