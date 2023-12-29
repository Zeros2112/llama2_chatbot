# Chat with CSV using Llama2 🦙🦜
## Overview
This application allows users to interact with a CSV (Comma-Separated Values) file using the Llama2 conversational model. It leverages Streamlit for the user interface, Hugging Face Transformers for language modeling, and FAISS for efficient vector search.

## Features
* CSV Upload: Users can upload a CSV file containing data that they want to interact with.

* Conversational Chat: The application supports a conversational chat interface where users can ask questions about the uploaded CSV data.

* History Tracking: The application keeps track of the chat history, providing a conversational context for each query.

* User and System Messages: Messages are displayed in a chat-like format with user messages and system-generated responses.

## Dependencies
Make sure you have the following dependencies installed to run the application:

* Python 3.x
* Streamlit
* langchain
* Hugging Face Transformers
* FAISS
* sentence-transformers
* tempfile
Install the dependencies using the following command:

```
pip install streamlit langchain sentence-transformers faiss-cpu tempfile
```

## Usage
1. Clone the repository:

```
git clone Zeros2112/llama2_chatbot
```

2. Navigate to the project directory:

```
cd csv_chatbot
```

3. Run the Streamlit app:

```
streamlit run app.py
```

Open your web browser and go to http://localhost:8501 to interact with the application.

## Configuration
* `DB_FAISS_PATH`: Path to the FAISS vector store. Change this if you want to store the vectors in a different location.

* `model`: Specify the Llama2 model file (e.g., "llama-2-7b-chat.ggmlv3.q8_0.bin") and other model parameters in the load_llm() function.

* `model_name`: Specify the Hugging Face model for embeddings (e.g., 'sentence-transformers/all-MiniLM-L6-v2').


