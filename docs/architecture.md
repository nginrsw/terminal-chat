# Project Architecture / Arsitektur Proyek

## Overview / Ringkasan

**EN:**
This project is a terminal-based chat client that communicates with OpenRouter's LLM API. It is designed for simplicity, modularity, and easy extensibility.

**ID:**
Proyek ini adalah chat client berbasis terminal yang terhubung ke API LLM OpenRouter. Dirancang agar sederhana, modular, dan mudah dikembangkan.

## Components / Komponen

- `src/main.py`: Main application loop. Handles user input, output, and chat history. Calls the OpenRouter API.
- `requests`: For HTTP communication with OpenRouter.
- `dotenv`: Loads API key from `ENV/.env`.
- `nginr_config.yaml`: Stores model and configuration (can be customized).
- `tests/test_main.xr`: Automated test for the chat loop.

## Design Principles / Prinsip Desain

- **Modular structure:** Code is separated into `src/` and `tests/` directories.
- **Environment isolation:** Uses `ENV/` for virtual environment and secrets.
- **Extensible:** Easy to add new CLI commands, logging, or even a GUI/web API in the future.
- **Configuration:** Model and provider can be changed via `nginr_config.yaml` or command-line (future).

---

- **Struktur modular:** Kode dipisah antara `src/` dan `tests/`.
- **Lingkungan terisolasi:** Menggunakan `ENV/` untuk virtual environment dan rahasia.
- **Mudah dikembangkan:** Mudah menambah fitur CLI, logging, atau bahkan GUI/web API.
- **Konfigurasi fleksibel:** Model/provider bisa diubah lewat `nginr_config.yaml` atau argumen command-line (nanti).

---

### [2025-06-09] Update: Configuration Handling

- All configuration (model, provider, temperature, top_p, max_tokens) is now loaded only from `nginr_config.yaml`.
- The main loop now prints a separator (`---`) before every user input and bot reply for better readability.
- No more config fallback in code; missing config will raise an error.

---