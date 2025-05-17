# 🧠 Small OpenAI Agent with LangChain and Calculator Tool

This is a minimal example of an interactive AI assistant built using the OpenAI API and [LangChain](https://www.langchain.com/). The agent is capable of chatting with the user and performing basic arithmetic using a custom tool.

## 🚀 Features

- Interactive chatbot interface via the terminal  
- Uses OpenAI's `ChatOpenAI` model  
- Supports a simple calculator tool (addition)  

## 📁 Project Structure

```
.
├── agent.py           # Main Python script
├── .env               # Environment variables (not committed)
└── .env.example       # Sample environment variable template
```

## 🛠️ Requirements

- Python 3.8+
- [uv](https://github.com/astral-sh/uv) (ultra-fast Python package manager)
- OpenAI API key

## 📦 Installing Dependencies

Install `uv` if you haven't already. You can install it using homebrew. For other installation alternatives check the documentation [here](https://docs.astral.sh/uv/getting-started/installation/):

```bash
brew install uv
```

Install the required dependencies:

```bash
uv add langchain langgraph langchain-openai python-dotenv
```

> `uv` automatically uses a virtual environment under the hood. You don't need to create one manually.

## 🔐 Setup

Create a `.env` file in the root directory with your OpenAI API key:

```
OPENAI_API_KEY=your_openai_api_key_here
```

You can copy the example template:

```bash
cp .env.example .env
```

## 🧪 Usage

Run the agent from your terminal:

```bash
uv run main.py
```

Example interaction:

```bash
Welcome! I am your AI assistant. Type 'quit' to exit.
You can ask me to perform calculations or chat with me.

You: Can you add 5 and 3?

Assistant: The sum of 5.0 and 3.0 is 8.0
```

## 🧰 Tools

### Calculator

A simple tool that takes two floats and returns their sum.

```python
@tool
def calculator(a: float, b: float) -> str:
    ...
```

## 📌 Notes

- The assistant uses streaming to print responses as they are generated.
- This project serves as a foundation and can be extended with more tools, memory, or custom prompts.

## 📄 License

MIT – free to use, modify, and distribute.