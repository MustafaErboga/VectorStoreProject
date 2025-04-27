# VectorStoreProject

VectorStoreProject is a search engine application built using LangChain. It allows for semantic search and context-aware question answering using a combination of OpenAI embeddings, Chroma as the vector store, and LangChain's powerful tools. This project demonstrates how to embed document content, store it in a vector database, and query it effectively.

## Features
- **Semantic Search**: Uses OpenAI's embeddings to represent documents and perform similarity search.
- **Context-Aware Question Answering**: Integrates retrieval-augmented generation (RAG) with GPT-3.5 turbo for context-driven responses.
- **Flexible Retrieval**: The ability to customize how many top results to retrieve and use them in the response.

## Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/VectorStoreProject.git
   cd VectorStoreProject
   ```

2. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Create a `.env` file and add your API keys:

   ```
   OPENAI_API_KEY=your_openai_api_key
   LANGCHAIN_API_KEY=your_langchain_api_key
   LANGCHAIN_TRACING_V2=true
   LANGCHAIN_PROJECT=VectorStoreProject
   ```

4. Run the project:

   ```bash
   python main.py
   ```

## How It Works

- The documents are embedded using OpenAI's `OpenAIEmbeddings` class.
- The embeddings are stored in Chroma’s vector store for efficient similarity search.
- When a question is asked, the retriever searches for the most relevant document(s) from the vector store.
- The question and the retrieved context are then passed to the GPT model to generate a context-aware answer.

## Usage Example

Once the setup is complete, you can run the following code to ask questions:

```python
response = rag_chain.invoke("tell me about cats")
print(response.content)
```

This will query the system with "tell me about cats" and generate an answer based on the provided documents.

## Contributions

Feel free to fork the repository, open issues, and submit pull requests. Contributions are always welcome!

---
🙌 Acknowledgements

This project is based on an example provided by LangChain.
