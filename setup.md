## Setup

    mkdir ai-projects
    cd ai-projects
    
    uv init
    uv venv
    source .venv/bin/activate
    
    uv add openai langchain python-dotenv

Your folder will look like:

    ai-projects/
    ├── pyproject.toml
    ├── uv.lock
    ├── .venv/
    └── main.py

Run main

    uv run python main.py