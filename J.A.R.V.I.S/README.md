# Prompt Engineering Chatbot

This project is a submission for the AI Bootcamp Week 2. It demonstrates how prompts can change the quality and style of an LLM's responses, while incorporating advanced functionality like Model A/B Testing and Action Intents.

## Features

- **Multi-Model Support**: Switch seamlessly between Google Gemini 1.5 Flash, OpenAI GPT-4o models, and Llama 3 (via Groq API).
- **Prompt Modes**: Experience how different system instructions change the LLM's behavior. Modes include:
  - Explain Like I'm 5
  - Professional Rewrite
  - Teacher Mode
  - Sarcastic Robot
  - Custom (write your own system instructions)
- **Model A/B Arena**: Test two different LLMs side-by-side with the exact same prompt and vote on the winner.
- **Action Intents**: The chatbot detects when you want to perform an action (e.g., "Show me a youtube video about machine learning") and automatically opens the relevant URL in your browser.
- **Prompt Evaluator**: A dedicated meta-mode where the LLM analyzes and scores your prompt instead of answering it, helping you become a better prompt engineer.
- **Streaming & Memory**: Enjoy ChatGPT-like streaming responses and full session memory/context.

## Setup Instructions

1. Ensure you have Python installed.
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Copy the `.env.example` to `.env` and fill in your API keys:
   ```bash
   cp .env.example .env
   ```
   *Note: You do not need to fill in all keys. The app will only enable the models for which you provide keys.*
4. Run the Streamlit application:
   ```bash
   streamlit run main.py
   ```

## Prompt Engineering Concepts Explored

This project highlights several key prompt engineering concepts:
- **System Prompting**: Setting the persona, constraints, and tone of the model before providing the user query.
- **Prompt Evaluation**: Using an LLM to critique and rewrite prompts based on best practices.
- **Function Calling / Intent Detection**: Using an LLM to parse a query, output structured JSON, and trigger external actions (like opening a browser). 
- **Model Evaluation**: Using the Side-by-Side arena to understand how different models react to the exact same prompt and system instructions.
