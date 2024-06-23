# RAG-pipeline

# Project Overview
This project explores the capabilities of Pinecone VectorDB and implements a basic Retrieval-Augmented Generation (RAG) pipeline. The goal is to enhance the performance of a standard Question Answering (QA) model by leveraging relevant documents from a vector database to reduce hallucinations and improve accuracy.

# Dataset Selection
We selected a dataset based on information about Lady Gaga songs. A standard QA model often fails to accurately answer questions about Lady Gaga's songs, resulting in hallucinations. The correct answers are available within a set of documents that have been stored in the Pinecone VectorDB.

# RAG Pipeline Implementation
The RAG pipeline consists of the following steps:

Document Reading and Preprocessing: Read and preprocess the dataset documents.
Chunking Documents for Embedding Generation: Split documents into smaller chunks suitable for embedding.
Embedding Generation and Insertion into Pinecone VectorDB: Generate embeddings for document chunks and insert them into Pinecone VectorDB.
Retrieval of Relevant Documents: Retrieve relevant documents from Pinecone VectorDB based on input questions.
Generating Answers Using Retrieved Documents: Use a generative model to generate answers from the retrieved documents

# Anecdotal Assessment
Dataset and Rationale
The Lady Gaga songs dataset was chosen because it presents a challenge for standard QA models, which often produce hallucinated answers. This makes it an ideal candidate to test the effectiveness of the RAG pipeline.

# Examples
Here are some anecdotal examples where the RAG pipeline succeeded where a standard QA model failed:

Standard QA Model Failure: which lady gaga song contain the phrase That Arizona sky Burnin in your eyes ? 

Standard QA Answer: "The phrase "That Arizona sky, burnin\' in your eyes" is from the song "Born This Way" by Lady Gaga." (hallucinated answer)

RAG Pipeline Answer: "Always Remember Us This Way"

Standard QA Model Failure: when was the song Charlotte Nights by Lady Gaga released?

Standard QA Answer: "Charlotte Nights' by Lady Gaga was released on May 21, 2020, as part of her sixth studio album, *Chromatica*. The song is a collaboration with American singer-songwriter Charlotte Lawrence and is the thirteenth track on the album." ((hallucinated answer))

RAG Pipeline Answer: "The song "Charlotte Nights" by Lady Gaga is unreleased, so it doesn\'t have a release date."


# Retrieval System and Prompts
The retrieval system uses Pinecone VectorDB to fetch relevant document chunks. The prompts used in the RAG pipeline are designed to provide context from the retrieved documents to the generative model, enhancing its ability to produce accurate answers.

