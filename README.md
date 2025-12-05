# Simulating B2B Sales Process Using Agentic AI

Prediction Guard Sales Agent is our end-to-end prototype for collapsing the entire B2B revenue motion into a secure, automated workflow. In a single demo, we show revenue leaders how tightly orchestrated LLM agents can research leads, book meetings, and send bespoke quotes faster than a traditional team while keeping sensitive data inside enterprise guardrails. It is the pitch deck we run live whenever someone asks what "agentic AI for sales" actually looks like.

This repository contains the research and codebase for our project presented at the Decision Sciences Institute conference. The goal was to explore the automation of B2B sales pipelines using AI agents deployed via [Prediction Guard](https://predictionguard.com) and LangChain, comparing performance with traditional human-led workflows.

## Project Overview

We designed a full-stack simulation of a modern sales pipeline using LLM agents to automate:
- Lead research
- Lead qualification
- Meeting scheduling
- Email outreach
- Meeting transcription
- Quote generation

Each agent replicates a traditional sales task and collectively forms a robust simulation environment for evaluating AI vs. human performance in sales.

## Agent Directory

### Gmail & Calendar Agent (`Gmail and calendar agent/`)
- `calendar agent.ipynb` spins up a two-agent CrewAI workflow that converts raw meeting transcripts into calendar invites by calling Composio’s Google Calendar and Gmail tools. The first agent schedules events (with Meet links) based on natural-language instructions, and the second automatically emails attendees with the generated details.

### Lead Agent (`Lead agent/`)
- `SalesAgent_summary_updated.ipynb` uses LangChain prompt templates plus Prediction Guard’s Hermes models to fuse company data, meeting notes, and analyst-selected topics into a concise research brief. The notebook is the “prep work” layer that arms downstream agents with structured context about each prospect.

### Lead Qualification Agent (`Lead Qualification Agent/`)
- The `src/` package encrypts and decrypts meeting transcripts (`data_loader.py`, `process_transcripts.py`), summarizes calls, infers next steps, and scores readiness in `ai_agent.py`. Companion utilities generate tailored product bundles, pricing terms, and subscription recommendations so reps always know which Prediction Guard offer best fits each account. The module ships with unit tests plus secure config helpers to keep Prediction Guard API keys out of notebooks.

### Quotation Agent (`Quotation agent/`)
- `main.py` orchestrates the data loaders and recommendation utilities to output a JSON sales quote per company. It pulls the cleaned meeting summary, recommended deployment model, product mix, and contractual terms, then saves the finished proposal to `Quotation agent/output/` for handoff to the customer.

## My Key Contributions



## Results Summary

| Metric                  | AI Pipeline | Human Workflow |
|-------------------------|-------------|----------------|
| Outreach/day            | 100 leads   | 30–50 leads     |
| Cost/Qualified Lead     | <$0.03      | $50–200         |
| Lead Score Precision    | ~60%        | 65–75%          |
| Sales Cycle Time        | 4 hours     | 13 hours        |

## Paper

*“Simulating B2B Sales Process Using Agentic AI”*  
Presented at: **Decision Sciences Institute 2025** and **INFORMS 2025 Poster Presentation Contest** 
Authors: Chhaya Tundwal, Kshitij Chauhan, Vishnu Anand, et al.

## Tech Stack

- LangChain
- Prediction Guard LLMs
- Google Calendar API
- Gmail API
- Python, JSON, Flask (for agent interface)
- Hugging Face Tokenizer
