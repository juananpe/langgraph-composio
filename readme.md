# Domain Deep Research Agent Guide

This guide provides detailed steps to create a Domain Deep Research Agent that leverages Composio, agentic frameworks such as Langgraph and Qwen3 to create a research agent. Ensure you have Python 3.8 or higher installed.


## Steps to Run

```
uv venv

source .venv/Scripts/activate # Windows
source .venv/bin/activate # macOS/Linux

# Login to your account
composio login

composio add tavily
composio add perplexityai
composio add googledocs

```

Edit .env file with the necessary environment variables.
(you can use the .env.example file as a reference)

Run the agent:
```
python main.py
```