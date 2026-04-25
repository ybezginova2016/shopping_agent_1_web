# Agent 1 — Tool-Calling Shopping Agent

## Overview

A conversational shopping assistant for an electronics store that demonstrates the core **ReAct pattern** in AI agents: **Reasoning + Acting**.

The agent receives a user request in natural language, decides which tools to call, executes them, and generates a response based on the results. This process continues in a loop until the task is complete.

**Demo video:** https://youtu.be/SACUXdGmMTo

### Problem Statement

The goal of this project is to demonstrate how an LLM-powered agent can go beyond simple text generation and interact with external tools to complete user tasks.

The agent can:

- understand shopping requests
- search products using filters
- select relevant items
- add products to cart
- remember context within one session
- show tool calls transparently in real time

### Data

- **Source:** Simulated electronics product catalog
- **Size:** Small demo catalog
- **Type:** Structured product data

The catalog includes product information such as:

- product ID
- product name
- category
- brand
- price
- rating

### Approach

#### Agent Logic

The project is built around a **ReAct loop**, where the agent repeatedly performs the following steps:

1. Understand the user request
2. Decide whether a tool is needed
3. Call the appropriate tool
4. Read the tool result
5. Decide the next action
6. Return the final answer when the task is complete

#### Tools Used

- **search_products**
  - filters the product catalog by:
    - query
    - category
    - brand
    - price
    - sort order

- **add_to_cart**
  - adds a selected product to the cart by product ID

#### Main Components

- **LLM: Claude Haiku**
  - understands user intent
  - decides what actions to take
  - chooses tool arguments

- **Tool Call Trace**
  - displays every tool call in real time
  - shows function name, arguments, and result

- **Cart**
  - stores products added during the session

- **Message History**
  - keeps short-term memory within a single session

#### Tech Stack

- Frontend: HTML, JavaScript
- LLM API: Anthropic Claude Haiku
- Architecture: ReAct agent pattern
- Tools: Function calling
- UI Components: chat interface, tool-call sidebar, cart, message history

### Results

The agent successfully demonstrates:

- single-step tool use
- multi-step tool use
- autonomous tool selection
- short-term conversational memory
- transparent tool-call tracing
- cart updates based on user intent

**Full project description and demo walkthrough:**
https://docs.google.com/document/d/1SEQ9Rkhqbe4n0PhngAN35SpD_sSbu0adjYZtsk-GinY/edit?tab=t.0

**Contacts**

- GitHub: https://github.com/ybezginova2016  
- LinkedIn: https://www.linkedin.com/in/yuliabezginova/  
- Telegram: https://t.me/ybezginova  
- Email: [ybezginova.rs@gmail.com](mailto:ybezginova.rs@gmail.com)