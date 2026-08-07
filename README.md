
# 🤖 Claude API



**A comprehensive, hands-on exploration of Anthropic's Claude API**  
*From basic requests to production-grade RAG pipelines — implemented in Python and Jupyter Notebooks*


[![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Anthropic](https://img.shields.io/badge/Anthropic-Claude%20API-D4A017?style=for-the-badge)](https://www.anthropic.com/)
[![AWS](https://img.shields.io/badge/AWS-Bedrock-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://aws.amazon.com/bedrock/)

---
 
## 📌 Overview
 
This repository is a **structured, self-directed deep-dive into the Anthropic Claude API**, covering the full spectrum of LLM engineering — from sending a first API request to building retrieval-augmented generation (RAG) pipelines with vector databases, BM25 keyword search, and hybrid retrieval strategies.
 
Each concept is implemented in an **isolated, well-documented Jupyter Notebook**, making the learning path easy to follow, reproduce, and extend. The project also includes a **CLI application**, an **app starter template**, and **AWS Bedrock integration** examples, demonstrating production deployment awareness beyond the Anthropic SDK alone.
 
> This repo demonstrates practical, up-to-date knowledge of LLM API integration, prompt engineering, tool use, retrieval systems, multimodal input, and cost-optimisation techniques — all implemented from scratch in Python.
 
---
 
## 🛠️ Skills & Technologies Demonstrated
 
| Category | Skills |
|---|---|
| **LLM APIs** | Anthropic Claude API, AWS Bedrock |
| **Python** | Jupyter Notebooks, scripting, CLI development |
| **Prompt Engineering** | System prompts, temperature control, prompt evals, advanced prompting |
| **Tool Use / Function Calling** | Tools, streaming tools, text editor tool, web search |
| **Retrieval-Augmented Generation** | Chunking strategies, embeddings, vector databases, BM25, hybrid search |
| **Multimodal** | Image inputs, citations, code execution |
| **Production Concerns** | Streaming, prompt caching, cost optimisation, extended thinking |
| **Cloud** | AWS Bedrock (Claude via managed cloud endpoint) |
| **App Development** | CLI project, application starter scaffold |
 
 
## 📂 Repository Structure
 
```
Claude-API/
│
├── 📓 001–020_*.ipynb        # Core learning notebooks (see table below)
│
├── 📁 AWS-Bedrock/           # Claude via Amazon Bedrock (cloud deployment)
├── 📁 app_starter/           # Starter template for Claude-powered applications
├── 📁 cli_project/           # Command-line interface built on the Claude API
├── 📁 images/                # Supporting images used across notebooks
│
├── 📄 questions-answers.md   # Sample Q&A document (used in RAG notebooks)
├── 📄 report.md              # Sample report document (used in search/citation notebooks)
├── 📄 streaming.csv          # Sample CSV data (used in streaming notebooks)
├── 📄 earth.pdf              # Sample PDF (used in document-processing notebooks)
└── 📄 VoyageAI_API_Key_Directions.pdf  # Setup guide for Voyage AI embeddings
```
 
---
 
## 📓 Notebook Map
 
The notebooks are numbered and meant to be explored in order, building from API fundamentals to advanced retrieval and multimodal techniques.
 
### 🔵 Foundations
 
| # | Notebook | What you'll learn |
|---|---|---|
| 001 | `001_requests.ipynb` | Authenticating and making your first Claude API call |
| 002 | `002_system_prompt.ipynb` | Shaping model behaviour with system prompts |
| 003 | `003_temperature.ipynb` | Controlling creativity and determinism via temperature |
| 004 | `004_streaming.ipynb` | Streaming responses token-by-token for real-time output |
 
### 🟡 Prompt Engineering & Evaluation
 
| # | Notebook | What you'll learn |
|---|---|---|
| 005 | `005_prompt_evals.ipynb` | Testing and comparing prompt quality systematically |
| 006 | `006_prompting.ipynb` | Advanced prompting patterns and best practices |
 
### 🟠 Tool Use & Agentic Capabilities
 
| # | Notebook | What you'll learn |
|---|---|---|
| 007 | `007_tools.ipynb` | Defining and calling tools (function calling) |
| 008 | `008_tools_streaming.ipynb` | Streaming responses when tools are in use |
| 009 | `009_text_editor_tool.ipynb` | Using Claude's built-in text editor tool |
| 010 | `010_web_search.ipynb` | Integrating the web search tool for live information retrieval |
 
### 🟣 Retrieval-Augmented Generation (RAG)
 
| # | Notebook | What you'll learn |
|---|---|---|
| 011 | `011_chunking.ipynb` | Document chunking strategies for effective retrieval |
| 012 | `012_embeddings.ipynb` | Generating semantic embeddings from text |
| 013 | `013_vectordb.ipynb` | Storing and querying embeddings in a vector database |
| 014 | `014_bm25.ipynb` | Keyword-based retrieval with BM25 |
| 015 | `015_hybrid.ipynb` | Hybrid search: combining BM25 + semantic embeddings |
 
### 🔴 Advanced Features
 
| # | Notebook | What you'll learn |
|---|---|---|
| 016 | `016_thinking.ipynb` | Extended thinking / chain-of-thought reasoning |
| 017 | `017_images.ipynb` | Sending images as multimodal input |
| 018 | `018_citations_complete.ipynb` | Grounded responses with document citations |
| 019 | `019_caching.ipynb` | Prompt caching for latency and cost reduction |
| 020 | `020_code_execution.ipynb` | Using Claude's code execution tool |
 
---
 
## ☁️ AWS Bedrock Integration
 
The `AWS-Bedrock/` folder contains examples of accessing Claude models through **Amazon Bedrock** — Anthropic's enterprise cloud partner. This demonstrates the ability to work with Claude in AWS-managed infrastructure, relevant for production environments that require VPC isolation, IAM-based auth, or existing AWS toolchains.
 
---
 
## 🚀 Getting Started
 
### Prerequisites
- Python 3.9+
- An [Anthropic API key](https://console.anthropic.com/) (required for all notebooks)
- A [Voyage AI API key](https://www.voyageai.com/) (required for embedding notebooks `012`–`015`)
- AWS credentials (optional — required for `AWS-Bedrock/` examples only)
### Installation
 
```bash
# 1. Clone the repository
git clone https://github.com/AndreasPr/Claude-API.git
cd Claude-API
 
# 2. (Recommended) Create a virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
 
# 3. Install dependencies
pip install anthropic python-dotenv voyageai jupyter
# Install additional packages as prompted within individual notebooks
 
# 4. Add your API key
cp .env.example .env   # or create .env manually
```
 
In your `.env` file:
```env
ANTHROPIC_API_KEY=your-anthropic-api-key-here
VOYAGE_API_KEY=your-voyage-api-key-here   # for embeddings notebooks
```
 
> ⚠️ **Security note:** A `.env` file is currently tracked in this repository. Ensure it does not contain live API keys before sharing or making the repo public.
 
### Running Notebooks
 
```bash
jupyter notebook
```
 
Open any numbered notebook and run cells from top to bottom. Start with `001_requests.ipynb` if you're new to the Claude API.
 
---
 
## 🎯 Purpose & Context
 
This project was built to develop deep, practical familiarity with the Claude API — going beyond documentation to implement every major feature from scratch. It is shared publicly as:
 
1. **A personal reference** for patterns and techniques I use in LLM-powered projects.
2. **A portfolio piece** demonstrating hands-on experience with the Anthropic ecosystem, RAG architecture, and modern Python LLM tooling.
---
 