# 🥣 AI Breakfast Planner (Multi-Agent Chatbot)

An **AI-powered, multi-agent chatbot** that helps users plan healthy, affordable breakfasts by combining nutrition data, web search, and price discovery.

The system uses an **agentic architecture** where specialized agents collaborate to:
- Suggest breakfast options
- Calculate calories and nutrition
- Fetch missing data from the web
- Estimate real-world prices

---

## ✨ Features

- 🤖 **Multi-Agent Chatbot** for breakfast planning  
- 🥗 **Calorie & Nutrition Analysis**  
- 🌐 **Web-augmented knowledge** when local data is missing  
- 💰 **Price estimation** for suggested breakfasts  
- ⚡ Built with modern Python and OpenAI tooling  

---

## 🧠 Architecture Overview

The chatbot is composed of multiple intelligent agents, each with a focused responsibility:

### 1. Planner Agent
- Interacts with the user
- Understands dietary preferences and constraints
- Proposes breakfast options

### 2. Nutrition Agent (RAG-based)
- Uses a **Retrieval-Augmented Generation (RAG)** pipeline
- Fetches calorie and nutrition information from a vector database

### 3. Web Search Agent
- Triggered when nutrition data is **not found** in the RAG database
- Uses **Exa Search** to fetch reliable information from the web

### 4. Price Discovery Agent
- Uses **OpenAI WebSearchTool Agent**
- Fetches approximate prices for breakfast items from online sources

---

## 🧰 Tech Stack

- **Language:** Python 3.13  
- **LLM:** OpenAI  
- **Agent Framework:** Agentic (multi-agent orchestration)  
- **Vector Store:** ChromaDB  
- **RAG Database:** Food & calorie embeddings  
- **Web Search:** Exa Search  
- **Price Fetching:** OpenAI WebSearchTool Agent  

---

## 📁 Project Structure

```text
.
├── agents/
│   ├── planner_agent.py
│   ├── nutrition_agent.py
│   ├── web_search_agent.py
│   └── price_agent.py
├── rag/
│   ├── chromadb/
│   └── ingest.py
├── prompts/
├── main.py
├── requirements.txt
└── README.md
