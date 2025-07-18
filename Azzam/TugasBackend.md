# 📚 Tugas FastAPI - CRUD API (Mirip Catatan API)

## ✅ Tugas Azzam Maulana Dzakwan: API To-do List (Tugas Harian)

### Deskripsi

Buatlah REST API untuk mencatat dan mengelola tugas harian. Setiap tugas memiliki status dan tanggal deadline.

### Struktur Data Tugas [Jika ditambahkan lagi fieldnya akan mendapat tambahan point]

| Kolom              | Tipe Data                               |
| ------------------ | --------------------------------------- |
| `id`               | Integer                                 |
| `judul`            | String                                  |
| `deskripsi`        | String                                  |
| `status`           | String (“rencana”, “sedang”, “selesai”) |
| `tanggal_deadline` | Date                                    |

### Endpoint yang Wajib Dibuat

- `GET /tugas` → Ambil semua tugas
- `POST /tugas` → Tambah tugas baru
- `PATCH /tugas/{id}` → Ubah sebagian data (misalnya hanya `status`)
- `DELETE /tugas/{id}` → Hapus tugas berdasarkan ID

### Ketentuan

- Gunakan `Pydantic` untuk validasi input/output.
- Gunakan `SQLAlchemy` untuk koneksi dan model ORM.
- Pisahkan folder `models/`, `schemas/`, `routes/`, dan `services/`.

### Nilai Plus jika:

1. Tambahkan fitur **soft delete**, **restore**, **force delete** (gunakan kolom `deleted_at`).
2. Tambahkan fitur **pagination** → pada ambil semua data buku.
3. Tambahkan fitur pencarian tugas berdasarkan:
   - `status`
   - `tanggal_deadline` (misalnya: tampilkan semua tugas yang deadline-nya hari ini)

---

## 🛠️ Petunjuk Umum

- Gunakan virtual environment (`venv`).
- Install library: `fastapi`, `uvicorn`, `sqlalchemy`, `pydantic`, `alembic`.
- Dokumentasi interaktif otomatis tersedia di `http://localhost:8000/docs`.

### Struktur Folder yang Disarankan

```

Azzam/backend/
├── app/
│   ├── main.py
│   ├── models/
│   ├── schemas/
│   ├── routes/
│   ├── services/
│   └── database/
├── alembic/
├── .env
├── requirements.txt
└── README.md

```

## 🧠 Kriteria Penilaian

| No  | Kategori                        | Aspek                                                           | Bobot |
| --- | ------------------------------- | --------------------------------------------------------------- | ----- |
| 1   | Penulisan Kode & Error Handling | Konsistensi struktur, clean code, penggunaan try-except-finally | 15%   |
| 2   | Backend API                     | CRUD lengkap, struktur modular, endpoint sesuai RESTful         | 65%   |
| 3   | Debugging & Pengujian           | Unit test / Swagger / dokumentasi untuk debugging & validasi    | 10%   |
| 4   | Presentasi Proyek               | Menjelaskan ide, alur, serta tantangan proyek                   | 10%   |

---

## 🏆 Ketentuan Nilai

| No  | Skor Akhir | Nilai | Keterangan                  |
| --- | ---------- | ----- | --------------------------- |
| 1   | 86 – 100   | A     | Sangat Baik / Istimewa      |
| 2   | 71 – 85    | B     | Baik                        |
| 3   | 56 – 70    | C     | Cukup                       |
| 4   | 41 – 55    | D     | Kurang                      |
| 5   | 0 – 40     | E     | Sangat Kurang / Belum Lulus |

> 💡 Catatan:
>
> - Backend API (65%) mendapat bobot tertinggi karena merupakan fokus utama mini proyek ini.
> - Debugging dan Presentasi (20%) penting untuk menunjukkan pemahaman dan komunikasi kerja.
> - Penulisan Kode & Error Handling (15%) penting karena:

```bash
    - **Konsistensi Struktur** → Mempermudah kolaborasi tim, karena semua developer bisa memahami alur dan struktur proyek dengan cepat. Ini sangat penting di proyek skala besar.
    - **Clean Code** → Membuat kode mudah dibaca, dipelihara, dan dikembangkan. Kode yang bersih mengurangi kemungkinan munculnya bug di masa depan.
    - **try-except-finally** → Menghindari crash aplikasi ketika terjadi error tak terduga. Misalnya saat koneksi database gagal, file tidak ditemukan, atau input user salah. Pengguna tetap mendapatkan feedback yang jelas dan sistem tetap stabil.
```

---

## 🧰 Tools yang Direkomendasikan

- Python 3.13+
- FastAPI
- SQLAlchemy
- Alembic
- MySQL / XAMPP
- Postman / Swagger UI
- VSCode / PyCharm

---

## 📝 Petunjuk Penilaian

1. Tulis `README.md` proyek Anda secara informatif.
2. Sertakan diagram alur atau arsitektur jika memungkinkan.
3. Buat file dokumentasi endpoint (`openapi.json` atau link Swagger UI).
4. Lampirkan link video demo sebagai tugas presentasi.
5. Coding push di folder backend

---

Selamat mengerjakan! 🚀
