# RAG_from_scratch  


📄 Document Q&A Assistant
A Python & Gradio-based web app that allows users to upload documents (PDFs or TXT) and ask questions. The system retrieves relevant text from the uploaded documents and provides precise answers using embeddings and optional LLMs.



🚀 Features
Upload multiple PDFs or TXT files simultaneously.
Automatically extracts text from PDFs.
Chunks documents for efficient semantic search.
Computes embeddings using BAAI/bge-small-en-v1.5 model.
Retrieves top relevant sentences using cosine similarity.
Optional LLM-based QA for precise answers.
Each query is processed independently — no history is stored.
Web-based interface powered by Gradio.


📦 Installation
Clone the repository:
git clone https://github.com/yourusername/document-qna.git
cd document-qna
Install dependencies:
pip install -r requirements.txt
Set your OpenAI API key (optional, for LLM responses):
import os
os.environ["OPENAI_API_KEY"] = "your_openai_api_key_here"



📝 Usage
Run the Colab / Python script:
python app.py
Upload your documents (PDF/TXT) in the Gradio interface.
Ask your questions in the input box.
Receive:
🔎 Retrieved Text: Relevant text snippets.
🎯 Precise Answer (optional, if OpenAI API key is provided).
⚙ How It Works
Document Processing
PDFs are converted to text.
Documents are split into smaller chunks for semantic search.
Embeddings
Each chunk is embedded using BAAI/bge-small-en-v1.5.
Cosine similarity is used to retrieve top relevant chunks.
LLM QA (Optional)
Top chunks are passed to a lightweight OpenAI GPT model for precise answers.
Example: extract “resume owner’s name” instead of returning full paragraphs.
💡 Example
Question: What is the resume owner’s name?
Answer: SHANMUKHA NARAYANA S
Question: Where did they win first place?
Answer: 🥇 Winner (1st Place) – Hackathon at IIT Mandi



🛠 Tech Stack
Python 3.x
Gradio — Web interface
PyMuPDF / fitz — PDF parsing
Transformers — Tokenizer & model
NumPy — Cosine similarity & embeddings
LangChain (optional) — LLM for precise QA
OpenAI GPT-3.5-turbo (optional)



📁 Folder Structure
.
├── documents/          # Uploaded PDF/TXT files
├── database/           # JSON data store for chunks & embeddings
├── app.py              # Main Gradio + processing script
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation


⚠️ Notes
For LLM responses, OpenAI API key is required. Without it, only retrieved text is shown.
The system does not store queries or document history, ensuring privacy.
Designed for educational and small-scale usage. Not production-ready without proper backend.
