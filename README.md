# LLM Based Document Query Processing Engine

Developed an AI-driven semantic PDF retrieval system using PyPDF2, FAISS, and HuggingFace embeddings, incorporating vector-based text chunking and cosine-similarity search to enable concept-aware querying, outperforming traditional keyword methods.

## Features

- **PDF Loading and Text Extraction**: Utilizes `PyPDFLoader` to load and split text from PDF documents.
- **Text Splitting and Embedding**: Segments the extracted text into manageable chunks and embeds them using `OllamaEmbeddings` model.
- **Vector Database Management**: Uses `Chroma` to create and manage a vector database (`vector_db`) for efficient document retrieval.
- **Question Generation and Answering**: Generates alternative versions of user questions to enhance document retrieval using `MultiQueryRetriever` and an AI language model (`ChatOllama`).
- **Pipeline for Question Answering**: Sets up a processing pipeline (`chain`) that integrates document retrieval, question prompts, and answer extraction.
- **Clean-up**: Includes functionality to delete collections (`local-rag`) from the vector database after use.

## Requirements

- Python 3.6+
- LangChain library (install via `pip install langchain`)

## Installation

1. Clone the repository:

   ```
   git clone https://github.com/SSunilDV/PDF_InfoRetrieval..git
   cd your_repository
   ```

2. Install dependencies:

   ```
   pip install -r requirements.txt
   ```

3. Download necessary models or resources as specified in the code comments or documentation.

## Usage

1. Ensure you have a PDF file (`local_path`) ready for processing. Update `local_path` in the script if necessary.

2. Run the script (`pdf_retrieval.ipynb` or your preferred filename):

   ```
   python pdf_retrieval.py
   ```

3. Follow the prompts to interact with the system. Example:

   ```
   What are the 5 pillars of global cooperation?
   ```

4. View the generated answers based on the document retrieval and question answering pipeline.

- LangChain developers and contributors for their open-source contributions and support.

