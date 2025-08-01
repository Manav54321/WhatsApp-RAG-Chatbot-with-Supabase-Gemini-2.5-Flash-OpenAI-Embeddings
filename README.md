## WhatsApp RAG Chatbot with Supabase, Gemini 2.5 Flash & OpenAI Embeddings

### Overview

- This n8n template demonstrates how to build a WhatsApp-based AI chatbot using **document retrieval (RAG)**. It stores documents in **Supabase** with **OpenAI embeddings** and generates user-friendly answers using **Gemini 2.5 Flash LLM**.

Use cases: Customer support, FAQs, internal team knowledge assistants, or any scenario where you want real-time document-based answers on WhatsApp.

---

### How it works

* **Trigger:** A WhatsApp webhook starts the workflow when a new message arrives.
* **Message Check:** Determines if the message is a text query or a document upload.
* **Document Handling:** Retrieves file URL → converts binary to text → generates embeddings with OpenAI → stores in Supabase for future queries.
* **Query Handling:** Creates embeddings for the user query → retrieves relevant context from Supabase → sends context to Gemini 2.5 Flash for generating a response.
* **Reply:** The crafted answer is returned to the user on WhatsApp instantly.

---

### How to use

* Configure **WhatsApp Business API**, **Supabase**, and **OpenAI credentials** in n8n’s credentials manager.
* Upload documents through WhatsApp to populate the vector store.
* Ask questions on WhatsApp; the chatbot retrieves context and answers in real time.

---

### Requirements

* WhatsApp Business API (or Twilio sandbox)
* Supabase account (for vector storage)
* OpenAI API key (for embeddings)
* Gemini API access (for LLM responses)

---

### Need Help?

Ask me directly on [X (formerly Twitter)](https://x.com/manav170303) or email me at [titanfactz@gmail.com](mailto:titanfactz@gmail.com).

Let me know how this works for you — always open to feedback and improvements :)
