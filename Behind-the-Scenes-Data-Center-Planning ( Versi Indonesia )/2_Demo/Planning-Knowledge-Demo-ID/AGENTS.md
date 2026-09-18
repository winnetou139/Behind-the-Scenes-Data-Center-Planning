# AGENTS.md — Aturan untuk AI yang Bekerja di Vault Ini

Folder ini adalah **vault Obsidian**: note Markdown biasa yang membentuk knowledge base pribadi seorang planner tentang
project planning, delivery data center, dan project controls, ditambah satu project **fiktif** bernama Project Alpha.
Claude membaca `CLAUDE.md`, yang meng-import file ini, jadi Claude mengikuti aturan ini.

## 1. Menjawab pertanyaan

1. **Jawab dari vault terlebih dahulu.** Cari dan baca note yang relevan sebelum menjawab.
2. **Kutip sumbermu.** Setelah setiap poin, kutip note asalnya sebagai `[[Note Name]]`. Untuk fakta Project Alpha,
   kutip juga ID catatannya (misalnya `A-3030`, `C-003`, `D-004`).
3. **Pisahkan knowledge dari vault dengan pengetahuan umum.** Kalau vault tidak membahas sesuatu, katakan
   **"Tidak ada di vault"** dan beri label pada pengetahuan umum yang kamu tambahkan. Jangan pernah menyajikan
   pengetahuan umum seolah-olah berasal dari note.
4. **Sebutkan kalau sebuah note dangkal atau tidak membahasnya.** Celah seperti ini informasi yang berguna bagi owner vault ini.
5. **Project Alpha itu fiktif.** Sebutkan hal ini setiap kali kamu memakai datanya.
6. **Jangan mengarang referensi.** Sumber diidentifikasi dengan REF-ID; masing-masing punya note di `06 Referensi/`.
7. **Jangan pakai `07 Template/`, `08 AI Output/` atau `09 Inbox/` sebagai sumber.** Isinya template, hasil AI sebelumnya,
   dan catatan cepat yang belum direview. Jawab dari note konsep, lesson learned, dan note project.
8. Jawaban singkat dan terstruktur (poin-poin atau tabel pendek).
9. Jawab dalam Bahasa Indonesia. Istilah teknis yang lazim dipakai dalam bahasa Inggris (schedule, critical path, float, constraint, readiness, recovery, dll.) tetap dalam bahasa Inggris.

## 2. Letak isi vault

| Folder | Isi |
|---|---|
| `00 Beranda/` | Titik awal (`Beranda Pengetahuan Planning`), informasi vs knowledge |
| `01 Planning & Scheduling/` | Note konsep: logic, critical path, float, baseline, lookahead, constraint, delay, recovery, acceleration |
| `02 Data Center/` | Lifecycle project data center, commissioning (L1–L5), IST, handover |
| `03 Project Controls/` | Forecasting, schedule quality check |
| `04 Project Alpha/` | Tampilan project fiktif (schedule, constraint, weekly planning, issue, keputusan, lesson learned) |
| `05 Lessons Learned/` | Lesson learned evergreen yang digeneralisasi dari pengalaman |
| `06 Referensi/` | Kartu referensi yang dikutip di slide |
| `07 Template/` | `Template Review Critical Path` — struktur dan aturan wajib untuk hasil AI yang disimpan |
| `08 AI Output/` | Hasil AI yang disimpan ke vault, menunggu review planner |
| `09 Inbox/` | Catatan cepat dari lapangan yang belum dirapikan |

Note konsep memakai bagian yang sama: Definisi · Kenapa Penting · Sudut Pandang Planner · Contoh Praktis ·
Kesalahan yang Sering Terjadi · Konsep Terkait · Referensi. Poin-poin di **Konsep Terkait** menjelaskan *kenapa* note saling terkait —
pakai itu saat ditanya bagaimana konsep-konsep saling terhubung.

## 3. Menyimpan jawaban ke vault

Kalau user meminta jawabannya **disimpan** ke vault memakai sebuah template:

1. Baca dulu template yang disebut user di `07 Template/`. Ikuti strukturnya **persis**: properties YAML, callout
   peringatan, urutan bagian, dan kolom tabel. Ikuti semua aturan di blok komentar `%% … %%` template itu, tapi
   **jangan salin blok komentar** ke note hasil.
2. Baca **hanya** note yang disebut di properties `sumber` dan aturan template. Jangan mencari ke note lain.
3. Isi hanya dengan data dari note sumber. Jangan menambah opini, saran, atau pengetahuan umum.
4. Simpan sebagai **satu** file di `08 AI Output/`:
   - untuk `Template Review Critical Path`: nama file `Review Critical Path - <data date>.md` (data date dari note sumber);
   - untuk template lain: `<Judul singkat> - <YYYY-MM-DD hari ini>.md`.
   Kalau file dengan nama itu sudah ada di `08 AI Output/`, timpa file itu.
5. Isi `prompt` dengan pertanyaan user apa adanya. Biarkan `reviewed: false` dan bagian Catatan Review Planner kosong.
6. **Jangan mengubah file lain apa pun.**
7. Di chat, **jangan ulangi isi note.** Cukup tulis nama file yang dibuat dan satu kalimat ringkasan dari bagian Ringkasan.

## 4. Aturan edit

- **Default-nya read-only.** Hanya buat file kalau user secara eksplisit memintanya (lihat bagian 3). Jangan pernah mengedit note yang sudah ada.
- **Jangan pernah edit** `.obsidian/`.
- **Jangan pernah edit konten yang di-generate:** bagian FACTS pada note di `04 Project Alpha/` dan note di `06 Referensi/`.
  Kalau sebuah fakta terlihat salah, laporkan — hanya presenter yang mengubah fakta project.
- Note hasil AI selalu disimpan di `08 AI Output/` dan hanya memberi link ke note yang sudah ada.
- Pakai wikilink (`[[Note Name]]`) dan letakkan properties YAML di bagian paling atas file.

## 5. Kerahasiaan

- Jangan pernah menambahkan nama project, client, tanggal, kuantitas, orang, atau dokumen yang nyata ke vault ini.
- Semua contoh project harus memakai Project Alpha yang fiktif.
