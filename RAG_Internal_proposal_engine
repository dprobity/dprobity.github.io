# Project: Strategic Proposal Factory (Internal Prototype)

## Executive Summary
An internal R&D project developing a multi-agent AI factory to automate high-stakes grant proposals (USAID/GAVI). The system prioritizes McKinsey-grounded logic and rigorous evaluation to solve the "capacity gap" in non-profit business development.

## Strategic Framework
* **The Problem:** Strategic NGOs often lose competitive bids due to inconsistent technical narratives and high-speed compliance requirements.
* **The Intensification:** Inconsistent AI outputs in traditional RAG systems create "fatal flaws" that lead to immediate disqualification.
* **The Solution:** A stateful multi-agent system grounded in **McKinsey MECE logic** and **Pyramid Principle** structuring.

## Technical Deep Dive: M&E for AI Agents
To ensure reliability before production, this prototype implements a rigorous **Monitoring & Evaluation** layer using **Truelens**:

### 1. The RAG Triad Evaluation
We measure the integrity of every generated response using three key feedback functions:
* **Context Relevance:** Evaluates if the retrieved "Institutional Memory" actually supports the query.
* **Groundedness:** A Judge Agent verifies that every claim in the response is explicitly supported by the retrieved context.
* **Answer Relevance:** Ensures the final technical narrative helpfully addresses the donor's original prompt.

### 2. GPA Alignment Monitoring
Using **LangGraph's StateGraph**, we track:
* **Goal Fulfillment:** Did the agent meet the objective defined in the original RFP shredder?
* **Plan Adherence:** Did the agent follow the McKinsey "Issue Tree" skeleton designed at the start of the workflow?
* **Execution Consistency:** Detecting and correcting drift during multi-turn agent reasoning.

## Tool Requirements & Stack
* **Orchestration:** LangGraph (Stateful workflow management).
* **Evaluation:** Truelens (Tracing, Triad metrics, and cost/latency monitoring).
* **Frameworks:** McKinsey Pyramid Principle & MECE Prompt Engineering.
* **Data Layer:** Private Vector Store (Chromadb/Pinecone) for Proprietary Data Sovereignty.
