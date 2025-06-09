# Developer Notes / Catatan Pengembang

## Future Ideas / Ide Pengembangan
- Add `/reset` command to clear chat history
- Log all conversations to a `logs/` directory
- Add retry logic for timeouts or errors
- Use `argparse` to allow model/config selection via command-line
- Add color output using `colorama` for better UX

---
- Tambahkan perintah `/reset` untuk menghapus riwayat chat
- Simpan semua percakapan ke folder `logs/`
- Tambahkan mekanisme retry jika timeout/error
- Gunakan `argparse` agar model/konfigurasi bisa dipilih via command-line
- Tambahkan warna output dengan `colorama` agar lebih nyaman

## Notes / Catatan
- The current model is rate-limited; consider caching long answers to reduce API calls
- Consider using `typer` or `rich` for enhanced CLI experience
- API key is loaded from `ENV/.env` (do not commit this file)
- Tests can be run with `nginr tests/test_main.xr`

---
- Model yang dipakai ada batasan rate-limit, sebaiknya cache jawaban panjang
- Bisa pakai `typer` atau `rich` untuk CLI yang lebih interaktif
- API key diambil dari `ENV/.env` (jangan di-commit ke repo)
- Tes bisa dijalankan dengan `nginr tests/test_main.xr`
