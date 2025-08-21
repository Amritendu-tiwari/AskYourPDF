📘 AskYourPDF

A Streamlit-based AI assistant that lets you upload single or multiple PDFs and chat to get concise, context-grounded answers. Built with Retrieval-Augmented Generation (RAG) and history awareness to handle follow-up questions accurately.

Ideal for:
📄 Research papers | 📑 Manuals | 📜 Policies | 📕 Textbooks | 📊 Reports | 📑 Contracts

🚀 Features

📂 Multi-file PDF upload & processing

🔎 Semantic chunking (5,000 chars, 500 overlap) with embeddings for precise retrieval

⚡ Local vector index for fast, on-device search

🧠 History-aware retriever reformulates follow-ups into standalone questions

📝 Concise answers (limited to 3 sentences for clarity)

❌ Honest fallback → says “don’t know” when context is insufficient

💬 Session-based chat with unique session IDs & in-memory history

🏗️ Architecture

PDF Parsing → PyPDF Loader

Chunking → RecursiveCharacterTextSplitter

Embeddings → HuggingFace (all-MiniLM-L6-v2)

Vector Storage → ChromaDB

RAG Pipeline → “stuff” chain passing retrieved context into LLM prompt

Frontend → Streamlit UI (with multi-file uploader, session handling, chat display)

📂 UI Flow

Enter API Key (runtime input or .env)

Enter / keep Session ID

Upload PDF(s)

Ask questions → get concise answers + chat history inline

⚙️ Installation
# Clone the repo
git clone https://github.com/Amritendu-tiwari/AskYourPDF.git
cd AskYourPDF

# Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows

# Install dependencies
pip install -r requirements.txt

▶️ Usage
streamlit run app.py


Enter your API key (e.g., Hugging Face / OpenAI).

Upload one or multiple PDFs.

Start chatting with your documents!

📊 Benefits

✅ Rapid, reliable answers sourced directly from your PDFs
✅ Saves hours of manual scanning/searching
✅ Lightweight → runs locally, ideal for personal workflows & internal demos
✅ Transparent → visible chat history & context grounding

🧭 Design Principles

Reliability → grounded in retrieval

Brevity → strict answer-length prompt

Transparency → shows context + session history

🔮 Future Enhancements

 Support for hybrid search (BM25 + embeddings)

 Export chat history as PDF/Markdown

 Integrate with cloud storage (Google Drive, OneDrive)

 Fine-tune for domain-specific datasets

📸 Demo Screenshot (optional)

(Add here after running a session → streamlit run app.py and take a screenshot of the chat UI)

🤝 Contributing

Pull requests are welcome! Please open an issue to discuss before submitting changes.
