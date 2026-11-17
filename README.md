# Resume and Application Toolkit

A collection of markdown runbooks, scripts, and other tools integrated with Supabase to produce output composed by the LLM but written by the user. Instead of slopped resumes, real information is chosen by relevance to the task at hand. Designed for maximum user control over output with minimum cost in both tokens and subscriptions.

- [Install](docs/install.md)
- [Guidance](docs/guidance.md)

## Internal Resume Tools

Resume information is written by hand and stored in Supabase: work experience, education, strengths, and pitches.

- **Data fill** by ingesting an existing resume
- **Custom resume** generated for a company and job description
- **Generic resume** generated without a job description
- **Custom Cover letter** generated for a company and job description
- **STAR review** checks pitches, employment, growth, and hardships for STAR adherence and suggests fixes
- **Fuzzy skill search** finds explicit, tangential, and related skills, and presents the best information relevant to the job post, with skill years grouped (e.g. "AWS (2) + Other cloud services (4)")

## Internal Application Tools

Using resume information in the database, apply to and track job applications.

- Find the top recent job posts matching job preferences
- Fill out applications with pre-specified responses only
- Track applications and responses
- Triage email with draft replies, file no-action mail, and log application responses
- Transcribe calls with speaker labels, from Fathom or local recordings (Windows, Mac, Phone)
- Generate embedded, low-token searchable transcripts, searched by meaning or keyword
- Record and validate abuses

## AI Techniques

- **Embeddings** generated locally (fastembed, BAAI/bge-base-en-v1.5 768-dim) and in Supabase Edge Functions (gte-small 384-dim), with no paid embedding API
- **Vector search** with pgvector, cosine similarity, and HNSW indexes
- **Hybrid search (RAG retrieval)** fusing semantic and Postgres full-text keyword results with reciprocal rank fusion (RRF)
- **Chunking** of transcripts by speaker turn, sentence, and silence gaps, with overlapping windows and token limits tuned against retrieval tests
- **Asymmetric retrieval** using query instruction prefixes
- **Speech-to-text** with faster-whisper and speaker diarization (pyannote), with Whisper hallucination filtering
- **Semantic skill matching** with similarity thresholds and abstract skill groups
- **Agentic workflows** as markdown runbooks and Claude skills, with MCP tool integrations (Supabase, Gmail, Google Calendar, browser automation)

## Personal Tools

- Todo list
- Interview Prep
