# Sales Assistant Agent

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://python.org)
[![LangGraph](https://img.shields.io/badge/LangGraph-Latest-green.svg)](https://langchain-ai.github.io/langgraph/)
[![Groq](https://img.shields.io/badge/Groq-LLM-orange.svg)](https://groq.com)

AI-powered sales assistant with human-in-the-loop approval. Built for Apple EMEIA Sales BPR requirements.

## Features

- **Sales Data Queries** - Get revenue, units sold, and growth metrics
- **Forecast Calculation** - Predict future sales based on growth assumptions  
- **Alert System** - Send team notifications with mandatory human approval
- **Human-in-the-Loop** - Sensitive actions pause and wait for human decision

## Architecture

User Question → Agent Decides → Safe? → Auto-Execute → Return
↓
Sensitive? → Ask Human → Approve? → Execute



## Tech Stack

| Technology | Purpose |
|------------|---------|
| LangGraph | Agent workflow orchestration |
| Groq API | Free LLM inference (Llama 3.1) |
| Python | Core programming |
| Gradio | Web interface |

## Quick Start

### Run in Colab (No Setup)

1. Click the badge below
2. Get free API key from [console.groq.com](https://console.groq.com)
3. Run all cells

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](YOUR_COLAB_LINK_HERE)

### Run Locally

```bash
git clone https://github.com/anshchordiya/sales-agent-langgraph.git
cd sales-agent-langgraph
pip install -r requirements.txt
export GROQ_API_KEY="your_key_here"
python sales_agent.ipynb


Example Output

User: How did Product X perform in Q2 2025?
Agent:
[SALES REPORT]
   Product: Product X
   Revenue: $1,800,000
   Units Sold: 1,450
   Growth: +20%

User: Send alert to UK team about Q3 results
Agent:
[HUMAN APPROVAL REQUIRED]
   To: UK team
   Message: Q3 results ready

Approve? (yes/no): yes

[APPROVED] Alert sent.


Author
Ansh Chordiya

GitHub: github.com/anshchordiya2002
LinkedIn: linkedin.com/in/anshchordiya


