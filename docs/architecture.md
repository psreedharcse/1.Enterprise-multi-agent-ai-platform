# High-Level Architecture

## Overview

The system is designed as a layered multi-agent AI architecture enabling intelligent orchestration across SAP and enterprise systems.

---

## Architecture Layers

### 1. User Layer

Handles user interaction through Microsoft Teams, APIs, or UI.

### 2. Channel Layer

Routes requests via bot framework, API gateway, or webhooks.

### 3. LLM Layer

Processes natural language input to:

* Understand intent
* Extract entities

### 4. Agent Layer

Acts as the decision engine:

* Determines required actions
* Breaks tasks into steps
* Routes to appropriate tools

### 5. MCP Layer

Provides standardized tool orchestration:

* Enables dynamic tool selection
* Supports reusable and modular architecture

### 6. Tool Layer

Includes specialized agents:

* SAP Agent → Executes SAP operations via OData APIs
* Email Agent → Sends notifications via Outlook
* RAG Agent → Retrieves contextual knowledge

### 7. Data Layer

Includes enterprise systems:

* SAP S/4HANA
* Email systems
* Vector database (for RAG)

### 8. Response Layer

Aggregates results and sends response back to the user.

---

## Summary Flow

User → Channel → LLM → Agent → MCP → Tools → Systems → Response → User
