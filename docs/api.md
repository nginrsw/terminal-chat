# API Reference / Referensi API

**EN:**
This project uses the OpenRouter Chat Completion API to interact with large language models (LLMs).

**ID:**
Proyek ini menggunakan OpenRouter Chat Completion API untuk berinteraksi dengan model bahasa besar (LLM).

---

### [2025-06-09] Update: Unified Configuration

- All model and API configuration (model, provider, temperature, top_p, max_tokens) are now loaded exclusively from `nginr_config.yaml`.
- No more default/fallback values in code. If a config key is missing, the app will raise a clear error.
- To change model or parameters, edit only `nginr_config.yaml`.
- See `src/main.xr` for details.

---

## Endpoint
```
POST https://openrouter.ai/api/v1/chat/completions
```

## Headers
- `Authorization: Bearer <API_KEY>`
- `Content-Type: application/json`

## Request Body Example / Contoh Request
```json
{
  "model": "deepseek/deepseek-r1-0528:free",
  "messages": [
    {"role": "user", "content": "Hello!"}
  ]
}
```

## Response Example / Contoh Response
```json
{
  "choices": [
    {
      "message": {
        "role": "assistant",
        "content": "Hi there! How can I help you today?"
      }
    }
  ]
}
```

## Usage in Code / Penggunaan di Kode
See `src/main.xr` for how the API is called using Python's `requests` library. The API key is loaded from the `.env` file in the `ENV/` directory.

Lihat `src/main.xr` untuk contoh pemanggilan API menggunakan library `requests` di Python. API key diambil dari file `.env` di folder `ENV/`.