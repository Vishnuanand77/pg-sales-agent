# Simulating B2B Sales Process Using Agentic AI

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

## My Key Contributions

### Project Architecture & Agent Design – *Vishnu Anand*
- Created the **overall simulation pipeline** structure
- Built the **Calendar Scheduling Agent** using Google Calendar API and LangChain
- Developed the **Gmail Email Agent** to auto-send meeting invites
- Branch link: [`vishnu/agents`]([https://github.com/your-repo-name/tree/vishnu/agents](https://github.com/Vishnuanand77/pg-sales-agent/tree/Vishnu_gmail_calendar_agent)) *(replace with actual URL)*

Other agents were implemented by team members specializing in data engineering, LLM tuning, and UI.

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
