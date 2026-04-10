# 🚀 Vectorless RAG QA Chatbot

An advanced implementation of **Retrieval-Augmented Generation (RAG)** that replaces traditional vector embeddings and flat chunking with structural document reasoning using **PageIndex**.

## 🧠 What is Vectorless RAG?

Traditional RAG systems rely on mathematical "similarity" (cosine similarity of vectors). While effective for massive datasets, they often lose the context of document structure, leading to fragmented information and hallucinations.

**Vectorless RAG** takes a "Structure Before Search" approach:
- **Hierarchical Indexing:** Documents are parsed into a logical tree (Sections -> Subsections -> Paragraphs).
- **Reasoning-Based Retrieval:** Instead of vector math, an LLM "reasons" over the structural summaries to navigate the tree and find the exact context needed.
- **Perfect Context:** By retrieving logically complete sections, the generator has all the surrounding context required to produce accurate, cited answers.

## 🛠️ Tech Stack

- **[PageIndex](https://pageindex.ai):** Hierarchical indexing and reasoning engine.
- **[Groq](https://groq.com):** Ultra-fast inference for the LLM generator (Llama 3/3.1).
- **Python:** Core implementation environment.

## 📁 Project Structure

- `main.ipynb`: The primary walkthrough and implementation of the vectorless pipeline.
- `data/`: Contains the PDF sources (e.g., Generative AI Interview Preparation).
- `.env`: API keys and Document IDs (not tracked by Git).

## 🧪 What was Tested

1. **Complex Hierarchy Parsing:** Successfully indexed a 60+ page PDF with deep nesting.
2. **Structural Navigation:** Verified that the LLM could correctly identify specific sections (like "Transformer Architecture") without any embedding search.
3. **Multi-Step Reasoning:** Tested queries that required cross-referencing summaries to find granular details.
4. **End-to-End QA:** Validated the generation of cited answers using Groq's high-speed models.

---
Built with curiosity and a desire to go beyond the "embedding-first" RAG paradigm.
