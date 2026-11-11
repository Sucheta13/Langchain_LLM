# Langchain_LLM

Small LangChain demos that serve and call LLMs two ways: through an API and through chat apps.

## Contents

- `api/app.py` – FastAPI + LangServe server with an `/essay` route (OpenAI) and a `/poem` route (local Llama 2 via Ollama).
- `api/client.py` – Streamlit client that calls those routes.
- `chatbot/app.py` – Streamlit chatbot using OpenAI (`gpt-3.5-turbo`).
- `chatbot/localama.py` – Streamlit chatbot using local Llama 2 through Ollama.
- Optional LangSmith tracing.

## Setup

```bash
pip install -r requirements.txt
```

Create a `.env` file with your keys:

```
OPENAI_API_KEY=...
LANGCHAIN_API_KEY=...
```

For the local model, install [Ollama](https://ollama.com) and run `ollama pull llama2`.

## Run

```bash
python api/app.py                  # start the API on localhost:8000
streamlit run api/client.py        # client UI
streamlit run chatbot/app.py       # OpenAI chatbot
streamlit run chatbot/localama.py  # Llama 2 chatbot
```

## Tech

Python, LangChain, LangServe, FastAPI, Streamlit, OpenAI API, Ollama
