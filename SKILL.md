| name | web-search |[span_0](start_span)[span_0](end_span)
| --- | --- |[span_1](start_span)[span_1](end_span)
| description | Search the internet for real-time information, scores, stock prices, or recent events. |[span_2](start_span)[span_2](end_span)
| metadata | **require-secret**: true <br> **require-secret-prompt**: Enter your Serper API key |[span_3](start_span)[span_3](end_span)

# Web Search[span_4](start_span)[span_4](end_span)

## Examples[span_5](start_span)[span_5](end_span)

* "Search for latest news[span_6](start_span)"[span_6](end_span)
* "Search [topic] on the internet[span_7](start_span)"[span_7](end_span)
* "Find latest [topic][span_8](start_span)"[span_8](end_span)
* "What is current [topic][span_9](start_span)"[span_9](end_span)
* "Search for today's weather[span_10](start_span)"[span_10](end_span)
* "Find Bitcoin price[span_11](start_span)"[span_11](end_span)

## Instructions[span_12](start_span)[span_12](end_span)

Call the `run_js` tool using `index.html` and a JSON string for `data` with the following fields:[span_13](start_span)[span_13](end_span)

* **query**: Required. Extract ONLY the key search terms from the user's request (e.g., "latest AI news", "Delhi weather today", "Bitcoin price"). Remove conversational words like "search for", "find me", "what is".[span_14](start_span)[span_14](end_span)

**Constraints:**[span_15](start_span)[span_15](end_span)

* Keep the query short: 2-5 English keywords only.[span_16](start_span)[span_16](end_span)
* Always respond in the same language as the user's original prompt.[span_17](start_span)[span_17](end_span)
* If no result is found, say: "I couldn't find reliable information right now. Please try again.[span_18](start_span)"[span_18](end_span)
