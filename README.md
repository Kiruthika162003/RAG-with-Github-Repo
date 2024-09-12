## Title
Example of RAG with a GitHub repo code

## Problem Statement
We aim to create a system that allows users to interact with their GitHub repository code through a conversational interface. This system should be able to answer questions about the code, provide insights, and help users understand their codebase better.

## Results Interpretation
The system successfully allows users to chat with their GitHub repository code. It can answer questions about the code, provide explanations, and offer insights into the codebase. This makes it easier for users to understand and work with their code.

## Steps Done
1. **Install Dependencies**
   - Installed necessary libraries such as `llama_index`, `llama-index-readers-github`, `llama-index-embeddings-langchain`, and `llama-index-llms-ollama`.

2. **Prevent Kernel Collapse**
   - Used `nest_asyncio` to prevent the Jupyter kernel from collapsing when downloading the GitHub repo content.

3. **Download Repo Code**
   - Initialized a GitHub client and used `GithubRepositoryReader` to load the repository data.

4. **Load Embedding Model**
   - Loaded the embedding model using `HuggingFaceEmbeddings` and `LangchainEmbedding`.

5. **Store Code into VectorStoreIndex**
   - Created a vector store and uploaded the indexed data using the loaded embedding model.

6. **Load LLM Model**
   - Selected the LLM model (`llama3`) and generated a query engine from the previously created vector store index.

7. **Chat with the Code**
   - Used the query engine to interact with the code and answer questions about the repository.

## Dataset
The dataset consists of the code from the GitHub repository `RAG-with-Github-Repo`. The repository contains Jupyter Notebook files (`.ipynb`) which are used to demonstrate the implementation of the RAG system. The data is loaded from the main branch of the repository and indexed for querying.

