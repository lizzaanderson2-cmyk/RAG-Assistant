# Punjab Board Approved Publications – AI Assistant



![n8n](https://img.shields.io/badge/n8n-Workflow-blue)
![Supabase](https://img.shields.io/badge/Supabase-VectorStore-green)
![Google Gemini](https://img.shields.io/badge/Google-Gemini-orange)



Overview

This project is an AI-powered chatbot designed for private schools in Punjab to help them identify Punjab Board approved textbooks and publications. It uses a Retrieval-Augmented Generation (RAG) workflow built with n8n, Supabase Vector Store, and Google Gemini to answer questions accurately, with source citations.

Problem Solved: Private schools often struggle to identify which publications are officially approved by the Punjab Board. This AI assistant provides quick, reliable, and safe answers.


---

Features

Accurate Answers: Only retrieves information from official Punjab Board approved documents.

Source Citation: Every response shows the document name and page number.

Interactive Chatbot: Users can type questions naturally in the n8n chat interface.

Memory Support: Maintains context during a session using Postgres Chat Memory.

Safety Guardrails: Refuses to answer unrelated or general knowledge questions.



---

Architecture

User Chat Input
       ↓
Chat Trigger (n8n)
       ↓
AI Agent Node
       ↓
Google Gemini Chat Model
       ↓
Supabase Vector Store → Embeddings & Document Retrieval
       ↓
Postgres Chat Memory (optional)
       ↓
AI Agent Output → Chat Response (with Source)


---

Tools & Technologies

Tool / Technology Purpose

n8n Workflow automation and chatbot integration
Supabase Vector Store Stores embeddings for document retrieval
Google Gemini LLM for generating answers
Postgres Memory Maintains conversation context
Google Drive Source of official Punjab Board documents



---

System Prompt / AI Guardrails

This is the System Message used in the AI Agent:

You are an AI assistant designed for private schools in Punjab.

Your task is to answer questions ONLY using the provided
Punjab Board approved documents stored in the vector database.

Always include the document name or source from which the answer
is retrieved. If page information is available, include it in
the following format:
Source: Document Name (Page Number)

If the information is not found in the documents, respond with:
"This information is not available in Punjab Board approved documents."

Do not answer general knowledge questions or questions outside
the scope of Punjab Board approved publications.


---

Example Usage

User Question:

> “Which books are allowed for Maths Grade 5?”



AI Assistant Response:

For Grade 5 Maths, the following books are allowed:

- Paramount Books:
  - Journey Through Maths Student Book 5 (Textbook)
  - New Mathematics Connection Textbook 5 (Textbook)

- Pioneer Books:
  - Pioneer Mathematics (Textbook)

Source: Punjab Board Approved Publications List (Page 36)

User Question:

> “Who is Babar Azam?”



AI Assistant Response:

This information is not available in Punjab Board approved documents.


---

How to Run

1. Ensure n8n is running locally or on a server.


2. Upload Punjab Board approved documents to Supabase Vector Store.


3. Start the AI Agent workflow with the System Prompt defined above.


4. Open the Chat Trigger URL and start typing queries.




---

Demo Video

Watch the AI assistant in action: Demo Video

(Replace with your uploaded video link or GitHub-hosted video file)


---

Future Improvements

WhatsApp integration for school admins.

Multi-language support (Urdu & English).

Automatic document updates and embedding refresh.

Analytics dashboard for most asked questions.



---

Key Takeaways

A practical RAG AI solution solving a real-world problem.

Source citation and guardrails prevent hallucinations.

Fully portfolio-ready and interview-friendly.



---
Author

Sidra Saleem
