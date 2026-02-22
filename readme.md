# Building a Simple MCP Server in Python

This project is a simple Task Tracker server built using the [Model Context Protocol (MCP)](https://modelcontextprotocol.io/) and the [FastMCP](https://gofastmcp.com/) framework. It follows the tutorial from [Machine Learning Mastery](https://machinelearningmastery.com/building-a-simple-mcp-server-in-python/).

## Project Overview

The project implements an MCP server that manages a simple task list. It demonstrates the three core primitives of MCP:
- **Tools**: Executable functions for the AI to perform actions.
- **Resources**: Read-only data access for the AI.
- **Prompts**: Templates to guide AI interactions.

## Features

### 🛠 Tools
- `add_task(title, description)`: Adds a new task to the in-memory list.
- `complete_task(task_id)`: Marks a specific task as completed.
- `delete_task(task_id)`: Removes a task from the list.
- `list_all_tasks()`: Returns a formatted list of all tasks.

### 📄 Resources
- `tasks://all`: Provides a formatted view of all current tasks.
- `tasks://pending`: Provides a view of only the pending tasks.

### 💡 Prompts
- `task_summary_prompt`: A guided prompt for the AI to analyze and summarize the task list, including progress assessment and suggested actions.

## Getting Started

### Prerequisites
- Python 3.10 or later.
- Virtual environment (recommended).

### Installation

1. Create and activate a virtual environment:
   ```powershell
   python -m venv venv
   .\venv\Scripts\Activate.ps1
   ```

2. Install dependencies:
   ```powershell
   pip install -r requirements.txt
   ```

## Running the Project

### Start the Server
Run the server locally:
```powershell
fastmcp run task_server.py
```
Or simply run the script:
```powershell
python task_server.py
```

### Test the Server
You can use the included test client to verify the server's functionality:
```powershell
python test_client.py
```

## Project Structure
- `task_server.py`: The main MCP server implementation.
- `test_client.py`: A client script to test the tools and resources of the local server.
- `requirements.txt`: List of required Python packages.
- `Steps.me`: Quick reference for setup commands.
- `t1.py`: An example of connecting to an external FastMCP client.

## Reference
This project is based on the tutorial: [Building a Simple MCP Server in Python](https://machinelearningmastery.com/building-a-simple-mcp-server-in-python/)
