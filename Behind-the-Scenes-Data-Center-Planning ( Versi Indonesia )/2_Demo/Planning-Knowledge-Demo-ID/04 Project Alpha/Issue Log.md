---
type: project-view
domain: project-alpha
project: Project Alpha
fictional: true
tags:
- project-alpha
- fictional
data_date: 2030-04-08
---
# Issue Log

> [!warning] Data proyek fiktif
> Semua nama proyek, activity, tanggal, quantity, issue dan informasi proyek di Project Alpha adalah fiktif dan dibuat khusus untuk demonstrasi.

Bagian dari [[Gambaran Umum Project Alpha]]

| ID | Judul | Prioritas | Status | Owner | Dibuka | Activity | Constraint |
|---|---|---|---|---|---|---|---|
| I-001 | Rigging route ke Area A terhalang | High | Open | Main Contractor Site Manager | 2030-04-02 | [[Electrical Equipment Installation - Area A\|A-3030]] | C-003 |
| I-002 | Delivery generator mundur | Medium | Open | Procurement Lead | 2030-04-03 | A-2050, A-3080 | C-002 |
| I-003 | Layout CRAH bentrok (RFI-014) | Medium | Open | Design Consultant | 2030-04-03 | A-3070 | C-001 |
| I-004 | Kekurangan crew cable pulling | Medium | Open | Electrical Subcontractor | 2030-04-04 | A-3040 | C-008 |
| I-005 | EPMS points list belum disepakati | Medium | Open | BMS Contractor | 2030-04-04 | A-4040, A-5040 | C-011 |
| I-006 | Pintu panel UPS rusak saat receiving inspection | Low | Closed | Procurement Lead | 2030-03-30 | A-2030 | C-005 |

### I-001 — Rigging route ke Area A terhalang
Scaffold facade yang dipasang melintang di loading bay menutup satu-satunya rigging route yang praktis untuk LV switchboard dan UPS ke Area A. Lifting permit LP-07 masih pending.

- **Kategori:** Access / Logistik · **Prioritas:** High · **Status:** Open
- **Langkah berikut / penyelesaian:** Pemindahan bay scaffold dan review permit secara fast-track disepakati di rapat W13 (D-001; D-002).

### I-002 — Delivery generator mundur
Supplier generator menahan unit karena QA hold. Forecast delivery mundur.

- **Kategori:** Procurement · **Prioritas:** Medium · **Status:** Open
- **Langkah berikut / penyelesaian:** Terima keterlambatan dan monitor setiap minggu (D-005).

### I-003 — Layout CRAH bentrok (RFI-014)
Posisi unit CRAH bentrok dengan cable tray di atas di Data Hall 1. Perlu revisi layout.

- **Kategori:** Desain · **Prioritas:** Medium · **Status:** Open
- **Langkah berikut / penyelesaian:** Menunggu revisi layout dari Design Consultant.

### I-004 — Kekurangan crew cable pulling
Electrical Subcontractor hanya bisa konfirmasi 16 dari 24 electrician yang dibutuhkan saat puncak cable pulling.

- **Kategori:** Manpower · **Prioritas:** Medium · **Status:** Open
- **Langkah berikut / penyelesaian:** Contingency extended hours atau second shift sudah disiapkan (D-004).

### I-005 — EPMS points list belum disepakati
Vendor switchboard dan BMS Contractor belum sepakat soal format dan protokol EPMS points list.

- **Kategori:** Interface · **Prioritas:** Medium · **Status:** Open
- **Langkah berikut / penyelesaian:** Workshop interface akan diadakan.

### I-006 — Pintu panel UPS rusak saat receiving inspection
Receiving inspection menemukan pintu panel yang rusak pada satu modul UPS.

- **Kategori:** Kualitas · **Prioritas:** Low · **Status:** Closed (closed 2030-04-06)
- **Langkah berikut / penyelesaian:** Pintu pengganti sudah dipasang dan diinspeksi ulang.

## Pola yang Saya Lihat

Beberapa issue bukan kegagalan teknis, tapi celah koordinasi: scaffold di tempat yang salah, points list yang tidak ada owner-nya, lead time booking. Informasinya sebenarnya sudah ada — tapi tersebar di inbox orang yang berbeda. Lihat [[Schedule Paling Sering Pecah di Interface]].
