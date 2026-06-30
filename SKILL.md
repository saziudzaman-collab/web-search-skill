---
name: web-search
description: Search the internet for real-time information like latest news, weather, scores, stock prices, or recent events.
metadata:
  require-secret: true
  require-secret-description: "Enter your Serper API key. Get free key at serper.dev"
---

# Web Search

## Examples

- "Search for latest news"
- "Search [topic] on the internet"
- "Find latest [topic]"
- "What is current [topic]"
- "Search for today's weather"
- "Find Bitcoin price"

## Instructions

Call the `run_js` tool using `index.html` and a JSON string for `data` with the following fields:
- **query**: Required. Extract ONLY the key search terms from the user's request (e.g., "latest AI news", "Delhi weather today", "Bitcoin price"). Remove conversational words like "search for", "find me", "what is".

**Constraints:**
- Keep the query short: 2-5 English keywords only.
- Always respond in the same language as the user's original prompt.
- If no result is found, say: "I couldn't find reliable information right now. Please try again."
