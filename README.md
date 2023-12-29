# 1. Chat with CSV using Llama2 🦙🦜
## Overview
This application allows users to interact with a CSV (Comma-Separated Values) file using the Llama2 conversational model. It leverages Streamlit for the user interface, Hugging Face Transformers for language modeling, and FAISS for efficient vector search.

## Demo 
[Google drive](https://drive.google.com/drive/folders/1KoKM79kUXy_fIcAaqkSSsShk9ol8GBJa?usp=sharing)

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


<br/> 

# 2. Medical Document QA Bot

This project implements a simple yet powerful Medical Question-Answering (QA) bot using LangChain, Chainlit, and Hugging Face models. The bot is designed to answer medical-related queries based on a pre-trained language model and a Faiss vector store.

## Features

- **Question-Answering Chain:** Utilizes LangChain and Chainlit to create a dynamic question-answering chain that retrieves relevant information from a Faiss vector store.
- **Language Model (LLM):** Employs the CTransformers language model from Hugging Face for generating context-aware responses.
- **Vector Database:** Implements a Faiss vector store for efficient retrieval of relevant documents, enabling a more focused response to user queries.
- **Document Embeddings:** Leverages Hugging Face's Sentence Transformers for creating embeddings of medical documents, enabling semantic similarity-based retrieval.

## Setup

### Prerequisites

- Python 3.6+
- Dependencies: see `requirements.txt`

### Installation

1. **Clone the repository:**

   ```
   git clone https://github.com/yourusername/medical-qa-bot.git
   cd medical-qa-bot
   ```

2. Install dependencies:

   ```
   pip install -r requirements.txt
   ```

3. Create the Faiss vector database:

   ```
   python main.py
   ```

## Usage
1. Start the bot:

```
python main.py
```

2. Interact with the bot:

* Send medical queries to the bot.
* The bot will respond with relevant information based on the Faiss vector store.

## Project Structure
* `main.py`: Main entry point for the bot. Creates the Faiss vector store, initializes the question-answering chain, and defines interaction using Chainlit.
* `langchain`: Directory containing modules for LangChain functionalities (document loaders, embeddings, etc.).
* `chainlit`: Directory containing modules for the Chainlit framework.
* `data`: Directory containing sample PDF documents used to create the Faiss vector store.
* `vectorstore`: Directory where the Faiss vector store is saved.

## Advanced Configuration
* Customize Prompts: Modify the custom_prompt_template in main.py to tailor the bot's response template for specific user needs.
* Model Tuning: Explore options for fine-tuning the language model and embeddings to better suit your medical domain.

## Acknowledgments
* LangChain: https://github.com/chinganho/langchain
* Chainlit: https://github.com/chinganho/chainlit
* Hugging Face: https://huggingface.co/

## License
This project is licensed under the MIT License.

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.
