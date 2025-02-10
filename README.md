# multi-pdf-reader-chatbot
# 📄 Multi-PDF Q&A App with RAG Search

This is a **Streamlit web application** that allows users to upload and query multiple PDF files using **Retrieval-Augmented Generation (RAG)**. The app extracts text from the PDFs, chunks the content, and uses OpenAI's GPT to provide relevant answers to user questions.

## 🌟 Features
- **Multiple PDF Uploads:** Upload multiple PDF documents for processing.
- **Text Extraction:** Extract plain text from all uploaded PDFs.
- **Chunking:** Split large documents into manageable text chunks for efficient retrieval.
- **RAG Search:** Retrieve the most relevant context from the uploaded PDFs using Sentence Transformers.
- **Answer Generation:** Generate accurate answers to user queries using OpenAI's GPT models.

---

## 🛠️ Setup Instructions

### 1. Clone the Repository
```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Create a Virtual Environment
```bash
python -m venv .venv
source .venv/bin/activate  # On MacOS/Linux
# OR
.venv\Scripts\activate    # On Windows
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Set Up the OpenAI API Key
- Create a `.env` file in the root directory:
  ```plaintext
  OPENAI_API_KEY="your_openai_api_key"
  ```
  - Replace `your_openai_api_key` with your actual OpenAI API key. You can generate or find your API key [here](https://platform.openai.com/account/api-keys).

### 5. Run the Application
```bash
streamlit run app.py
```

The app will launch in your default web browser.

---

## 📂 Project Structure
```
├── app.py                 # Main Streamlit application
├── pdf_reader.py          # Extracts text from PDFs
├── text_chunker.py        # Splits the extracted text into manageable chunks
├── rag_search.py          # Retrieves relevant chunks using RAG search
├── .env                   # Stores the OpenAI API key
├── requirements.txt       # Dependencies for the project
└── README.md              # Project documentation
```

---

## 🔧 How It Works
1. **PDF Upload:** Users can upload one or more PDF files via the Streamlit interface.
2. **Text Extraction:** Text is extracted using the `pdf_reader.py` module.
3. **Chunking:** The extracted text is split into chunks using the `text_chunker.py` module to enhance retrieval.
4. **RAG Search:** The `rag_search.py` module identifies the most relevant chunks using Sentence Transformers.
5. **Answer Generation:** OpenAI's GPT processes the relevant chunks to answer user queries.

---

## 🧰 Requirements
- Python 3.8 or higher
- Streamlit
- PyMuPDF (fitz)
- Sentence Transformers
- OpenAI API
- python-dotenv

### Installing Requirements
Use the following command to install dependencies:
```bash
pip install -r requirements.txt
```

---

## 🚀 Usage Guide
1. Launch the app with `streamlit run app.py`.
2. Upload one or more PDFs using the **file uploader**.
3. View a preview of the extracted content.
4. Enter a question in the text input field.
5. Get an AI-generated response based on the content of the uploaded documents.

---

## 🌐 Environment Variables
- `OPENAI_API_KEY`: The API key to interact with OpenAI's GPT.

Make sure to store it securely in the `.env` file.

---

## ✨ Future Enhancements

Add support for large PDFs using chunk-wise processing and external vector databases.

Explore integrating other RAG pipelines, such as FAISS or Pinecone for scalable retrieval.

Improve the chunking logic to handle structured data (tables, headers, etc.).

Combine image processing (maybe too hard).

Refine search/output quality.

Refer to relevant page numbers at the end as a “For more information, refer to:” thing.

---

## 👨‍💻 Author
Built by Mira Kapoor Wadehra (https://github.com/mirakw).
