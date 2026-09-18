# Behind the Scenes of Data Center Project

**Mastering Control, Management, and Continuous Monitoring from Ground to Cloud**
LinkedIn Live · Project Management Prodigy · Jumat, 18 September 2026 · 20.00 WIB
Pembicara: Masron Hutabalian & Abdul Kausar · Operator slide: Abdul

> Semua contoh project dan data di sesi ini fiktif dan dibuat untuk demonstrasi.

Satu deck untuk sesi 1 jam. Bahasa utama Bahasa Indonesia; istilah teknis yang lazim di proyek tetap dalam bahasa Inggris. Setiap informasi hanya disimpan di **satu** tempat.

## Susunan Sesi

| Menit | Slide | Bagian | Pembicara |
|---|---|---|---|
| 0:00 – 2:00 | 1–3 | Pembuka, agenda, disclaimer | Masron (& Abdul) |
| 2:00 – 21:30 | 4–16 | Bagian 1 — proyek data center dari ground sampai cloud: ekosistem, interface, control loop, lifecycle & commissioning, monitoring, satu activity | Masron |
| 21:30 – 48:15 | 17–30 | Bagian 2 — informasi, knowledge, perkenalan Obsidian (slide 21), asal vault demo dan cara memulai (slide 23), demo Obsidian (slide 24), AI dan demo Claude (slide 26–27) | Abdul |
| 48:15 – 60:00 | 31 | Tanya jawab | Masron & Abdul |

## Isi Folder

| Folder | Isi | Untuk |
|---|---|---|
| `1_Presentasi/` | `Behind-the-Scenes-of-Data-Center-Project.pptx` (31 slide, speaker notes per pembicara di dalamnya), PDF-nya, `Poster-Square.png` | Presentasi. PDF hanya cadangan — tombol di slide tidak aktif di PDF. |
| `2_Demo/` | Vault `Planning-Knowledge-Demo-ID`, `Demo-Launcher.html`, `Panduan-Demo.md`, `Offline-Demo.pdf` | Demo Obsidian dan Claude serta cadangannya |
| `3_Persiapan/` | `Runbook-dan-Checklist.md`, `Q&A.md` | Waktu per slide, tugas operator, latihan, checklist LinkedIn Live, tanya jawab |

## Mulai dari Sini

1. **Masron:** baca dan sesuaikan speaker notes slide 1–16. Isi bagian 1 disusun sebagai draft dari catatan data center di vault.
2. **Sekali saja (laptop operator):** buka Obsidian → *Open folder as vault* → pilih **hanya** `2_Demo/Planning-Knowledge-Demo-ID`.
3. Siapkan Claude dan coba semua tombol demo: `2_Demo/Panduan-Demo.md`.
4. Waktu, tugas operator dan checklist hari H: `3_Persiapan/Runbook-dan-Checklist.md`.

> Jangan pisahkan `1_Presentasi/` dan `2_Demo/`: tombol *Salin prompt* di slide 26 membuka `../2_Demo/Demo-Launcher.html`. Kalau dipindah, pindahkan seluruh folder sekaligus.
> Folder versi Inggris lama memiliki vault bernama `Planning-Knowledge-Demo`. Karena itu vault di folder ini sengaja diberi nama unik `Planning-Knowledge-Demo-ID`, supaya tombol di slide selalu membuka vault yang benar.

## Di Mana Setiap Informasi Berada

| Informasi | Satu-satunya tempat |
|---|---|
| Isi slide dan speaker notes kedua pembicara | PPTX |
| Project Alpha: activity, constraint, issue, decision, lesson | Vault → `04 Project Alpha` |
| Pengetahuan planning, data center (lifecycle, commissioning L1–L5, IST, handover), lessons learned | Vault → folder `00`–`05` |
| Sumber dan referensi (REF-xxx) | Vault → `06 Referensi` |
| Aturan untuk AI | Vault → `AGENTS.md` (`CLAUDE.md` hanya memuatnya) |
| Template hasil AI dan tempat Claude menyimpan note | Vault → `07 Template/Template Review Critical Path.md` → hasilnya di `08 AI Output/` |
| Prompt demo Claude | `2_Demo/Demo-Launcher.html` (juga tampil di slide 26) |
| Langkah demo, prompt tes dan cadangan, cara pemulihan | `2_Demo/Panduan-Demo.md` |
| Jawaban AI yang direkam dan screenshot cadangan | `2_Demo/Offline-Demo.pdf` |
| Waktu per slide, tugas operator, checklist LinkedIn Live | `3_Persiapan/Runbook-dan-Checklist.md` |
| Jawaban Q&A (bagian Obsidian & AI) | `3_Persiapan/Q&A.md` |

## Kerahasiaan

Sesi ini **publik**. Folder ini tidak berisi informasi proyek nyata. Project Alpha — termasuk semua activity, tanggal (tahun 2030), quantity, issue dan decision — adalah data sintetis. Saat share layar, pastikan tidak ada jendela, file, vault atau percakapan Claude lain yang berisi data proyek nyata.
