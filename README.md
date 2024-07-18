# ASK QUESTION FROM THE DOCUMENT

This repository contains a Streamlit application that allows users to ask questions based on the content of PDF documents. The application leverages the capabilities of various libraries, including LangChain, FAISS, PyPDF2, and Google's Generative AI for embeddings.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)


## Features

- **Document Ingestion**: Load PDF documents from a specified directory.
- **Text Splitting**: Split documents into manageable chunks for processing.
- **Embedding Generation**: Create embeddings for document chunks using Google's Generative AI.
- **Vector Store Creation**: Store embeddings in a FAISS vector store.
- **Question Answering**: Retrieve relevant document chunks and answer questions based on the context.

## Installation

### Prerequisites

- Python 13.2 
- [pip](https://pip.pypa.io/en/stable/installation/)

### Steps

1. **Clone the repository**
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```

2. **Activate the virtual environment**
    ```bash
    source venv/bin/activate  # On Windows use `venv\\Scripts\\activate`
    ```

3. **Install dependencies**
    ```bash
    pip install -r rq.txt
    ```

4. **Set up environment variables**
    - The `.env` file is already present in the project.
    - Update the `.env` file with your own API keys:
    ```env
    GROQ_API_KEY=your_groq_api_key
    GOOGLE_API_KEY=your_google_api_key
    ```
To get Your Groq API Key: https://console.groq.com/keys 
To get Your Google API Key: https://aistudio.google.com/app/apikey

## Usage

1. **Run the Streamlit application**
    ```bash
    streamlit run app.py
    ```

2. **Upload PDF documents if want to test with other Content PDF **
   - which is PDF documents is already in the `./data_corpus` directory.

3. **Generate Document Embeddings**
   - Click the "Create Documents Embedding" button to generate embeddings for the documents.

4. **Ask Questions**
   - Enter your question in the text input field and press Enter.
   - NOTE: can also ask from the sample questions as well 

## Project Structure
 ├── app.py # Main application file
 ├── data_corpus/ # Directory to store PDF documents
 ├── .env # Environment variables value which are the API keys
 ├── rq.txt # List of dependencies basically the requirement 
 └── README.md # This file



## Dependencies

The project uses the following libraries:

- [faiss-cpu](https://github.com/facebookresearch/faiss)
- [groq](https://github.com/groq)
- [langchain-groq](https://github.com/langchain-ai/langchain-groq)
- [PyPDF2](https://github.com/py-pdf/PyPDF2)
- [langchain_google_genai](https://github.com/langchain-ai/langchain-google-genai)
- [langchain](https://github.com/langchain-ai/langchain)
- [streamlit](https://github.com/streamlit/streamlit)
- [langchain_community](https://github.com/langchain-ai/langchain-community)
- [python-dotenv](https://github.com/theskumar/python-dotenv)
- [pypdf](https://github.com/py-pdf/pypdf)

