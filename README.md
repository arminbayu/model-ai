# model-ai

Model AI offline untuk aplikasi POS AkunQu, diunduh aplikasi sekali lalu
dipakai tanpa internet.

## siglip2-b32-q4-v1

Validasi foto barang Niaga Rakyat (foto harus sesuai judul barang).

| Berkas | Ukuran (byte) | SHA-256 |
|---|---|---|
| `siglip2_image_q4.onnx` | 75886583 | `281c5a69611ab4281a6166a0da10b325be5220ff1baff736a46f2a514e427e43` |
| `siglip2_text_q4.onnx` | 101883695 | `fd6a06593a50e628b8a4e6512f226366b94023a4531db623c8f9734af005cdec` |
| `siglip2_tokenizer.json` | 3184281 | `79d573125de64590ccf7990513b019c9b0e2b0c4cb9767ee50e3b943989ec6b9` |

Aplikasi mengunduh dari
`https://raw.githubusercontent.com/arminbayu/model-ai/main/siglip2-b32-q4-v1/`
dan menolak berkas yang SHA-256-nya tidak cocok dengan manifest di aplikasi.
Jangan mengganti berkas di folder ini; versi baru dibuat di folder baru.

Sumber: [google/siglip2-base-patch32-256](https://huggingface.co/google/siglip2-base-patch32-256),
lisensi Apache-2.0. Diekspor ke ONNX, kosakata teks dipangkas, dan bobot
MatMul dikuantisasi 4-bit dengan skrip `scripts/siglip2_*.py` di repo
pos-akunqu.
