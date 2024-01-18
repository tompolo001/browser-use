<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./static/browser-use-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="./static/browser-use.png">
  <img alt="Browser Use Logo" src="./static/browser-use.png" width="full">
</picture>

<h1 align="center">Enable AI to Control Your Browser 🤖</h1>

[![Stars](https://img.shields.io/github/stars/org-name/browser-use?style=social)](https://github.com/org-name/browser-use/stargazers)
[![Community Chat](https://img.shields.io/discord/000000000000000000?color=7289DA&label=Community&logo=discord&logoColor=white)](#)
[![Cloud](https://img.shields.io/badge/Cloud-☁️-blue)](#)
[![Documentation](https://img.shields.io/badge/Documentation-📕-blue)](#)

🌐 A minimal and extensible framework to connect AI agents with the browser.

💡 Share what you're building or get inspired in the community chat.

☁️ No setup required — explore the <b>hosted version</b> instantly. <b>[Try the cloud ☁︎](#)</b>

---

## Quick Start

Install via pip (Python >= 3.11):

```bash
pip install browser-use
```

For memory functionality (Python < 3.13 required for compatibility):

```bash
pip install "browser-use[memory]"
```

Install Browser Patch:

```bash
patchright install chromium
```

Launch an agent:

```python
from langchain_openai import ChatOpenAI
from browser_use import Agent
import asyncio
from dotenv import load_dotenv
load_dotenv()

async def main():
    agent = Agent(
        task="Compare the price of different AI models",
        llm=ChatOpenAI(model="gpt-4o"),
    )
    await agent.run()

asyncio.run(main())
```

Add the required keys to your `.env`:

```env
OPENAI_API_KEY=
ANTHROPIC_API_KEY=
AZURE_OPENAI_ENDPOINT=
AZURE_OPENAI_KEY=
GEMINI_API_KEY=
DEEPSEEK_API_KEY=
GROK_API_KEY=
NOVITA_API_KEY=
```

For full configuration and model support, refer to the [documentation 📕](#).

---

## UI Testing

Try out the optional UI:

- [Web UI Repository](#)
- Or run the demo:

```bash
uv pip install gradio
python examples/ui/gradio_demo.py
```

---

## Demo Examples

🛒 **Task:** Add grocery items to cart and proceed to checkout  
📎 **Automation Prompt:** Add latest LinkedIn follower to CRM leads  
🧑‍💻 **Job Search Prompt:** Scan CV, find relevant jobs, and apply  
📄 **Writing Prompt:** Draft a letter in a document editor and save as PDF  
🔍 **Model Discovery:** Search and sort AI models by license and popularity

For more examples, check the [examples](./examples) folder.

---

## Vision

A world where you tell your browser what to do—and it does it.

---

## Roadmap

### Agent Improvements

- [ ] Smarter memory (summarization, compression, etc.)
- [ ] Improved planning and task context
- [ ] Lower token usage

### DOM Extraction

- [ ] Handle complex elements (dropdowns, datepickers)
- [ ] Enhanced state extraction for UI logic

### Task Re-Execution

- [ ] Fallback handling
- [ ] Workflow templating
- [ ] Export to automation script

### Dataset & Benchmarking

- [ ] Public datasets for testing agents
- [ ] Benchmark various models
- [ ] Fine-tuned models for UI tasks

### User Experience

- [ ] Human-in-the-loop control
- [ ] Better visual outputs (GIFs, recordings)
- [ ] More interactive demos

---

## Contributing

All contributions are welcome!  
Open issues for bugs or features, or submit a PR.

Documentation lives in the `/docs` folder.

---

## Local Development

For development setup instructions, refer to the [developer guide 📕](#).

> ⚠️ The `main` branch contains the latest development code. For production use, install a [tagged release](https://github.com/org-name/browser-use/releases).

---

## Licensing

This project is open-sourced under the MIT license.

---

<div align="center">
Built with ❤️ by the open-source community
</div>
