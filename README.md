🚀 Agentic RAG with Pinecone — End-to-End Pipeline

This repository contains a modular workflow to build a production-ready Agentic RAG system using Pinecone, Amazon Bedrock, and vector database pipelines.
Each stage of the pipeline is implemented via a dedicated notebook, enabling a clear and scalable development flow.

📦 agentic-rag-pinecone/
├── 1_data_loading_pipeline.ipynb        # Load data, chunk, embed & upload vectors to Pinecone
├── 2_data_query_pipeline.ipynb          # Query Pinecone & generate a basic RAG response
├── 3_agentic_rag.ipynb                  # Agentic RAG — use tools & multi-step reasoning
└── 4_clean_up.ipynb                     # Delete resources & clean up Pinecone/AWS setup


📌 Project Overview

This project demonstrates how to build an Agentic Retrieval-Augmented Generation (RAG) workflow using Pinecone + AWS Bedrock.
It teaches how to:

✔ Load and process documents
✔ Create & query vector embeddings
✔ Implement multi-step Agentic RAG
✔ Clean up resources programmatically

The workflow is modular and scalable — ideal for experimentation, workshops, and production prototyping.

🔧 Installation
# Create environment
conda create -n rag_env python=3.10 -y
conda activate rag_env

# Install dependencies
pip install -r requirements.txt


💡 If requirements.txt is missing, install the libraries directly from the notebooks (pip install sections inside each notebook).

🔑 Environment Setup

Create a .env file with your credentials:

PINECONE_API_KEY=your_key_here
AWS_ACCESS_KEY=...
AWS_SECRET_KEY=...
AWS_REGION=...


Ensure these are not committed to Git. Add them to .gitignore.

📘 Notebook Workflow
🧩 1️⃣ Module — Data Loading

Notebook: 1_data_loading_pipeline.ipynb

Chunk & embed documents

Create Pinecone index

Upload vectors to database

🔍 2️⃣ Module — Data Query + RAG

Notebook: 2_data_query_pipeline.ipynb

Perform semantic search via Pinecone

Generate a basic RAG response

Interface with AWS Bedrock for LLM inference

🧠 3️⃣ Module — Agentic RAG

Notebook: 3_agentic_rag.ipynb
Implements agent-style reasoning & tool usage:

Tool selection and planning

Query re-ranking & retrieval enhancement

Multi-step reasoning based on context

🧹 4️⃣ Module — Clean Up

Notebook: 4_clean_up.ipynb

Delete Pinecone index

Release AWS resources

Ensure no unwanted cloud resources remain

📈 Future Enhancements

You can extend this project with:

📊 Evaluation metrics (nDCG, MRR, recall@k)

🔍 Hybrid search (text + metadata)

🧪 RAG evaluation benchmarks

🖥️ Streamlit or Gradio UI

🧠 Fine-tuned reasoning agents
