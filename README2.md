# Medical Document QA Bot

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

