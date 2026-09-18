---
type: project-view
domain: project-alpha
project: Project Alpha
fictional: true
tags:
- project-alpha
- fictional
- readiness
data_date: 2030-04-08
---
# Electrical Equipment Installation - Area A

> [!warning] Data proyek fiktif
> Semua nama proyek, activity, tanggal, quantity, issue dan informasi proyek di Project Alpha adalah fiktif dan dibuat khusus untuk demonstrasi.

Bagian dari [[Gambaran Umum Project Alpha]]

## Kartu Activity
| Kolom | Nilai |
|---|---|
| Activity ID | A-3030 |
| Nama Activity | Electrical Equipment Installation — Area A (LV Switchboards & UPS) |
| WBS | ALPHA.3 Construction |
| Area | Area A |
| Disiplin | Electrical |
| Fase | CON |
| Durasi Awal (hk) | 12 |
| Baseline | 2030-04-08 → 2030-04-20 |
| Saat Ini | 2030-04-08 → 2030-04-20 |
| Total Float (hk) | 0 (critical) |
| Status | Not Started (0%) |
| Constraint Status | Constrained: C-003 |

## Yang Terlihat di Schedule
| Activity | Start | Finish | Durasi |
|---|---|---|---|
| Electrical Equipment Installation — Area A (LV Switchboards & UPS) | 2030-04-08 | 2030-04-20 | 12 hk |

## Apa yang Membuatnya Bisa Dimulai — Readiness Check
**Kesimpulan: NOT READY** — 4 dari 5 prerequisite yang tercatat sudah ready.

| Prerequisite | Kondisi | Constraint | Bukti / Deskripsi |
|---|---|---|---|
| Drawing | ✅ Ready | C-004 | Shop drawing LV switchboard dan UPS sudah approved (A-1020). |
| Material | ✅ Ready | C-005 | LV switchboard dan UPS sudah delivery dan lolos receiving inspection (A-2030) termasuk penggantian pintu panel UPS yang rusak. |
| Access | ❌ NOT READY | C-003 | Rigging route ke Area A terhalang scaffold facade yang dipasang melintang di loading bay; lifting permit LP-07 untuk rigging switchboard dan UPS masih pending. |
| Predecessor | ✅ Ready | C-007 | Finishing ruangan (A-3010) dan cable containment (A-3020) di Area A sudah selesai. |
| Manpower | ✅ Ready | C-006 | Crew instalasi elektrikal dan crew rigging sudah mobilisasi untuk Area A. |
| Inspection | Belum ada catatan | — | — |
| Interface | Belum ada catatan | — | — |

## Predecessor
| ID | Activity | Hubungan | Status |
|---|---|---|---|
| A-1020 | Shop Drawing Approval — LV Switchboards & UPS | FS | Complete |
| A-2030 | Delivery & Receiving Inspection — LV Switchboards & UPS | FS | Complete |
| A-3020 | Cable Containment Installation — Area A | FS | Complete |

## Successor
| ID | Activity | Hubungan | Total Float (hk) |
|---|---|---|---|
| A-3040 | Busway & LV Cable Pulling — Area A to Data Hall 1 | SS+6 | 0 (critical) |

## Issue dan Decision Terkait
| ID | Ringkasan | Status |
|---|---|---|
| I-001 | Rigging route ke Area A terhalang | Open |
| D-001 | Jangan release A-3030 untuk rigging sampai access constraint C-003 dipastikan clear. Selama menunggu crew hanya melakukan pengecekan unpacking dan setting-out. | Approved |
| D-002 | Facade Subcontractor memindahkan bay scaffold di loading bay; lifting permit LP-07 diajukan untuk review fast-track. | Approved |
| D-004 | Siapkan recovery contingency: jika start A-3030 mundur lebih dari dua hari kerja, cable pulling A-3040 dijalankan dengan extended hours atau second shift. | Contingency |

## Interpretasi — Apakah Kita Benar-Benar Ready?

Di atas kertas activity ini siap dimulai: drawing sudah approved, equipment sudah delivery dan diinspeksi, crew sudah mobilisasi, ruangan sudah selesai. Tapi ada satu prerequisite yang belum ready: rigging route. Empat dari lima bukan "hampir ready" — ini **belum ready**, karena tidak ada yang bisa masuk ke ruangan sampai akses clear.

Yang saya ambil dari sini:

- Bar di schedule hanya menunjukkan start yang normal. Readiness check yang menunjukkan risikonya. → [[Cek Readiness Sebelum Mulai]]
- Activity ini menggerakkan path energization, jadi start yang terlambat bukan masalah lokal. → [[Critical Path]], [[Total Float]]
- Tim menghilangkan constraint dari sumbernya dan menyiapkan recovery contingency, bukan memulai sebagian. → [[Decision Log]], [[Schedule Recovery]]
- Pengecekan akses seharusnya masuk di [[Lookahead Planning]] beberapa minggu sebelumnya — bukan pada tanggal start.
