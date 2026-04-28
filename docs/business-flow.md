# End-to-End Business Flow

## Overview

This system enables users to perform enterprise operations across SAP and external systems using natural language, powered by a multi-agent AI architecture.

---

## Step-by-Step Flow

### Step 1: User Request

User submits a request via Microsoft Teams, API, or UI.

### Step 2: Channel Layer

The request is routed through a communication layer (Teams bot / API gateway / webhook).

### Step 3: LLM Processing

The Large Language Model processes the request to:

* Understand user intent
* Extract required entities

### Step 4: Agent Decision Layer

The master agent:

* Interprets intent
* Breaks request into tasks
* Determines required tools

### Step 5: Tool Selection & Invocation

The agent dynamically invokes tools:

* SAP Agent → SAP S/4HANA APIs (OData)
* Email Agent → Outlook notifications
* RAG Agent → Knowledge retrieval

### Step 6: Execution Layer

Each tool executes independently:

* Fetch or update SAP data
* Send emails
* Retrieve contextual information

### Step 7: Aggregation

Results from all tools are combined into a structured response.

### Step 8: Response Delivery

Final response is sent back to the user via the same channel.

---

## Summary Flow

User → Channel → LLM → Agent → Tools → SAP/External Systems → Response → User
