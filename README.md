# QnA with PDF & Text Documents using LangChain

A Streamlit-based chatbot that allows you to upload documents (PDF, DOCX, TXT) and ask questions about their content using OpenAI's GPT-4o and conversational retrieval chains.

## Features

- Upload and process PDF, DOCX, and TXT files
- Document chunking with recursive text splitting
- Vector embeddings using OpenAI's embedding model
- Semantic search with ChromaDB vector store
- Conversational memory for follow-up questions
- Interactive Streamlit UI

## Tech Stack

- **LLM**: OpenAI GPT-4o
- **Embeddings**: OpenAI text-embedding-ada-002
- **Vector Store**: ChromaDB
- **Framework**: LangChain
- **Frontend**: Streamlit

## Setup

### Prerequisites

- Python 3.11+
- OpenAI API key

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/nisha1365/QnA-with-PDF-LangChain.git
   cd QnA-with-PDF-LangChain
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate  # Windows
   source .venv/bin/activate  # macOS/Linux
   ```

3. Install dependencies:
   ```bash
   pip install streamlit langchain langchain-openai langchain-community langchain-text-splitters chromadb pypdf docx2txt
   ```

4. Create an `apikey.py` file with your OpenAI credentials:
   ```python
   OPENAI_API_KEY = "your-openai-api-key"
   OPENAI_API_BASE_URL = "https://api.openai.com/v1"
   ```

## Running the App

```bash
streamlit run chatdoc.py
```

## Usage

1. Upload a PDF, DOCX, or TXT file using the file uploader
2. Click **Add File** to process and embed the document
3. Type your question in the text input field
4. View the answer along with conversation history

## Project Structure

```
QnA_with_pdf_textdocs_langchain/
├── chatdoc.py          # Main Streamlit application
├── apikey.py           # API key configuration (not committed)
├── constitution.txt    # Sample document for testing
└── README.md
```

## Notes

- The OpenAI API key must have access to both the embeddings and chat completions endpoints.
- If using a project-scoped API key (`sk-proj-...`), ensure your network is within the allowed geography (US VPN may be required).
