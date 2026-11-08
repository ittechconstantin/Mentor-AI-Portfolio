# Five-Minute Technical Demo — IT Career Mentor

[← Back to the portfolio](../README.md)

This is a concise presentation script for recruiters, hiring managers and junior developer interviews. It refers to the **locally running application**; there is no publicly hosted live demo.

## 0:00–0:40 — Introduce the problem and project

> “I built IT Career Mentor as my final Python and Agentic AI course project. It helps people exploring IT careers find useful guidance through structured content, semantic search and an AI mentor. The goal was to integrate a real backend, persistent data storage, retrieval and an AI interface — not just call an LLM in isolation.”

## 0:40–1:30 — Career Guides

- Open **Career Guides** in Streamlit.
- Show the eight starter guides and filter to the *Interviews* category.
- Open a guide and explain that guide records are stored in MySQL.

**Explain:** “The content is structured and persistent. The frontend retrieves data through FastAPI rather than talking directly to the database.”

## 1:30–2:20 — Semantic Search

- Open **Semantic Search**.
- Enter: `How should I prepare for my first Python developer interview?`
- Display the returned guide titles and distances.

**Explain:** “The text is converted to semantic vectors using OpenAI embeddings, then ChromaDB finds the closest documents. The distance is a retrieval measure, not a confidence score.”

## 2:20–3:20 — AI Mentor and sources

- Open **AI Mentor**.
- Ask: `How should I prepare for my first junior Python interview?`
- Show the response and expand the **Sources** section.
- Ask a follow-up: `What should I demonstrate from my GitHub portfolio?`

**Explain:** “The LangChain agent can retrieve guide content before answering. The retrieved text is accessible so I can inspect which sources informed the answer. The conversation is maintained in the active Streamlit session.”

## 3:20–4:15 — Add and remove a guide

- Open **Add a Guide**.
- Enter a unique temporary title such as `Preparing for a Pair Programming Interview`.
- Add a short useful text of at least 50 characters.
- Confirm it appears in **Career Guides** and can be retrieved.
- Delete the temporary guide.

**Explain:** “I update the persistent record and the search index when content changes. One improvement for a production system would be stronger coordination if one of those updates fails.”

## 4:15–5:00 — Backend architecture and lessons learned

- Briefly show the [architecture diagram](../assets/architecture.svg).
- Open FastAPI Swagger locally (`http://127.0.0.1:8005/docs`) to show the exposed API routes.
- Explain the main trade-offs: in-memory vector index, local environment, no public deployment and no complete automated tests yet.

**Close with:** “This project strengthened my understanding of Python backend development, SQL databases, API integration, vector retrieval and debugging across a multi-component application. I am now looking for a junior Python, backend or automation role where I can keep learning and contribute to real software systems.”

## Common technical interview questions

**Why FastAPI and Streamlit?**  
FastAPI keeps backend concerns and validation separate; Streamlit provides a fast Python-based UI for a demonstration application.

**Why RAG instead of directly asking an LLM?**  
RAG lets the application use a known set of career guides as retrieval context and show the material it used.

**What is the difference between MySQL and ChromaDB here?**  
MySQL stores durable guide data. ChromaDB stores searchable embeddings for semantic similarity.

**What happens when you restart the app?**  
MySQL guides remain. The in-memory vector index is rebuilt and may trigger fresh embedding requests.

**Does RAG guarantee a correct answer?**  
No. It offers relevant context and source visibility, but still needs quality checks and evaluation.

**Is the app deployed for external users?**  
No. It is a locally tested course project; future work would be needed for secure production hosting.

[← Back to the portfolio](../README.md)
