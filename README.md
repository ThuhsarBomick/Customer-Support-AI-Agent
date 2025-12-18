Customer Support AI Agent (RAG-Powered)

Automated customer support system that classifies incoming emails, retrieves verified answers using Retrieval-Augmented Generation (RAG), drafts replies, and assigns queries to support agents — built using n8n.

 Overview

This project implements an end-to-end Customer Support AI Agent that removes manual email triage and response drafting.

Incoming customer emails are:

Classified (Support vs Promotional)

Routed to an AI agent

Enriched with verified policy data from a vector database

Drafted into professional email responses

Assigned to a support agent with notifications

The system ensures fast, accurate, and policy-compliant replies while keeping humans in the loop.

 Key Features

Email Classification

Automatically categorizes incoming emails (Support / Promotional)

RAG-Based Knowledge Retrieval

Retrieves answers only from verified policy documents

Prevents hallucinations

AI-Drafted Responses

Generates professional, context-aware email drafts

Agent Assignment & Alerts

Notifies support agents when a draft is ready

Human-in-the-Loop

Drafts can be reviewed before sending

 Architecture
Gmail Trigger
   ↓
Email Pre-processing
   ↓
Text Classification
   ↓
AI Agent (RAG)
   ├─ Supabase Vector Store
   ├─ OpenAI Embeddings
   └─ Policy Retrieval
   ↓
Email Draft Creation
   ↓
Agent Notification

Components
Component	Purpose
Gmail Trigger	Listens for incoming support emails
Text Classifier	Classifies emails by intent
AI Agent	Generates responses using RAG
Supabase Vector Store	Stores policy embeddings
OpenAI Embeddings	Enables semantic search
Gmail Draft	Creates reply drafts
Notifications	Alerts assigned agents
🛠️ Tech Stack

Automation: n8n

LLM: OpenAI

Vector Database: Supabase (pgvector)

Email: Gmail API

AI Pattern: Retrieval-Augmented Generation (RAG)

📈 Impact

Reduced manual email triage

Faster first response time

Consistent, policy-accurate answers

Scalable customer support automation

Production-ready workflow

 Repository Contents
.
├── customer-support-ai-agent-workflow.json
└── README.md

How to Use

Import the JSON workflow into n8n

Configure credentials (Gmail, OpenAI, Supabase)

Add your policy documents to the vector store

Activate the workflow

What This Project Demonstrates

Building production-ready AI automation systems

Implementing RAG pipelines in real workflows

Combining LLMs + vector search + automation

Designing human-in-the-loop AI systems

Shipping practical AI solutions using n8n
