# 🔎 LangChain Search Agent — Conversational Web & Research Assistant

## 🚀 Project Overview

This is an **AI-powered conversational search agent** built with **LangChain** and **Streamlit**, capable of searching the web, Wikipedia, and scientific papers from Arxiv — all in real-time — to deliver **relevant, concise answers** to your questions.

The app leverages **LangChain agents** to dynamically choose the best information source, integrate results, and respond naturally in a chat interface.  
It showcases skills in **tool-augmented LLMs**, **API integration**, and **real-time conversational UX**.

---

## 💡 Key Features

- **Multi-Source Search:**
  - 🔍 **DuckDuckGo Search** for general web queries.
  - 📚 **Wikipedia Search** for quick factual lookups.
  - 📄 **Arxiv Search** for scientific research papers.
- **LangChain Agents:** Uses a `ZERO_SHOT_REACT_DESCRIPTION` agent to decide which tool(s) to call based on the user query.
- **Groq LLM Integration:** Powered by **Llama3-8b-8192** for fast and accurate responses.
- **Live Thought Process:** Displays the agent’s reasoning steps using `StreamlitCallbackHandler`.
- **Interactive Chat UI:** Maintains conversation history for a smooth chat-like experience.
- **Configurable API Key:** Securely input your Groq API key from the sidebar.

---

## 🎯 Why This Project?

This project demonstrates **production-relevant AI engineering skills**, including:

- **Tool-Augmented LLM Workflows** — enabling the LLM to call APIs and fetch real-time data.
- **Research Assistant Use Case** — combines general, encyclopedic, and academic knowledge sources.
- **LangChain Agent Integration** — implements reasoning + action loop for tool selection.
- **Streamlit Frontend** — builds an interactive UI for non-technical end users.

It’s a **portfolio-ready showcase** of how AI can be extended beyond static knowledge into **live, dynamic information retrieval**.

---

## 📦 Tech Stack

| Technology              | Purpose                                         |
| ----------------------- | ----------------------------------------------- |
| Python 3.8+             | Core programming language                       |
| Streamlit               | Web UI framework                                |
| LangChain               | Agent orchestration and tool integration       |
| Groq LLM API            | Language model for reasoning & answering        |
| DuckDuckGo Search Tool  | Web search integration                          |
| Wikipedia API Wrapper   | Encyclopedic knowledge search                   |
| Arxiv API Wrapper       | Scientific paper search                         |
| python-dotenv           | Environment variable management                 |

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- A valid **Groq API Key** (register at [Groq](https://www.groq.com/))

### Installation

```bash
git clone https://github.com/yourusername/langchain-search-agent.git
cd langchain-search-agent

python -m venv venv
source venv/bin/activate  # Windows: .\venv\Scripts\activate

pip install -r requirements.txt
```

### Running the App
```bash

streamlit run app.py

```
- Enter your Groq API key in the sidebar.
- Type any query in the chat box (e.g., "What is machine learning?" or "Recent research papers on quantum computing").
- Watch the assistant think, choose tools, and fetch results in real time.


## 📈 How It Works — High-Level Flow
1. User Query Input: Captured via Streamlit’s chat_input.
2. Agent Initialization: LLM + tools (DuckDuckGo, Wikipedia, Arxiv) wrapped as LangChain tools.
3. Zero-Shot Agent Reasoning: Chooses which tool(s) to invoke based on the question.
4. Tool Execution: Fetches relevant search results from the selected source(s).
5. Response Generation: LLM composes a concise answer from the retrieved data.
6. Thought Process Display: StreamlitCallbackHandler streams the agent’s reasoning steps live.
7. Chat History Storage: Session state maintains conversation flow.


💡 This mini project is part of my AI portfolio to demonstrate practical LangChain agent applications for real-time information retrieval.