# Visual Code Server

`Visual Code Server` is a Python-based project that uses the `FastMCP` framework to fetch and visualize source code from GitHub repositories. It provides a simple interface to extract code and generate visual representations of its structure.

## Features

- Fetch source code from GitHub repositories.
- Visualize the structure of the code in a readable format.
- Built using `FastMCP` for efficient server-side processing.
- Asynchronous HTTP requests powered by `httpx`.

## Requirements

- Python 3.11 or higher
- Dependencies listed in `pyproject.toml` and `uv.lock`

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/habibsifat/MCP-Server.git
   cd MCP-Server
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Running the Server

To start the `FastMCP` server, run the following command:
```bash
python visual.py
```

The server will listen for requests and process GitHub URLs to fetch and visualize code.

### Example

To visualize code from a GitHub repository, use the `visualize_code` tool:
```python
# Example usage in Python
from visual import visualize_code

url = "https://github.com/user/repo/blob/main/file.py"
result = await visualize_code(url)
print(result)
```

### Running the Main Script

You can also run the `main.py` script to see a simple greeting:
```bash
python main.py
```

### Project Structure

- **`visual.py`**: Main server script that fetches and visualizes code.
- **`main.py`**: A simple entry point script.
- **`pyproject.toml`**: Project metadata and dependencies.
- **`uv.lock`**: Lock file for dependency versions.
- **`README.md`**: Documentation for the project.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.


## Acknowledgments

- Built with [FastMCP](https://github.com/fastmcp) and [httpx](https://www.python-httpx.org/).
