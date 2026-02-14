# Agentic-AI-Research-Assistant

# 🔎 Agentic AI Research Assistant

An Agentic AI-powered Research Assistant built using **LangGraph, LangChain, Groq LLM, and Tavily Search**, capable of autonomously using tools like Arxiv, Wikipedia, and Web Search to answer research queries.

Live Demo: [https://agentic-ai-research-assistant-jenzfs7znik77qrgzfuxge.streamlit.app/]

---

## 🚀 Overview

This project implements an **Agentic AI system** that:

- Accepts a research query
- Uses reasoning to decide which tools to call
- Retrieves data from:
  - 📚 Arxiv (Research Papers)
  - 📖 Wikipedia
  - 🌐 Tavily Web Search
- Synthesizes results using an LLM
- Returns a structured response

Unlike a simple chatbot, this system follows a:


loop using **LangGraph state-based execution**.

---

## 🧠 Architecture

### 1️⃣ Agent Graph (LangGraph)

The agent is implemented using a StateGraph workflow:

- START → LLM reasoning
- Conditional tool execution
- ToolNode (Arxiv, Wiki, Tavily)
- Loop back to LLM
- END

Graph builder: `agent.py`

Core logic:
- Tool binding
- Conditional edges
- Agent loop
- Environment variable validation

---

### 2️⃣ Tools Used

| Tool | Purpose |
|------|----------|
| ArxivQueryRun | Fetch research papers |
| WikipediaQueryRun | Fetch factual summaries |
| TavilySearch | Real-time web search |
| ChatGroq | LLM reasoning engine |

---

### 3️⃣ LLM

- Model: `qwen/qwen3-32b`
- Provider: Groq
- Tool-aware binding via `bind_tools()`

---

### 4️⃣ Streamlit UI

The frontend is built with Streamlit:

- Chat-style interface
- Session-based memory
- Cached agent loading
- Real-time response rendering

---

## 📦 Installation (Local Setup)

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/agentic-ai-research-assistant.git
cd agentic-ai-research-assistant



# 🔎 Agentic AI Research Assistant

An Agentic AI-powered research assistant that can autonomously use tools like Arxiv, Wikipedia, and Web Search to answer complex research queries.

Built with LangGraph, LangChain, Groq LLM, and Streamlit.

---

## 🚀 What This Project Does

This system allows users to:

- Ask research questions
- Automatically search research papers (Arxiv)
- Retrieve factual summaries (Wikipedia)
- Perform real-time web search (Tavily)
- Combine all information into one final answer

Unlike a simple chatbot, this assistant:
- Decides which tool to use
- Calls tools dynamically
- Loops between reasoning and tools
- Produces a structured final response

---

## 🧠 How It Works (Simple Explanation)

1. User enters a research query.
2. The LLM reasons about the question.
3. It selects the appropriate tool (Arxiv / Wikipedia / Web).
4. Tool returns data.
5. The LLM processes results.
6. Final answer is generated.

This is implemented using a graph-based agent loop with LangGraph.

---

## 🛠 Tech Stack

- Python
- LangChain
- LangGraph
- Groq (Qwen model)
- Tavily Web Search
- Arxiv API
- Wikipedia API
- Streamlit

---

## 📦 Installation (Run Locally)

### 1. Clone the repository

```bash
git clone https://github.com/your-username/agentic-ai-research-assistant.git
cd agentic-ai-research-assistant


