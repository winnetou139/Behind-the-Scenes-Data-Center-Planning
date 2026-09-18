---
type: project-view
domain: project-alpha
project: Project Alpha
fictional: true
tags:
- project-alpha
- fictional
- constraints
data_date: 2030-04-08
---
# Constraint Register

> [!warning] Data proyek fiktif
> Semua nama proyek, activity, tanggal, quantity, issue dan informasi proyek di Project Alpha adalah fiktif dan dibuat khusus untuk demonstrasi.

Bagian dari [[Gambaran Umum Project Alpha]]

Status pada data date **2030-04-08**: 10 open dari 14 constraint.

## Open Constraint per Impact
| Impact Rating | Open |
|---|---|
| High | 4 |
| Medium | 3 |
| Low | 3 |

## Per Kategori
| Kategori | Total | Open |
|---|---|---|
| Drawing | 2 | 1 |
| Material | 2 | 1 |
| Access | 2 | 2 |
| Predecessor | 1 | 0 |
| Manpower | 2 | 1 |
| Inspection | 2 | 2 |
| Interface | 3 | 3 |

## Register
| ID | Activity | Kategori | Deskripsi | Owner | Dibutuhkan Tanggal | Status | Impact | Total Float Activity (hk) | Tindakan |
|---|---|---|---|---|---|---|---|---|---|
| C-001 | A-3070 | Drawing | Revisi layout CRAH menunggu jawaban RFI-014 (posisi CRAH bentrok dengan cable tray di atas di Data Hall 1). | Design Consultant | 2030-04-08 | Open | Low | 23 | Design Consultant menerbitkan revisi layout; planner mengecek ulang float di update berikutnya. |
| C-002 | A-3080 | Material | Forecast delivery generator mundur karena supplier QA hold; generator belum ada di site. | Procurement Lead | 2030-04-25 | Open | Medium | 17 | Procurement Lead meminta bukti progress supplier setiap minggu dan tanggal kirim yang sudah dikonfirmasi. |
| C-003 | [[Electrical Equipment Installation - Area A\|A-3030]] | Access | Rigging route ke Area A terhalang scaffold facade yang dipasang melintang di loading bay; lifting permit LP-07 untuk rigging switchboard dan UPS masih pending. | Main Contractor Site Manager | 2030-04-08 | Open | High | 0 (critical) | Facade Subcontractor memindahkan bay scaffold; Site Manager mengajukan LP-07 untuk review fast-track (lihat D-001 dan D-002). |
| C-004 | [[Electrical Equipment Installation - Area A\|A-3030]] | Drawing | Shop drawing LV switchboard dan UPS sudah approved (A-1020). | Design Consultant | 2030-04-08 | Closed | High | 0 (critical) | Tidak ada — sudah closed. |
| C-005 | [[Electrical Equipment Installation - Area A\|A-3030]] | Material | LV switchboard dan UPS sudah delivery dan lolos receiving inspection (A-2030) termasuk penggantian pintu panel UPS yang rusak. | Procurement Lead | 2030-04-08 | Closed | High | 0 (critical) | Tidak ada — sudah closed. |
| C-006 | [[Electrical Equipment Installation - Area A\|A-3030]] | Manpower | Crew instalasi elektrikal dan crew rigging sudah mobilisasi untuk Area A. | Electrical Subcontractor | 2030-04-08 | Closed | High | 0 (critical) | Tidak ada — sudah closed. |
| C-007 | [[Electrical Equipment Installation - Area A\|A-3030]] | Predecessor | Finishing ruangan (A-3010) dan cable containment (A-3020) di Area A sudah selesai. | Main Contractor Site Manager | 2030-04-08 | Closed | High | 0 (critical) | Tidak ada — sudah closed. |
| C-008 | A-3040 | Manpower | Puncak cable pulling butuh 24 electrician; Electrical Subcontractor baru konfirmasi 16. | Electrical Subcontractor | 2030-04-15 | Open | High | 0 (critical) | Electrical Subcontractor mengonfirmasi tambahan crew atau ketersediaan second shift (contingency D-004). |
| C-009 | A-4010 | Inspection | Inspection pihak ketiga sebelum energization harus di-booking minimal 10 hari kerja sebelumnya. | Project Planner | 2030-05-06 | Open | High | 0 (critical) | Booking inspection sekarang untuk window yang sudah direncanakan (D-003). |
| C-010 | A-4020 | Interface | Ketersediaan permanent power dari MV substation dan approval dari otoritas untuk energize. | Utility Coordinator | 2030-05-23 | Open | High | 0 (critical) | Utility Coordinator mengonfirmasi tanggal energization dan status pengajuan approval setiap minggu. |
| C-011 | A-4040 | Interface | EPMS points list dan protokol komunikasi belum disepakati antara vendor switchboard dan BMS Contractor. | BMS Contractor | 2030-05-17 | Open | Medium | 1 (near-critical) | Adakan workshop interface antara vendor dan BMS Contractor; sepakati points list dan protokol. |
| C-012 | A-4030 | Inspection | Pressure test chilled water harus disaksikan Commissioning Agent. | Commissioning Agent | 2030-05-13 | Open | Low | 3 (near-critical) | Konfirmasi tanggal witness setelah tanggal chiller setting sudah pasti. |
| C-013 | A-5030 | Access | Area penempatan load bank sementara dan rute kabel di generator yard belum dialokasikan. | Main Contractor Site Manager | 2030-05-25 | Open | Low | 7 | Alokasikan area di site logistics plan. |
| C-014 | A-5050 | Interface | Script Integrated Systems Testing harus di-approve oleh Commissioning Agent dan perwakilan Owner. | Commissioning Agent | 2030-05-25 | Open | Medium | 0 (critical) | Commissioning Agent menerbitkan draft script IST untuk direview. |

## Interpretasi — Cara Saya Membaca Register

Saya mengurutkan constraint dengan tiga pertanyaan. Apakah masih open? Apakah ada di path dengan float kecil atau nol? Seberapa cepat dibutuhkan? Access constraint yang open di critical path dan dibutuhkan sekarang lebih prioritas daripada drawing constraint pada activity yang float-nya masih banyak — walaupun keduanya sama-sama "Open".

- Kategori mengikuti catatan [[Constraints]] saya.
- Item dengan lead time (booking inspection, permit) butuh horizon yang lebih panjang → [[Lookahead Planning]].
- Interface constraint adalah yang paling tidak terlihat → [[Schedule Paling Sering Pecah di Interface]].
