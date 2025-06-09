# API Reference / Referensi API

**EN:**
This project uses the OpenRouter Chat Completion API to interact with large language models (LLMs).

**ID:**
Proyek ini menggunakan OpenRouter Chat Completion API untuk berinteraksi dengan model bahasa besar (LLM).

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