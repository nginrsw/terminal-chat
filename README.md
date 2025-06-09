# Terminal-chat

A simple terminal-based chat application powered by the [nginr-preprocessor](https://github.com/nginrsw/nginr). This project allows you to interact with AI models directly from your terminal.

## Features
- Chat with AI models in your terminal
- Command-based interface
- Easy to extend and customize

## Quick Start

### Prerequisites
- Python 3.12 or later
- `nginr` installed in your environment (see [requirements.txt](requirements.txt))

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/nginrsw/terminal-chat.git
   cd terminal-chat
   ```
2. (Optional) Create and activate a virtual environment:
   ```bash
   python3 -m venv ENV
   source ENV/bin/activate
   ```
   > you can use any virtual environment tools you have / favorite
   > 
   > Ignore this command to install all packages from requirements.txt globally (without a virtual environment).
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Usage
To start the chat application, run:
```bash
nginr src/main.xr
```

To run the tests:
```bash
nginr tests/test_main.xr
```

## Configuration Example
This project uses a YAML config file (`nginr_config.yaml`) to set the model and other parameters. By default, it uses the Deepseek model via OpenRouter:

```yaml
model: deepseek/deepseek-r1-0528:free
provider: openrouter
temperature: 1.0
top_p: 1.0
max_tokens: 1024
```

You can change these values in `nginr_config.yaml` to use a different model or adjust parameters as needed.

## Project Structure
- `src/` : Source code for the chat application
- `tests/` : Test scripts
- `docs/` : Documentation (API, architecture, developer notes)
- `requirements.txt` : Python dependencies

## Contributing
Contributions are welcome!

## License
This project is licensed under the [MIT License](LICENSE).
