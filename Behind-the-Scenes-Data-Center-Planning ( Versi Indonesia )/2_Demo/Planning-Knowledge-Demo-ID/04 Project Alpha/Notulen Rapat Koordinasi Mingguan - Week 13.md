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
# Notulen Rapat Koordinasi Mingguan - Week 13
> [!warning] Data proyek fiktif
> Semua nama proyek, activity, tanggal, quantity, issue dan informasi proyek di Project Alpha adalah fiktif dan dibuat khusus untuk demonstrasi.

Bagian dari [[Gambaran Umum Project Alpha]]

## Rapat Weekly Coordination W13 — 2030-04-05

**Peserta (peran):** BMS Contractor, Design Consultant, Electrical Subcontractor, Facade Subcontractor, Main Contractor Site Manager, Procurement Lead, Project Planner

### 1. Issue Baru Minggu Ini
| ID | Judul | Prioritas | Owner |
|---|---|---|---|
| I-001 | Rigging route ke Area A terhalang | High | Main Contractor Site Manager |
| I-002 | Delivery generator mundur | Medium | Procurement Lead |
| I-003 | Layout CRAH bentrok (RFI-014) | Medium | Design Consultant |
| I-004 | Kekurangan crew cable pulling | Medium | Electrical Subcontractor |
| I-005 | EPMS points list belum disepakati | Medium | BMS Contractor |

### 2. Review Constraint (Tiga Minggu ke Depan)
| ID | Activity | Kategori | Dibutuhkan Tanggal | Impact | Owner |
|---|---|---|---|---|---|
| C-001 | A-3070 | Drawing | 2030-04-08 | Low | Design Consultant |
| C-003 | [[Electrical Equipment Installation - Area A\|A-3030]] | Access | 2030-04-08 | High | Main Contractor Site Manager |
| C-008 | A-3040 | Manpower | 2030-04-15 | High | Electrical Subcontractor |
| C-002 | A-3080 | Material | 2030-04-25 | Medium | Procurement Lead |

### 3. Decision
| ID | Decision | Alasan | Status |
|---|---|---|---|
| D-001 | Jangan release A-3030 untuk rigging sampai access constraint C-003 dipastikan clear. Selama menunggu crew hanya melakukan pengecekan unpacking dan setting-out. | Start sebagian tanpa rigging route yang clear berisiko double handling dan pengangkatan yang tidak aman. Empat dari lima prerequisite ready artinya belum ready. | Approved |
| D-002 | Facade Subcontractor memindahkan bay scaffold di loading bay; lifting permit LP-07 diajukan untuk review fast-track. | Menghilangkan access constraint dari sumbernya, bukan mengakalinya. | Approved |
| D-003 | Booking inspection pihak ketiga sebelum energization sekarang untuk window A-4010 yang direncanakan. | Lead time inspector berada di luar lookahead tiga minggu. Booking lebih awal melindungi tanggal energization. | Approved |
| D-004 | Siapkan recovery contingency: jika start A-3030 mundur lebih dari dua hari kerja, cable pulling A-3040 dijalankan dengan extended hours atau second shift. | A-3040 mengikuti A-3030 di path elektrikal. Recovery hanya realistis jika crew sudah dikonfirmasi dari awal. | Contingency |
| D-005 | Terima keterlambatan delivery generator tanpa acceleration; monitor setiap minggu dan laporkan pemakaian float. | Path generator masih punya float. Acceleration akan menambah biaya tanpa melindungi tanggal finish. Pemakaian float tetap harus terlihat. | Approved |
| D-006 | Tambahkan readiness review atas constraint register sebagai agenda tetap di rapat weekly coordination. | Constraint baru ketahuan pada tanggal start, bukan beberapa minggu sebelumnya. | Approved |

### 4. Action
| Dari | Action | Owner | Batas |
|---|---|---|---|
| D-001 | Konfirmasi akses clear saat daily check-in sebelum rigging dimulai. | Main Contractor Site Manager | 2030-04-08 |
| D-002 | Bay scaffold sudah dipindahkan dan permit sudah approved. | Facade Subcontractor | 2030-04-10 |
| D-003 | Konfirmasi booking sudah diarsipkan. | Project Planner | 2030-04-10 |
| D-004 | Electrical Subcontractor mengonfirmasi ketersediaan crew second shift secara tertulis. | Electrical Subcontractor | 2030-04-12 |
| D-005 | Laporkan float path generator di catatan weekly planning. | Project Planner | 2030-04-12 |
| D-006 | Review constraint sudah ditambahkan ke template agenda. | Project Planner | 2030-04-12 |

## Yang Saya Ambil dari Rapat

Sebagian besar decision adalah soal *menghilangkan* constraint (akses, booking, interface), bukan mengubah tanggal. Rapat ini juga mengubah proses: review constraint menjadi agenda tetap. Perubahan seperti ini yang membuat perbaikan sekali jalan menjadi kebiasaan.

Lihat [[Constraints]] dan [[Schedule Recovery]].
