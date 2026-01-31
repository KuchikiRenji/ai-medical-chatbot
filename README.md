# AI Medical Chatbot – Healthcare Conversational AI with RAG & LLMs

<!--
  SEO meta: Production-ready AI medical chatbot for healthcare. Open-source medical consultation assistant using IBM WatsonX, OpenAI, RAG, and LLMs (Llama 3, Mixtral). Medical interviewer, fine-tuning, Gradio UI. Python 3.9+.
-->

<div align="center">

![AI Medical Chatbot – Healthcare conversational AI with RAG and LLMs](assets/images/posts/README/im-778762.png)

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python](https://img.shields.io/badge/python-3.9%2B-blue)](https://www.python.org/downloads/)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

**Production-ready AI medical chatbot for healthcare.** Open-source medical consultation assistant using **IBM WatsonX**, **OpenAI**, **RAG**, and multiple **LLMs** (Llama 3, Mixtral, GPT).

[Features](#-features) · [Quick Start](#-quick-start) · [Installation](#-installation) · [Usage](#-usage) · [Project Structure](#-project-structure) · [FAQ](#-faq) · [Author](#-author)

</div>

---

## What is this?

**AI Medical Chatbot** is an open-source, production-ready **healthcare conversational AI** system. It helps with medical consultation assistance using **Retrieval Augmented Generation (RAG)**, **IBM WatsonX**, **OpenAI**, and multiple foundation models (e.g. **Llama 3**, **Mixtral**, **GPT-4**). It includes a **medical interviewer**, fine-tuning pipelines, and **Gradio** web UIs.

> **Disclaimer:** This software does not replace a doctor. It helps explore possible health-related information. Always consult a qualified healthcare professional for medical advice.

| | |
|---|---|
| **Version** | 2.0.0 |
| **Status** | Production-ready |
| **License** | Apache 2.0 |

---

## Features

- **Multi-model support** – flan-ul2-20b, mt0-xxl-13b, gpt-neox-20b, flan-t5-xxl-11b, mpt-7b-instruct, **OpenAI GPT-4/3.5**, **Meta Llama 3**, fine-tuned variants  
- **RAG-powered answers** – Retrieval Augmented Generation for context-aware medical responses  
- **Vector stores** – Milvus, FAISS, ChromaDB for similarity search  
- **Medical interviewer** – Chatbot that conducts structured medical interviews  
- **Gradio UIs** – Web interfaces for chatbot and interviewer  
- **Production setup** – Tests (pytest), type hints, PEP 8, Makefile, optional CI/CD  

---

## Quick Start

### Prerequisites

- **Python 3.9+**
- **UV** (recommended) or **pip**
- API keys: **OpenAI** and/or **IBM WatsonX**

### Installation

**With UV (recommended):**

```bash
pip install uv
git clone https://github.com/KuchikiRenji/ai-medical-chatbot.git
cd ai-medical-chatbot
make install
# Optional: make install-dev  |  make install-gpu
```

**With pip:**

```bash
git clone https://github.com/KuchikiRenji/ai-medical-chatbot.git
cd ai-medical-chatbot
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -e .
```

### Environment

Create a `.env` in the project root:

```bash
OPENAI_API_KEY=your_openai_api_key_here
# Optional: WatsonX
WATSONX_API_KEY=your_watsonx_api_key_here
WATSONX_PROJECT_ID=your_project_id_here
# Optional: Milvus
REMOTE_SERVER=127.0.0.1
SYSTEM_MESSAGE=You are a helpful medical assistant.
```

---

## Usage

**Run the medical chatbot:**

```bash
make run-chatbot
# or: python 5-HuggingFace/app.py
```

**Run the medical interviewer:**

```bash
make run-interviewer
# or: python 8-Interviewer/hf/app.py
```

**Development commands:**

```bash
make help          # List all targets
make format        # black + isort
make lint          # flake8, pylint
make type-check    # mypy
make test          # pytest
make test-cov      # tests + coverage
make clean         # Remove artifacts
```

---

## Project Structure

| Component | Description |
|-----------|-------------|
| [**1-Environment**](./1-Environment/README.md) | Local environment and model setup |
| [**2-Data**](./2-Data/README.md) | Medical datasets and preprocessing |
| [**3-Modeling**](./3-Modeling/README.md) | RAG, feature engineering, model building |
| [**4-Chatbot**](./4-Chatbot/) | Chatbot logic and references |
| [**5-HuggingFace**](./5-HuggingFace/README.md) | Production chatbot app (Gradio, WatsonX) |
| [**6-FineTunning**](./6-FineTunning/README.md) | Fine-tuning medical LLMs |
| [**7-Multimodal**](./7-Multimodal/README.md) | Multimodal medical chatbot (e.g. images) |
| [**8-Interviewer**](./8-Interviewer/README.md) | Medical interviewer app |

### Related resources

- **WatsonX + Milvus:** [Watsonx-Assistant-with-Milvus-as-Vector-Database](https://github.com/ruslanmv/Watsonx-Assistant-with-Milvus-as-Vector-Database)  
- **Custom LLM chatbot:** [Medical-Chatbot-with-Langchain-with-a-Custom-LLM](https://github.com/ruslanmv/Medical-Chatbot-with-Langchain-with-a-Custom-LLM)  
- **Playground / demos:** [Medical-Llama3-Chatbot](https://huggingface.co/spaces/ruslanmv/Medical-Llama3-Chatbot), [AI-Medical-Chatbot](https://huggingface.co/spaces/ruslanmv/AI-Medical-Chatbot), [Medical-Interviewer](https://huggingface.co/spaces/ruslanmv/Medical-Interviewer)  
- **Fine-tuned models:** [Medical-Llama3-8B](https://huggingface.co/ruslanmv/Medical-Llama3-8B), [Medical-Llama3-v2](https://huggingface.co/ruslanmv/Medical-Llama3-v2), [Medical-Mixtral-7B-v2k](https://huggingface.co/ruslanmv/Medical-Mixtral-7B-v2k)  
- **Empathy / NVC:** [Empathy Chatbot v1](https://huggingface.co/spaces/ruslanmv/Empathy_Chatbot_v1), [empathyondemand](https://github.com/energycombined/empathyondemand)  
- **Watsonx Medical MCP Server:** [watsonx-medical-mcp-server](https://github.com/ruslanmv/watsonx-medical-mcp-server)  

---

## FAQ

**What is an AI medical chatbot?**  
An AI medical chatbot is a conversational system that uses natural language and (often) RAG/LLMs to help with health-related questions. It does not replace a doctor and should be used only as an informational aid.

**Which models are supported?**  
The project supports IBM WatsonX models (e.g. flan-ul2, mt0-xxl, gpt-neox, flan-t5, mpt-7b), OpenAI GPT-4/GPT-3.5, and fine-tuned Llama 3 and Mixtral variants.

**Do I need WatsonX and OpenAI?**  
You need at least one: OpenAI and/or IBM WatsonX. Configure the corresponding API keys in `.env`.

**Is this for production use?**  
The codebase is structured for production (tests, type hints, Makefile). Deployment and compliance (e.g. HIPAA, local regulations) are your responsibility.

**How do I run the medical interviewer?**  
Use `make run-interviewer` or `python 8-Interviewer/hf/app.py`. See [8-Interviewer](./8-Interviewer/README.md).

---

## Contributing

Contributions are welcome: bug reports, feature ideas, and pull requests. Please follow usual open-source guidelines for patches and issues.

---

## License

This project is licensed under the **Apache License 2.0**. See [LICENSE](LICENSE) for the full text.

---

## Author

**KuchikiRenji**

- **Email:** [KuchikiRenji@outlook.com](mailto:KuchikiRenji@outlook.com)
- **GitHub:** [github.com/KuchikiRenji](https://github.com/KuchikiRenji)
- **Discord:** `kuchiki_renji`

---

## Acknowledgments

- IBM WatsonX, OpenAI, and Hugging Face for models and infrastructure  
- Tilburg University for empathy/NVC research collaboration  
- The open-source community for contributions and feedback  

---

<div align="center">

[⬆ Back to top](#ai-medical-chatbot--healthcare-conversational-ai-with-rag--llms)

</div>
