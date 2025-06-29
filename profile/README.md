# YumeSession

> Google Meet Live Meeting Assistant

![YumeSession Logo](https://github.com/YumeSession/.github/blob/main/yumesession.jpeg?raw=true)

---

## Project Overview

Meeting assistants like Fireflies.ai make it easy to transcribe and summarize meetings after they end. But what about during the meeting? There’s currently no effective solution that helps users stay fully engaged, process information, and make smart decisions in real time. Imagine someone is discussing Case A, then B, then C. By the time they reach C, many people have already forgotten the details of Case A, losing the opportunity to ask insightful questions or identify contradictions. This often results in delayed follow-ups and wasted meeting time.

Taking manual notes on the fly is cognitively demanding — it forces users to split their attention between listening, thinking, and writing. That’s where YumeSession, our open-source, MIT-licensed live meeting assistant, comes in.

YumeSession is designed for freelancers, students, and enterprise teams who attend frequent meetings and need real-time cognitive support. It consists of two components: a browser extension and a cross-platform desktop application.

- The browser extension captures live transcription data from Google Meet and streams it via WebSocket.
- The desktop application is built using Go (Wails Framework) and embeds Python for running local inference with Granite 3.3 8B, an open-source LLM.

### Key Features

Within the app, users can:
1. View live transcriptions and select segments to ask contextual questions like “What did X mean by Y?”
2. Get real-time meeting notes updated every 20 seconds using AI-generated summaries.
3. Chat with an AI assistant that references the current transcription and user-uploaded documents.
4. Use a PDF viewer where the assistant can cite and link to relevant pages from the uploaded documents.

### AI Backend

Our AI backend uses:
- **Bee-AI Framework:** for agentic RAG (Retrieval-Augmented Generation) to generate grounded responses.
- **Docling:** for fast and structured PDF data extraction.
- **Ollama:** for local LLM hosting with full user control and privacy.

### Workflow

1. User uploads relevant PDFs to build a meeting-specific knowledge base.
2. They create or open a workspace in the app.
3. They initiate live monitoring via Google Meet and the browser extension.
4. Transcriptions stream in and are chunked for real-time summarization every 20 seconds.
5. The user chats with the assistant, explores context, and navigates linked references instantly.

Unlike typical tools that operate post-meeting or require cloud-based processing, YumeSession is fully local, secure, and real-time — offering a uniquely interactive, private, and actionable AI-driven meeting experience.