WORK IN PROGRESS - USE WITH CAUTION - Windows

# MCP PDF Tools Server

An MCP (Model Context Protocol) server that provides PDF manipulation tools. This server allows LLMs to perform operations like merging PDFs and extracting pages through the Model Context Protocol.

## Features

- Merge multiple PDF files into a single PDF
- Merge multiple PDF files into a single PDF in user specified order
- Extract specific pages from a PDF file
- Search PDFs *filesystem search or Everything search works better than this*
- Find related PDFs based on text extraction and regex pattern matching from a target input PDF

## Installation

```bash
# Create and activate virtual environment
uv venv
.venv\Scripts\activate

# Install the package
uv pip install -e .

## Usage with Claude Desktop

Add this to your Claude Desktop configuration file (claude_desktop_config.json):

```json
{
    "mcpServers": {
        "pdf-tools": {
            "command": "uv",
            "args": [
                "--directory",
                "PATH_TO/pdf-tools",
                "run",
                "pdf-tools"
            ]
        }
    }
}

