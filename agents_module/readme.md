# Agents Module – Agentic RAG Implementation

## 📌 Overview
This project implements an **Agentic Retrieval-Augmented Generation (RAG)** system.  
The agent decides **when** to retrieve information from a FAQ knowledge base and **when** to answer directly.

The pipeline integrates:
- **Groq API** for LLM inference
- **FAQ Search Tool** for retrieval
- **Function Calling** for tool execution
- **Custom Agent Loop** to handle multi-step reasoning

---

## 🗂️ Workflow Diagram
![Agentic RAG Workflow](aef14b6c-bf21-4017-bcb5-fb24962a6685.png)

---

## ⚙️ Features
- **Dynamic tool calling** using Groq’s structured output
- **FAQ search integration** with knowledge base indexing
- **Custom tool registration** (`search_tool` & `add_entry_tool`)
- **Two-loop agent structure**:
  1. Main Q&A loop – handles user input
  2. Request-response loop – executes tools until final answer

---

## 📜 How It Works
1. User asks a question.
2. Agent decides whether FAQ retrieval is needed.
3. If yes → searches KB and retrieves top results.
4. Constructs context + question → sends to LLM.
5. Returns answer to user.

---

## 🚀 Running the Agent
```bash
# Clone repository
git clone https://github.com/yourusername/agents-module.git
cd agents-module

# Install dependencies
pip install -r requirements.txt

# Run in Jupyter
jupyter notebook
