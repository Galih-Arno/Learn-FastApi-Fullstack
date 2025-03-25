# Belajar Fullstack FastAPI :books:

[FastAPI](https://fastapi.tiangolo.com) adalah kerangka kerja web yang modern, cepat (berkinerja tinggi) untuk membangun API dengan Python berdasarkan petunjuk tipe Python standar.

## :bulb: Fitur utama:

- Fast: Kinerja tinggi setara dengan NodeJS dan Golang.
- Fast to Code.
- Fewer bugs: Mengurangi 40% kesalahan oleh pengembang.
- Intuitive: Penyelesaian yang cepat untuk men-debug.
- Easy.
- Short: Meminimalkan duplikasi kode.
- Robust: Dapatkan kode siap produksi dan dokumentasi interaktif otomatis.
- Standard-based: Sangat kompatibel dengan OpenAPI dan Skema JSON.

## Typer - FastAPI CLI :globe_with_meridians:

[Typer](https://typer.tiangolo.com) merupakan adik dari FastAPI yang dimaksudkan untuk menjadi FastAPI CLI. 
> Baca dokumentasi `[Typer](https://typer.tiangolo.com)`.

## Persyaratan :label:

FastAPI berdiri pada:
- [Starlette](https://www.starlette.io) untuk komponen web.
- [Pydantic](https://docs.pydantic.dev/latest) untuk bagian data.

## Instalasi :round_pushpin:

Buat dan aktifkan [virtual environment](https://fastapi.tiangolo.com/virtual-environments) lalu instal FastAPI:

```
    pip install "fastapi[standard]"
```

> Catatan: Pastikan Anda memasukkan `"fastapi[standard]"` dalam tanda kutip untuk memastikannya berfungsi di semua terminal.

## Contoh 

- Buat file 'main.py' :

```python
    from typing import Union
    from fastapi import FastAPI

    app = FastAPI()

    @app.get("/")
    def read_root():
        return {"Hello": "World"}
    
    @app.get("/item/item{item_id}")
    def read_item(item_id: int, q: Union[str, None] = None):
        return {"item_id": item_id, "q": q}
```

- Jalankan server :

```bash
    $ fastapi dev main.py
    ╭────────── FastAPI CLI - Development mode ───────────╮
    │                                                     │
    │  Serving at: http://127.0.0.1:8000                  │
    │                                                     │
    │  API docs: http://127.0.0.1:8000/docs               │
    │                                                     │
    │  Running in development mode, for production use:   │
    │                                                     │
    │  fastapi run                                        │
    │                                                     │
    ╰─────────────────────────────────────────────────────╯

    INFO:     Will watch for changes in these directories: ['/home/user/code/awesomeapp']
    INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
    INFO:     Started reloader process [2248755] using WatchFiles
    INFO:     Started server process [2248757]
    INFO:     Waiting for application startup.
    INFO:     Application startup complete.

```

> Perintah `fastapi dev` untuk membaca file `main.py`, kemudian mendeteksi aplikasi FastAPI didalamnya, dan memulai server menggunakan Uvicorn. Secara default, `fastapi dev` akan dimulai dengan auto-reload yang diaktifkan untuk pengembangan lokal.

- Periksa dan buka browser di `http://127.0.0.1:8000` atau localhost. Anda juga bisa menambahkan parameter pada browser `http://127.0.0.1:8000/items/1`.

## Dokumentasi

Anda dapat membaca dokumentasi resminya di [FastAPI](https://fastapi.tiangolo.com).

### Referensi

- [Typer](https://typer.tiangolo.com)
- [Starlette](https://www.starlette.io)
- [Pydantic](https://docs.pydantic.dev/latest)
- [FUll-Stack FastAPI Template](https://fastapi.tiangolo.com/id/project-generation)

## :phone: Kontak
- Email: galihgratiaarno@gmail.com
- Instagram: [@g9.arno](https://instagram.com/g9.arno)
- LinkedIn: [Galih Gratia Arno](www.linkedin.com/in/galihgratiaarno)