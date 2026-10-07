RAG Chatbot using n8n, Google Gemini, OpenAI & Vector Store

An AI-powered Retrieval-Augmented Generation (RAG) chatbot built with n8n. The workflow allows users to upload their own documents, convert the content into embeddings, store the vectors, and ask questions based on the uploaded data.

The project combines n8n, Google Gemini, OpenAI, embeddings, a vector store, an AI Agent, and memory to create a practical document-question-answering system.

🚀 Project Overview

Traditional LLM applications may not know the information contained in a user's private documents. This project uses RAG (Retrieval-Augmented Generation) to retrieve relevant information from a vector store and provide context to the LLM before generating an answer.

Main Flow

Document Upload
      ↓
Data Loader
      ↓
Text Chunking
      ↓
Gemini Embeddings
      ↓
Vector Store
      ↓
User Question
      ↓
AI Agent
      ↓
Query Vector Store
      ↓
OpenAI Model
      ↓
Answer

🎯 Features

📄 Upload PDF, DOC, or text-based documents

✂️ Split documents into smaller chunks

🧠 Generate embeddings using Google Gemini

🗄️ Store document embeddings in a vector store

💬 Accept user questions through a chat interface

🔎 Retrieve relevant information from stored documents

🤖 Generate answers using an LLM

🧠 Maintain conversation context using simple memory

⚙️ Automate the complete RAG pipeline using n8n

🏗️ Workflow Architecture

1. Load Data Flow

The first part of the workflow prepares the user's documents for retrieval.

Upload File → Data Loader → Gemini Embeddings → Vector Store

Upload File: Accepts PDF, DOC, or text documents.

Data Loader: Loads the document and prepares its content.

Chunking: Splits large documents into smaller text chunks.

Gemini Embeddings: Converts text chunks into numerical vector representations.

Vector Store: Stores the vectors so that relevant information can be searched later.

2. Retriever Flow

The second part handles user questions.

Chat Message → AI Agent → Query Data Tool → Vector Store

The AI Agent receives the user's question and uses the query tool to search the vector store for relevant document information.

The retrieved context is then provided to the LLM, which generates the final answer.

🧩 Technologies Used

Technology

Purpose

n8n

Workflow automation and orchestration

RAG

Retrieval-Augmented Generation

Google Gemini

Text embeddings

OpenAI

LLM-based answer generation

Vector Store

Stores and retrieves document embeddings

AI Agent

Handles user queries and tool usage

Simple Memory

Maintains conversation context

🔄 How RAG Works in This Project

User uploads a document.

The document is loaded into the workflow.

The content is split into smaller chunks.

Each chunk is converted into an embedding.

The embeddings are stored in a vector database/vector store.

User asks a question.

The AI Agent determines that it needs information from the document.

The query tool searches the vector store for relevant chunks.

Relevant context is sent to the LLM.

The LLM generates an answer using the retrieved information.

This approach helps the chatbot answer questions using the user's own data rather than relying only on the model's pre-trained knowledge.

🖼️ Workflow Preview

Add the project animation/screenshot to your repository, for example:

assets/rag-chatbot-workflow.gif

Then display it in this README:

![RAG Chatbot Workflow](assets/rag-chatbot-workflow.gif)

⚙️ Setup

Prerequisites

Before running the workflow, you need:

An n8n instance (cloud or self-hosted)

Google Gemini API credentials

OpenAI API credentials

A supported vector store

Access to the required n8n AI/LangChain nodes

Basic Setup

Create or open an n8n workflow.

Configure the document upload/data loading section.

Configure the text splitter/chunking step.

Add Google Gemini embeddings.

Connect the embeddings to your vector store.

Configure the AI Agent.

Connect the OpenAI model.

Configure the vector-store retrieval tool.

Add memory if conversation history is required.

Test the workflow with a sample document and questions.

🔐 Security Considerations

When working with customer or private documents:

Never expose API keys in workflow data or public repositories.

Use n8n credentials/environment variables for secrets.

Avoid sending unnecessary sensitive information to an external LLM.

Apply appropriate access controls to the vector store.

Validate uploaded files and input data.

Follow applicable data-protection and privacy requirements.

🛠️ Error Handling & Production Improvements

For a production-ready version, I would add:

API rate-limit handling

Retry mechanisms

Error workflows in n8n

Input and output validation

File-type and file-size validation

Logging and monitoring

Authentication and authorization

Duplicate-document detection

Metadata filtering

Chunking optimization

Vector-store cleanup/versioning

Structured LLM output where required

💡 Possible Use Cases

This architecture can be adapted for:

📚 Document Q&A chatbot

🏢 Company knowledge-base assistant

📑 HR policy chatbot

🎓 Educational document assistant

⚖️ Legal document search assistant

🧾 Invoice/document analysis

🛠️ Technical documentation assistant

📖 Research-paper assistant

💼 Customer-support knowledge assistant

📌 Example

User:

What is the company's leave policy?

Workflow:

User Question
     ↓
AI Agent
     ↓
Vector Store Search
     ↓
Relevant Document Chunks
     ↓
OpenAI Model
     ↓
Answer based on company document

📈 Future Improvements

Add a web-based chat UI

Add authentication for users

Support multiple document types

Add metadata-based filtering

Add conversation history

Add citations/source references in answers

Add document management and deletion

Add evaluation of RAG accuracy

Add monitoring and analytics

Deploy the workflow using a production n8n instance

👨‍💻 Project Learning

Through this project, I gained practical understanding of:

RAG architecture

LLM integration

Embeddings

Vector stores

AI Agents

Prompt engineering

Document chunking

Semantic search

n8n workflow automation

Memory in AI applications

Connecting multiple AI services

⭐ Conclusion

This project demonstrates how n8n can be used to build an end-to-end RAG chatbot without writing the entire application from scratch.

The combination of document processing + embeddings + vector search + AI Agent + LLM makes it possible to build useful AI assistants that can work with custom business or personal data.

Tech Stack

n8n · RAG · Google Gemini · OpenAI · Vector Store · AI Agent · LLM · Generative AI · Automation

📬 Feedback

I’m continuously learning and improving my AI Automation and Generative AI projects.

Suggestions, feedback, and ideas for improving this RAG workflow are always welcome.
