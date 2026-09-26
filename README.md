# airline-ai-multimodal-assistant

A skeleton for a multi-modal AI customer support assistant for an airline ("FlightAI"), built with the OpenAI Python client and Gradio. Extends the basic tool-calling assistant with:

- A `get_ticket_price` tool backed by SQLite, so fare answers use real data.
- Image generation (`gpt-image-1-mini`) to illustrate a destination city.
- Voice output (`gpt-4o-mini-tts`) so the assistant talks back.
- A custom `gr.Blocks` UI instead of the standard `ChatInterface`.

## Requirements

- Python 3.12+
- [uv](https://docs.astral.sh/uv/) for dependency/environment management
- An OpenAI API key

## Setup

1. Clone the repo and `cd` into it.
2. Install dependencies into an isolated `.venv` (created automatically):
   ```
   uv sync
   ```
3. Copy `.env.example` to `.env` and fill in `OPENAI_API_KEY`.

## Usage

Open `airline_multimodal_assistant.ipynb` in Jupyter, select the project's `.venv` as the kernel, and build out the assistant from there:

```
uv run jupyter notebook airline_multimodal_assistant.ipynb
```
