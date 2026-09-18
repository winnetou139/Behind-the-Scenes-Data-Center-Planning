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
# Decision Log

> [!warning] Data proyek fiktif
> Semua nama proyek, activity, tanggal, quantity, issue dan informasi proyek di Project Alpha adalah fiktif dan dibuat khusus untuk demonstrasi.

Bagian dari [[Gambaran Umum Project Alpha]]

| ID | Tanggal | Decision | Status | Issue | Constraint |
|---|---|---|---|---|---|
| D-001 | 2030-04-05 | Jangan release A-3030 untuk rigging sampai access constraint C-003 dipastikan clear. Selama menunggu crew hanya melakukan pengecekan unpacking dan setting-out. | Approved | I-001 | C-003 |
| D-002 | 2030-04-05 | Facade Subcontractor memindahkan bay scaffold di loading bay; lifting permit LP-07 diajukan untuk review fast-track. | Approved | I-001 | C-003 |
| D-003 | 2030-04-05 | Booking inspection pihak ketiga sebelum energization sekarang untuk window A-4010 yang direncanakan. | Approved | — | C-009 |
| D-004 | 2030-04-05 | Siapkan recovery contingency: jika start A-3030 mundur lebih dari dua hari kerja, cable pulling A-3040 dijalankan dengan extended hours atau second shift. | Contingency | I-004 | C-008 |
| D-005 | 2030-04-05 | Terima keterlambatan delivery generator tanpa acceleration; monitor setiap minggu dan laporkan pemakaian float. | Approved | I-002 | C-002 |
| D-006 | 2030-04-05 | Tambahkan readiness review atas constraint register sebagai agenda tetap di rapat weekly coordination. | Approved | I-001; I-005 | — |

### D-001 — Rapat Weekly Coordination W13
**Keputusan:** Jangan release A-3030 untuk rigging sampai access constraint C-003 dipastikan clear. Selama menunggu crew hanya melakukan pengecekan unpacking dan setting-out.

**Alasan:** Start sebagian tanpa rigging route yang clear berisiko double handling dan pengangkatan yang tidak aman. Empat dari lima prerequisite ready artinya belum ready.

- **Activity:** [[Electrical Equipment Installation - Area A|A-3030]]
- **Tindak lanjut:** Konfirmasi akses clear saat daily check-in sebelum rigging dimulai. — Main Contractor Site Manager, batas 2030-04-08

### D-002 — Rapat Weekly Coordination W13
**Keputusan:** Facade Subcontractor memindahkan bay scaffold di loading bay; lifting permit LP-07 diajukan untuk review fast-track.

**Alasan:** Menghilangkan access constraint dari sumbernya, bukan mengakalinya.

- **Activity:** [[Electrical Equipment Installation - Area A|A-3030]]
- **Tindak lanjut:** Bay scaffold sudah dipindahkan dan permit sudah approved. — Facade Subcontractor, batas 2030-04-10

### D-003 — Rapat Weekly Coordination W13
**Keputusan:** Booking inspection pihak ketiga sebelum energization sekarang untuk window A-4010 yang direncanakan.

**Alasan:** Lead time inspector berada di luar lookahead tiga minggu. Booking lebih awal melindungi tanggal energization.

- **Activity:** A-4010
- **Tindak lanjut:** Konfirmasi booking sudah diarsipkan. — Project Planner, batas 2030-04-10

### D-004 — Rapat Weekly Coordination W13
**Keputusan:** Siapkan recovery contingency: jika start A-3030 mundur lebih dari dua hari kerja, cable pulling A-3040 dijalankan dengan extended hours atau second shift.

**Alasan:** A-3040 mengikuti A-3030 di path elektrikal. Recovery hanya realistis jika crew sudah dikonfirmasi dari awal.

- **Activity:** [[Electrical Equipment Installation - Area A|A-3030]], A-3040
- **Tindak lanjut:** Electrical Subcontractor mengonfirmasi ketersediaan crew second shift secara tertulis. — Electrical Subcontractor, batas 2030-04-12

### D-005 — Rapat Weekly Coordination W13
**Keputusan:** Terima keterlambatan delivery generator tanpa acceleration; monitor setiap minggu dan laporkan pemakaian float.

**Alasan:** Path generator masih punya float. Acceleration akan menambah biaya tanpa melindungi tanggal finish. Pemakaian float tetap harus terlihat.

- **Activity:** A-2050, A-3080, A-5030
- **Tindak lanjut:** Laporkan float path generator di catatan weekly planning. — Project Planner, batas 2030-04-12

### D-006 — Rapat Weekly Coordination W13
**Keputusan:** Tambahkan readiness review atas constraint register sebagai agenda tetap di rapat weekly coordination.

**Alasan:** Constraint baru ketahuan pada tanggal start, bukan beberapa minggu sebelumnya.

- **Activity:** —
- **Tindak lanjut:** Review constraint sudah ditambahkan ke template agenda. — Project Planner, batas 2030-04-12

## Mengapa Decision Ini Penting

Dua decision sengaja memilih untuk *tidak* bertindak: tidak me-release activity yang baru sebagian ready, dan tidak melakukan acceleration pada path yang masih punya float. Decision planning yang baik sering kali justru soal menahan diri.

Lihat [[Cek Readiness Sebelum Mulai]], [[Acceleration]], [[Schedule Recovery]] dan [[Pantau Float, Bukan Hanya Tanggal]].
