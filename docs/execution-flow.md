# Detailed Execution Flow

## Overview

This flow describes how a user query is processed end-to-end using LLM reasoning, agent decision-making, and MCP-based tool execution.

---

## Step-by-Step Execution

### Step 1: User Query

User submits a natural language request via Teams, API, or UI.

---

### Step 2: LLM Reasoning

The LLM processes the query to:

* Understand intent
* Extract relevant entities
* Interpret user requirements

---

### Step 3: Agent Decision Layer

The agent:

* Analyzes the LLM output
* Breaks the request into tasks
* Determines which tools are required

---

### Step 4: MCP Tool Selection

MCP dynamically selects appropriate tools:

* SAP Tool → For business operations
* Email Tool → For notifications
* RAG Tool → For knowledge retrieval

---

### Step 5: Tool Execution

Each selected tool executes:

* SAP APIs retrieve or update data
* Email system sends notifications
* RAG system retrieves contextual information

---

### Step 6: Response Aggregation

Results from all tools are collected and combined into a structured response.

---

### Step 7: Final Output

The system generates a final response and returns it to the user.

---

## Summary Flow

Query → Reasoning → Decision → Tool Selection → Execution → Aggregation → Response
7
