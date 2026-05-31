# REST Notebook

Use Jupyter Notebooks as a REST client in VS Code, managed with [uv](https://github.com/astral-sh/uv).

## Setup

```sh
uv venv .venv
uv pip install jupyter httpx requests
```

Open `example_rest_client.ipynb` in VS Code and select `.venv` as the kernel.

## HTTP Client

Use either `httpx` or `requests` — both work well:

```python
import httpx
JSON(httpx.get("https://api.example.com/todos/1").raise_for_status().json())
```

```python
import requests
JSON(requests.get("https://api.example.com/todos/1").json())
```
