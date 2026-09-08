🧠 ResearchMind AI

Your Complete AI Research Team

ResearchMind AI is a multi-agent AI research platform designed to help users research, analyze, verify, visualize, summarize, cite, and generate professional reports from a single workspace.

Instead of relying on one general-purpose AI assistant, ResearchMind AI uses 9 specialized AI agents, each responsible for a different stage of the research workflow.

🚀 Core Idea

ResearchMind AI follows a complete research workflow:

Research → Analyze → Retrieve → Verify → Cite → Visualize → Summarize → Write → Orchestrate

The platform supports both:

Individual Agent Mode — use one specialist agent for a specific task.

Multi-Agent Mode — select multiple agents and let them work together, with the Orchestrator combining their results.

🤖 9 AI Agents

Agent

Main Responsibility

🔎 Research Agent

Web research and information discovery

📄 PDF Analysis Agent

PDF extraction, document analysis and OCR

🧠 Knowledge Agent

Private knowledge-base retrieval

📝 Report Writer Agent

Professional report generation and export

🔗 Citation Agent

Citation and reference management

✅ Fact Checker Agent

Claim verification and evidence checking

📊 Visualization Agent

Generates actual charts and visual outputs

🧾 Summary Agent

Research and document summarization

🎯 Orchestrator Agent

Coordinates multiple agents and workflows

🔎 1. Research Agent

The Research Agent performs research-oriented tasks and gathers relevant information.

Features

Web research

Topic exploration

Information discovery

Source-oriented research

Research synthesis

Follow-up questions

Conversational research context

Research results can be passed to other agents for verification, citation, visualization, summarization, or report generation.

📄 2. PDF Analysis Agent

The PDF Analysis Agent processes uploaded documents.

Features

PDF upload

Text extraction

Document analysis

Structured document understanding

Scanned PDF support

OCR fallback for image-based PDFs

Document ID tracking

Follow-up questions about uploaded documents

The system attempts normal PDF text extraction first and can use OCR when the document is scanned or contains image-only pages.

🧠 3. Knowledge Agent

The Knowledge Agent is designed for retrieving information from private knowledge sources.

Features

Knowledge retrieval

Context-aware answers

Private document information

Research context integration

Follow-up questions

This allows ResearchMind AI to combine external research with private knowledge.

📝 4. Report Writer Agent

The Report Writer Agent converts research and analysis into professional reports.

Report Structure

Reports can include:

Title

Executive Summary

Introduction

Background

Objectives

Methodology

Analysis

Findings

Discussion

Advantages

Limitations

Future Scope

Conclusion

References

Export Formats

PDF

DOCX

Markdown

TXT

HTML

PDF is the primary professional report format.

🔗 5. Citation Agent

The Citation Agent focuses on references and supporting sources.

Features

Citation generation

Reference organization

Source tracking

Research-to-reference linking

Citation-ready report content

✅ 6. Fact Checker Agent

The Fact Checker Agent evaluates claims and identifies supporting or uncertain evidence.

Features

Claim verification

Evidence comparison

Fact checking

Uncertainty indication

Research source analysis

Verification summaries

The goal is to reduce unsupported or unreliable information in research outputs.

📊 7. Visualization Agent

The Visualization Agent is designed to produce actual visual outputs, not only describe charts or return plotting code.

Supported Visualization Types

Bar charts

Line charts

Pie charts

Scatter plots

Other data-driven visualizations

Workflow

Research/Data → Chart Specification → Matplotlib → PNG Visualization → Display in Chat

Generated visualizations can be displayed directly in the ResearchMind AI workspace and can be saved/exported where supported.

🧾 8. Summary Agent

The Summary Agent converts large research outputs and documents into concise, understandable summaries.

Features

Research summarization

PDF summarization

Key-point extraction

Findings summary

Short and structured summaries

Context-aware follow-up

🎯 9. Orchestrator Agent

The Orchestrator is the coordination layer of ResearchMind AI.

It can combine multiple specialist agents into one workflow.

Example

A user can request:

Research the impact of AI in education, verify the major claims, add citations, create a visualization, and prepare a report.

The system can coordinate:

Research Agent
↓
Fact Checker Agent
↓
Citation Agent
↓
Visualization Agent
↓
Report Writer Agent
↓
Orchestrator

The final output is synthesized into a coherent research result.

🤝 Multi-Agent Mode

ResearchMind AI supports selecting multiple agents for a single request.

Example Workflow

User Request
     ↓
Selected Agents
     ↓
┌───────────────┐
│ Research      │
│ Fact Checker  │
│ Citation      │
│ Visualization │
│ Summary       │
└───────────────┘
     ↓
Orchestrator
     ↓
Unified Result

Each selected agent performs its own specialist responsibility rather than simply repeating the same task.

💬 Intelligent Chat

ResearchMind AI includes a conversational research workspace.

Chat Features

Continuous conversation

Follow-up questions

Context preservation

Chat memory

New Conversation

Clear Conversation

Copy responses

Loading indicators

Error handling

Markdown rendering

Scrollable output

Enter to send

Shift + Enter for a new line

Auto-expanding message input

Three-dot menu and controls

Chat history can be stored locally so conversations can continue within the browser.

📑 PDF + OCR Pipeline

ResearchMind AI supports both standard and scanned PDFs.

PDF Upload
    ↓
Document ID
    ↓
Text Extraction
    ↓
Is readable text available?
   ↙                 ↘
 YES                  NO
 ↓                    ↓
Analyze              OCR
 ↓                    ↓
 └──────────┬─────────┘
            ↓
       AI Analysis

OCR support is intended for image-based/scanned documents.

📊 Agent Performance

The platform can be extended to expose agent-level performance information such as:

Agent status

Current task

Response time

Success/failure

Sources processed

Documents processed

Visualizations generated

Workflow completion

This provides visibility into the multi-agent research pipeline.

🎨 User Interface

ResearchMind AI uses a dark blue/purple professional research interface.

The main interface includes:

ResearchMind AI branding

Navigation bar

Hero section

9-agent overview

Agent workspace

Workflow section

About section

Pricing section

Contact section

Get Started action

Professional footer

Three-dot controls

The current UI is intended to remain consistent rather than being repeatedly redesigned.

🏗️ System Architecture

                 ┌─────────────────────┐
                 │    React Frontend   │
                 │      + Vite         │
                 └──────────┬──────────┘
                            │
                            │ HTTP / REST
                            ↓
                 ┌─────────────────────┐
                 │    FastAPI Backend  │
                 └──────────┬──────────┘
                            │
          ┌─────────────────┼─────────────────┐
          ↓                 ↓                 ↓
     Groq / LLM          Tavily            OCR/PDF
          │                 │                 │
          └─────────────────┼─────────────────┘
                            ↓
                  ┌──────────────────┐
                  │ 9 AI Agents      │
                  └────────┬─────────┘
                           ↓
                    Orchestrator
                           ↓
                    Unified Output

🛠️ Technology Stack

Frontend

React

Vite

JavaScript

CSS

React Markdown

Remark GFM

Backend

Python

FastAPI

Uvicorn

AI / Data

Groq

Tavily

Hugging Face

Pandas

NumPy

Matplotlib

PDF / OCR

pypdf

PyMuPDF

Pillow

pytesseract

Tesseract OCR

📁 Project Structure

researchmind-ai/
│
├── frontend/
│   ├── src/
│   │   ├── App.jsx
│   │   ├── index.css
│   │   └── ...
│   ├── package.json
│   └── ...
│
├── main.py
├── requirements.txt
├── .env
├── README.md
└── ...

⚙️ Installation

1. Clone the Repository

git clone https://github.com/ideoflux/researchmind-ai.git
cd researchmind-ai

2. Backend Setup

Create a virtual environment:

python -m venv venv

Activate it on Windows:

venv\Scripts\activate

Install dependencies:

pip install -r requirements.txt

Start the FastAPI backend:

uvicorn main:app --reload

Backend:

http://127.0.0.1:8000

API documentation:

http://127.0.0.1:8000/docs

💻 Frontend Setup

Open a second terminal.

cd frontend
npm install
npm run dev

Frontend:

http://localhost:5173

🔐 Environment Variables

Create a .env file for the backend.

GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
HF_TOKEN=your_huggingface_token

Never commit real API keys to GitHub.

Add .env to .gitignore:

.env
venv/
node_modules/
__pycache__/
*.pyc

🔌 Main API Endpoints

The backend provides endpoints for the major platform workflows.

Examples include:

POST /run-agent
POST /run-multi-agent
POST /upload-pdf
GET  /visualizations/{image_id}
POST /export-report

Exact endpoint behavior depends on the current backend implementation.

🔄 Example Research Workflow

Simple Research

User
 ↓
Research Agent
 ↓
Research Result

Research + Verification

User
 ↓
Research Agent
 ↓
Fact Checker Agent
 ↓
Verified Result

Research + Report

User
 ↓
Research Agent
 ↓
Summary Agent
 ↓
Report Writer Agent
 ↓
PDF Report

Complete Workflow

User
 ↓
Research
 ↓
PDF / Knowledge Analysis
 ↓
Fact Checking
 ↓
Citation
 ↓
Visualization
 ↓
Summary
 ↓
Report Writing
 ↓
Orchestrator
 ↓
Final Research Package

🧪 Testing Checklist

Before considering the application production-ready, test:

Frontend

Homepage loads

All navigation sections work

All 9 agents appear

Individual agent selection works

Multi-agent selection works

Chat sends messages

Enter sends

Shift + Enter creates a newline

Follow-up questions preserve context

New Conversation works

Clear Conversation works

Copy works

Markdown renders correctly

PDF upload works

Visualization image appears

Report export works

Backend

FastAPI starts

/run-agent works

/run-multi-agent works

PDF extraction works

OCR works for scanned PDFs

Research works with Tavily

LLM requests work with Groq

Visualization generation works

Generated images are accessible

Report export works

Errors are handled correctly

Security

API keys are not exposed

.env is ignored

Uploaded files are validated

Production CORS is configured

API rate limits are considered

🚀 Deployment

The application can be deployed using services such as:

GitHub

Render

Other cloud platforms supporting React and FastAPI

A typical production setup is:

GitHub
   ↓
Frontend Hosting
   +
FastAPI Backend Hosting
   ↓
External AI APIs

For production deployment, configure the frontend API URL to point to the deployed backend instead of:

http://127.0.0.1:8000

🗺️ Future Scope

Potential future improvements include:

User authentication

Cloud chat history

Persistent knowledge bases

Vector database integration

Advanced RAG

More document formats

Better OCR

Streaming AI responses

Agent performance dashboard

Advanced citation styles

Team collaboration

Research project workspaces

Saved research projects

More visualization types

Advanced report templates

Role-based access

Production monitoring

Usage analytics

🎯 Product Vision

ResearchMind AI aims to become a complete AI research workspace where users do not need to switch between multiple tools.

Instead of:

Search Engine
+
PDF Reader
+
AI Chatbot
+
Fact Checker
+
Citation Tool
+
Chart Tool
+
Report Writer

ResearchMind AI brings these capabilities together:

              RESEARCHMIND AI
                    │
     ┌──────────────┼──────────────┐
     ↓              ↓              ↓
  Research       Documents      Knowledge
     ↓              ↓              ↓
 Fact Check      Analyze         Retrieve
     └──────────────┼──────────────┘
                    ↓
                Citation
                    ↓
              Visualization
                    ↓
                 Summary
                    ↓
              Report Writer
                    ↓
              Orchestrator
                    ↓
             Final Research

⭐ Why ResearchMind AI?

One Platform

All major research tasks are available from one workspace.

Specialized Agents

Each agent has a clearly defined responsibility.

Multi-Agent Intelligence

Complex research tasks can be divided among specialist agents.

Document Intelligence

Users can upload and analyze PDFs, including scanned documents with OCR support.

Evidence-Oriented Research

Fact checking and citation workflows help users produce more reliable research.

Visual Research

The Visualization Agent can turn data into actual charts and images.

Professional Reports

Research can be transformed into structured professional documents.

📌 Current Project Status

ResearchMind AI has the core architecture for:

9-agent architecture

Individual agent workflows

Multi-agent workflows

Conversational chat

Chat memory

PDF upload

OCR fallback

Research integration

Citation workflow

Fact checking

Visualization generation

Summary generation

Report generation/export

React + FastAPI architecture

Some production-level capabilities still require final integration testing, API configuration, deployment validation, and performance/security hardening.

📄 License

This project is intended for educational, research, and development purposes.

MIT License.

👨‍💻 Author

Jaswant VV

GitHub:

https://github.com/ideoflux/researchmind-ai

🧠 ResearchMind AI

Research smarter. Verify better. Visualize clearly. Write professionally.
