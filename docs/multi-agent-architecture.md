# Multi-Agent Architecture

## Overview

The system uses a master-agent and sub-agent architecture to enable modular, scalable, and intelligent execution of tasks across multiple systems.

---

## Master Agent

The master agent is responsible for:

* Understanding the user request
* Interpreting intent
* Breaking the request into tasks
* Routing tasks to appropriate sub-agents

---

## Sub-Agents

Each sub-agent is responsible for a specific domain:

### SAP Agent

* Executes SAP S/4HANA operations using OData APIs

### Email Agent

* Sends notifications and communication via Outlook

### RAG Agent

* Retrieves contextual knowledge from vector database

### External API Agent

* Interacts with third-party services

---

## Tool Isolation Strategy

Each agent operates independently with:

* Dedicated tools
* Separate execution logic
* No shared responsibilities

This ensures:

* Reduced hallucination
* Clear separation of concerns
* Improved maintainability

---

## Execution Flow

1. Master agent receives request
2. Identifies required tasks
3. Routes tasks to appropriate sub-agents
4. Sub-agents execute independently
5. Master agent aggregates responses
6. Final response returned to user

---

## Benefits

* Modular architecture
* Scalable design
* Improved accuracy
* Easy to extend with new agents
