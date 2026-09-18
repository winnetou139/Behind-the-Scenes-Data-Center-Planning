---
type: project-view
domain: project-alpha
project: Project Alpha
fictional: true
tags:
- project-alpha
- fictional
- lookahead
data_date: 2030-04-08
---
# Weekly Planning - Week 14

> [!warning] Data proyek fiktif
> Semua nama proyek, activity, tanggal, quantity, issue dan informasi proyek di Project Alpha adalah fiktif dan dibuat khusus untuk demonstrasi.

Bagian dari [[Gambaran Umum Project Alpha]]

## Data Date dan Horizon
| Item | Nilai |
|---|---|
| Data date | 2030-04-08 (Week 14) |
| Lookahead tiga minggu | 2030-04-08 → 2030-04-27 |
| Horizon trigger enam minggu | 2030-04-08 → 2030-05-18 |
| Forecast Ready for Service vs baseline | 2030-07-03 vs 2030-07-03 |

## Minggu Lalu (Week 13)
| Tanggal | Tipe | Yang terjadi | Terkait |
|---|---|---|---|
| 2030-04-02 | Issue Raised | Scaffold facade yang dipasang melintang di loading bay menghalangi rigging route ke Area A; lifting permit LP-07 masih pending. | I-001; C-003; A-3030 |
| 2030-04-03 | Notification | Supplier generator memberitahukan QA hold; forecast delivery mundur. | I-002; C-002; A-2050 |
| 2030-04-03 | Issue Raised | RFI-014 diajukan: posisi CRAH bentrok dengan cable tray di atas di Data Hall 1. | I-003; C-001; A-3070 |
| 2030-04-04 | Notification | Electrical Subcontractor konfirmasi 16 dari 24 electrician tersedia untuk puncak cable pulling. | I-004; C-008; A-3040 |
| 2030-04-04 | Issue Raised | Vendor switchboard dan BMS Contractor belum sepakat soal format EPMS points list. | I-005; C-011; A-4040 |
| 2030-04-05 | Meeting | Rapat weekly coordination W13 diadakan; decision D-001 sampai D-006 dicatat. | D-001; D-002; D-003; D-004; D-005; D-006 |
| 2030-04-05 | Update | Crew instalasi dan crew rigging untuk Area A dikonfirmasi sudah mobilisasi. | C-006; A-3030 |
| 2030-04-06 | Closure | Pintu panel UPS pengganti sudah dipasang dan diinspeksi ulang; receiving inspection selesai. | I-006; C-005; A-2030 |
| 2030-04-06 | Update | Catatan weekly planning Week 14 diterbitkan dengan data date 2030-04-08. | A-3030; A-3040; A-3070 |

## Lookahead Tiga Minggu
| ID | Activity | Start | Finish | Total Float (hk) | Readiness | Open Constraint |
|---|---|---|---|---|---|---|
| A-2050 | Manufacture & Delivery — Standby Generators | 2030-01-28 | 2030-04-25 | 17 | Ready | — |
| A-2040 | Manufacture & Delivery — Air-Cooled Chillers | 2030-02-22 | 2030-05-04 | 3 (near-critical) | Ready | — |
| A-3060 | Chilled Water Piping — Plant Yard & Data Hall 1 | 2030-02-22 | 2030-04-23 | 8 | Ready | — |
| [[Electrical Equipment Installation - Area A\|A-3030]] | Electrical Equipment Installation — Area A (LV Switchboards & UPS) | 2030-04-08 | 2030-04-20 | 0 (critical) | NOT READY | C-003 |
| A-3070 | CRAH Unit Installation — Data Hall 1 | 2030-04-08 | 2030-04-20 | 23 | NOT READY | C-001 |
| A-3040 | Busway & LV Cable Pulling — Area A to Data Hall 1 | 2030-04-15 | 2030-05-04 | 0 (critical) | NOT READY | C-008 |
| A-3080 | Generator Setting & Fuel System — Generator Yard | 2030-04-26 | 2030-05-13 | 17 | NOT READY | C-002 |

## Constraint yang Harus Di-clear (Horizon Enam Minggu)
| ID | Activity | Kategori | Owner | Dibutuhkan Tanggal | Hari Kerja dari Data Date | Impact |
|---|---|---|---|---|---|---|
| C-001 | A-3070 | Drawing | Design Consultant | 2030-04-08 | 0 | Low |
| C-003 | [[Electrical Equipment Installation - Area A\|A-3030]] | Access | Main Contractor Site Manager | 2030-04-08 | 0 | High |
| C-008 | A-3040 | Manpower | Electrical Subcontractor | 2030-04-15 | 6 | High |
| C-002 | A-3080 | Material | Procurement Lead | 2030-04-25 | 15 | Medium |
| C-009 | A-4010 | Inspection | Project Planner | 2030-05-06 | 24 | High |
| C-012 | A-4030 | Inspection | Commissioning Agent | 2030-05-13 | 30 | Low |
| C-011 | A-4040 | Interface | BMS Contractor | 2030-05-17 | 34 | Medium |

## Float Watch (Total Float ≤ 5 hk)
| ID | Activity | Finish | Total Float (hk) |
|---|---|---|---|
| M-9000 | Data Hall 1 Ready for Service | 2030-07-03 | 0 (critical) |
| [[Electrical Equipment Installation - Area A\|A-3030]] | Electrical Equipment Installation — Area A (LV Switchboards & UPS) | 2030-04-20 | 0 (critical) |
| A-3040 | Busway & LV Cable Pulling — Area A to Data Hall 1 | 2030-05-04 | 0 (critical) |
| A-3050 | Cable Termination & Dressing — Area A | 2030-05-16 | 0 (critical) |
| A-4010 | Pre-Energization Inspection & IR Testing — LV Switchboards (L2) | 2030-05-22 | 0 (critical) |
| A-4020 | Permanent Power Energization — LV Switchboards | 2030-05-24 | 0 (critical) |
| A-5010 | Start-Up & Functional Testing — UPS & LV Switchboards (L3/L4) | 2030-06-07 | 0 (critical) |
| A-5020 | Start-Up & Functional Testing — Chillers & CRAH (L3/L4) | 2030-06-07 | 0 (critical) |
| A-5050 | Integrated Systems Testing (L5) — Data Hall 1 | 2030-06-19 | 0 (critical) |
| A-6010 | Punch List Closeout & O&M Documentation | 2030-07-03 | 0 (critical) |
| A-4040 | BMS/EPMS Point-to-Point Checks | 2030-05-28 | 1 (near-critical) |
| A-5040 | BMS/EPMS Integration & Graphics Verification | 2030-06-06 | 1 (near-critical) |
| A-2040 | Manufacture & Delivery — Air-Cooled Chillers | 2030-05-04 | 3 (near-critical) |
| A-3065 | Chiller Setting — Mechanical Plant Yard | 2030-05-11 | 3 (near-critical) |
| A-4030 | Pressure Testing & Flushing — Chilled Water (L2) | 2030-05-21 | 3 (near-critical) |
| A-6020 | Operator Training & Handover Documentation | 2030-06-28 | 4 (near-critical) |

## Decision yang Harus Ditindaklanjuti
| ID | Tindak Lanjut | Owner | Batas | Status |
|---|---|---|---|---|
| D-001 | Konfirmasi akses clear saat daily check-in sebelum rigging dimulai. | Main Contractor Site Manager | 2030-04-08 | Approved |
| D-002 | Bay scaffold sudah dipindahkan dan permit sudah approved. | Facade Subcontractor | 2030-04-10 | Approved |
| D-003 | Konfirmasi booking sudah diarsipkan. | Project Planner | 2030-04-10 | Approved |
| D-004 | Electrical Subcontractor mengonfirmasi ketersediaan crew second shift secara tertulis. | Electrical Subcontractor | 2030-04-12 | Contingency |
| D-005 | Laporkan float path generator di catatan weekly planning. | Project Planner | 2030-04-12 | Approved |
| D-006 | Review constraint sudah ditambahkan ke template agenda. | Project Planner | 2030-04-12 | Approved |

## Open Issue
| ID | Judul | Prioritas | Owner |
|---|---|---|---|
| I-001 | Rigging route ke Area A terhalang | High | Main Contractor Site Manager |
| I-002 | Delivery generator mundur | Medium | Procurement Lead |
| I-003 | Layout CRAH bentrok (RFI-014) | Medium | Design Consultant |
| I-004 | Kekurangan crew cable pulling | Medium | Electrical Subcontractor |
| I-005 | EPMS points list belum disepakati | Medium | BMS Contractor |

## Komentar Planner

Minggu ini soal akses dan orang, bukan soal bar. Instalasi Area A tidak bisa di-release sampai rigging route clear. Cable pulling bergantung pada jumlah crew yang belum dikonfirmasi.

- Path near-critical perlu perhatian yang sama dengan critical path → [[Pantau Float, Bukan Hanya Tanggal]].
- Booking inspection adalah trigger yang berada di luar window tiga minggu → [[Lookahead Planning]].
- Catatan metode terkait: [[Lookahead Planning]], [[Forecasting]].
