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
# Area A - LV Electrical Room

> [!warning] Data proyek fiktif
> Semua nama proyek, activity, tanggal, quantity, issue dan informasi proyek di Project Alpha adalah fiktif dan dibuat khusus untuk demonstrasi.

Bagian dari [[Gambaran Umum Project Alpha]]

**Area A — LV Electrical Room.** Berisi LV main switchboard dan modul UPS yang menyuplai Data Hall 1.

## Activity di Area A
| ID | Activity | Start | Finish | Total Float (hk) | Status | Constraint Status |
|---|---|---|---|---|---|---|
| A-1010 | IFC Drawings — LV Electrical Room (Area A) | 2030-01-07 | 2030-01-26 | — | Complete | n/a (complete) |
| A-1020 | Shop Drawing Approval — LV Switchboards & UPS | 2030-01-28 | 2030-02-09 | — | Complete | n/a (complete) |
| A-2030 | Delivery & Receiving Inspection — LV Switchboards & UPS | 2030-03-27 | 2030-04-06 | — | Complete | n/a (complete) |
| A-3010 | Civil & Architectural Finishes — LV Electrical Room (Area A) | 2030-01-07 | 2030-02-27 | — | Complete | n/a (complete) |
| A-3020 | Cable Containment Installation — Area A | 2030-02-28 | 2030-03-22 | — | Complete | n/a (complete) |
| [[Electrical Equipment Installation - Area A\|A-3030]] | Electrical Equipment Installation — Area A (LV Switchboards & UPS) | 2030-04-08 | 2030-04-20 | 0 (critical) | Not Started | Constrained: C-003 |
| A-3050 | Cable Termination & Dressing — Area A | 2030-05-06 | 2030-05-16 | 0 (critical) | Not Started | Clear |
| A-4010 | Pre-Energization Inspection & IR Testing — LV Switchboards (L2) | 2030-05-17 | 2030-05-22 | 0 (critical) | Not Started | Constrained: C-009 |
| A-4020 | Permanent Power Energization — LV Switchboards | 2030-05-23 | 2030-05-24 | 0 (critical) | Not Started | Constrained: C-010 |
| A-5010 | Start-Up & Functional Testing — UPS & LV Switchboards (L3/L4) | 2030-05-25 | 2030-06-07 | 0 (critical) | Not Started | Clear |

## Constraint pada Activity Area A
| ID | Activity | Kategori | Status | Dibutuhkan Tanggal |
|---|---|---|---|---|
| C-003 | [[Electrical Equipment Installation - Area A\|A-3030]] | Access | Open | 2030-04-08 |
| C-004 | [[Electrical Equipment Installation - Area A\|A-3030]] | Drawing | Closed | 2030-04-08 |
| C-005 | [[Electrical Equipment Installation - Area A\|A-3030]] | Material | Closed | 2030-04-08 |
| C-006 | [[Electrical Equipment Installation - Area A\|A-3030]] | Manpower | Closed | 2030-04-08 |
| C-007 | [[Electrical Equipment Installation - Area A\|A-3030]] | Predecessor | Closed | 2030-04-08 |
| C-009 | A-4010 | Inspection | Open | 2030-05-06 |
| C-010 | A-4020 | Interface | Open | 2030-05-23 |

## Issue yang Menyangkut Area A
| ID | Judul | Prioritas | Status |
|---|---|---|---|
| I-001 | Rigging route ke Area A terhalang | High | Open |
| I-006 | Pintu panel UPS rusak saat receiving inspection | Low | Closed |

## Interpretasi

Area A kecil tapi critical: di sinilah permanent power untuk Data Hall 1 berawal. Ruangan seperti ini mengumpulkan banyak interface — finishing sipil, containment, rigging equipment berat, cabling, inspection dan energization. Karena itu saya melihatnya lewat [[Schedule Paling Sering Pecah di Interface]] dan [[Cek Readiness Sebelum Mulai]].
