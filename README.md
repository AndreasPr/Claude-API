# Claude-API

A hands-on, notebook-by-notebook exploration of Anthropic's Claude API — built as a personal learning project to understand and demonstrate practical, production-relevant patterns for working with large language models.

This repository walks through the Claude API feature by feature, from a first basic request all the way to retrieval-augmented generation (RAG) techniques like embeddings, BM25, and hybrid search, plus integration with AWS Bedrock. It's intended as a portfolio piece showing applied LLM/API engineering skills.

## What's inside

The core of the repo is a sequence of numbered Jupyter notebooks, each focused on a single concept. They are designed to be read/run in order, building from fundamentals to more advanced techniques.

| Notebook | Topic |
|---|---|
| `001_requests.ipynb` | Making basic requests to the Claude API |
| `002_system_prompt.ipynb` | Using system prompts to steer model behavior |
| `003_temperature.ipynb` | Controlling output randomness with temperature |
| `004_streaming.ipynb` | Streaming responses token-by-token |
| `005_prompt_evals.ipynb` | Evaluating and testing prompts |
| `006_prompting.ipynb` | Prompt engineering techniques |
| `007_tools.ipynb` | Tool use / function calling |
| `008_tools_streaming.ipynb` | Combining tool use with streaming |
| `009_text_editor_tool.ipynb` | Using Claude's text editor tool |
| `010_web_search.ipynb` | Web search tool integration |
| `011_chunking.ipynb` | Chunking strategies for document processing |
| `012_embeddings.ipynb` | Generating and using embeddings |
| `013_vectordb.ipynb` | Storing and querying embeddings in a vector database |
| `014_bm25.ipynb` | Keyword-based retrieval with BM25 |
| `015_hybrid.ipynb` | Hybrid search (combining BM25 + embeddings) |
| `016_thinking.ipynb` | Extended thinking / reasoning features |
| `017_images.ipynb` | Sending and working with images |
| `018_citations_complete.ipynb` | Citations support for grounded responses |
| `019_caching.ipynb` | Prompt caching for cost/latency optimization |
| `020_code_execution.ipynb` | Code execution tool |

### Other folders

- **`AWS-Bedrock/`** – Examples of calling Claude through Amazon Bedrock instead of the direct Anthropic API.
- **`app_starter/`** – A starter template/scaffold for building an application on top of Claude.
- **`cli_project/`** – A command-line interface project built using the Claude API.
- **`images/`** – Sample/supporting images used in the notebooks.

### Supporting files

- `questions-answers.md` / `report.md` – Sample text/markdown content used as test data within some of the notebooks (e.g. for RAG, search, and citation exercises).
- `streaming.csv` – Sample data used in the streaming examples.
- `earth.pdf`, `VoyageAI_API_Key_Directions.pdf` – Reference/sample documents used in certain notebooks.

## Getting started

### Prerequisites
- Python 3.9+
- An [Anthropic API key](https://console.anthropic.com/)
- (Optional) AWS credentials, if you want to run the Bedrock examples

### Setup

```bash
git clone https://github.com/AndreasPr/Claude-API.git
cd Claude-API
```

Create a `.env` file in the project root with your API key:

```
ANTHROPIC_API_KEY=your-api-key-here
```

Then open any notebook with Jupyter:

```bash
jupyter notebook
```

> **Note:** Never commit your real API keys. If a `.env` file exists in this repo, make sure it does not contain live secrets before publishing or sharing the repository.

## Why this repo exists

This project was built to systematically learn the Claude API surface area — prompting fundamentals, tool use, multimodal input, retrieval-augmented generation, prompt caching, and cloud deployment via AWS Bedrock — through small, focused, runnable examples rather than just reading documentation. It's shared publicly as a demonstration of applied experience working with Claude and modern LLM tooling.

## Tech stack

- **Language:** Python, Jupyter Notebook
- **Core API:** Anthropic Claude API
- **Cloud:** AWS Bedrock (for cloud-hosted Claude access)
- **Concepts covered:** prompting, tool use, streaming, embeddings, vector search, BM25, hybrid retrieval, citations, prompt caching, code execution, multimodal (image) input
