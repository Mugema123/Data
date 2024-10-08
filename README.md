# PDF Chat Streamlit App
This Streamlit app allows users to chat with multiple PDF documents using Retrieval-Augmented Generation (RAG) powered by OpenAI's language model and embeddings.

## Features

**Upload multiple PDF documents**

**Extract text from PDFs**

**Create text chunks and embeddings**

**Implement Retrieval-Augmented Generation (RAG) for enhanced question-answering**

**Use OpenAI's language model for generating responses**

**Interactive chat interface**

## Technologies Used

**Python:** The primary programming language used for the application.

**Streamlit:** For creating the web application interface.

**LangChain:** Utilized for implementing the RAG pipeline, including text splitting, embeddings, and creating conversational chains.

**Retrieval-Augmented Generation (RAG):** The core technique used to enhance the language model's responses with relevant information retrieved from the uploaded documents.

**OpenAI:** Leveraged for its powerful language models and embeddings in the RAG process.

**PyPDF2:** Used for extracting text from PDF documents.

**FAISS (Facebook AI Similarity Search):** Employed for efficient similarity search and clustering of dense vectors, crucial for the retrieval part of RAG.

**dotenv:** For loading environment variables.

**HuggingFace Transformers:** Although commented out in the current version, the code includes an option to use HuggingFace's instruction embeddings.


## How RAG Works in This Project

**Document Ingestion:** PDFs are uploaded and their text is extracted.

**Text Chunking:** The extracted text is split into manageable chunks.

**Embedding Creation:** Each chunk is converted into a vector embedding using OpenAI's embedding model.

**Vector Storage:** Embeddings are stored in a FAISS vector store for efficient retrieval.

**Query Processing:** When a user asks a question, it's also converted to an embedding.

**Retrieval:** The most relevant text chunks are retrieved based on similarity to the query embedding.

**Generation:** The retrieved information and the original query are sent to the language model to generate a contextualized response.

## Installation

**Clone this repository:** git clone https://github.com/your-username/pdf-chat-streamlit.git
cd pdf-chat-streamlit

**Install the required packages:** pip install -r requirements.txt

**RetSet up your OpenAI API key:** Create a .env file in the project root and add your OpenAI API

## Usage

**Run the Streamlit app:** streamlit run app.py

**Open your web browser and go to:** http://localhost:8501

**Upload PDF documents using the sidebar.**

**Click "Process":** To extract text, create embeddings, and set up the RAG pipeline

**Start chatting with your documents using natural language queries!**

## Contributing

*Contributions are welcome! Please feel free to submit a Pull Request.*