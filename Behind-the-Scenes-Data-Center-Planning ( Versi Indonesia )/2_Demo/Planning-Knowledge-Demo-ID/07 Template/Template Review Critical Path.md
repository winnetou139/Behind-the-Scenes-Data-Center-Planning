---
type: ai-output
reviewed: false
dibuat_oleh: Claude
data_date: YYYY-MM-DD
prompt: "<pertanyaan persis seperti yang diketik user>"
activity:
  - A-xxxx
sumber:
  - "[[Constraint Register]]"
  - "[[Decision Log]]"
  - "[[Project Alpha Schedule]]"
  - "[[Weekly Planning - Week 14]]"
tags:
  - ai-output
  - project-alpha
  - fictional
---

%%
ATURAN PENGISIAN — jangan salin blok komentar ini ke note hasil.
1. Data date diambil dari [[Weekly Planning - Week 14]] (baris "Data date").
2. Baris tabel = setiap constraint di [[Constraint Register]] dengan Status "Open" DAN "Total Float Activity (hk)" = "0 (critical)". Tidak ada baris lain.
3. Urutkan menurut "Dibutuhkan Tanggal" (paling awal dulu); kalau sama, menurut Constraint ID.
4. Nama Activity disalin persis dari tabel activity di [[Project Alpha Schedule]].
5. Kolom Decision = semua ID di [[Decision Log]] yang kolom Constraint-nya memuat Constraint ID itu, dipisah koma. Kalau tidak ada, tulis "—".
6. Pertanyaan review diambil persis dari tabel "Pertanyaan per kategori" di bawah, sesuai kategori constraint. Jangan menambah pertanyaan lain.
7. Jangan menambah opini, saran, atau pengetahuan umum. Semua isi harus berasal dari note sumber.

Pertanyaan per kategori:
| Kategori | Pertanyaan review |
|---|---|
| Drawing | Apakah revisi drawing yang approved sudah ada di site sebelum tanggal dibutuhkan? |
| Material | Apakah tanggal kirim sudah dikonfirmasi supplier dan material lolos inspeksi? |
| Access | Apakah akses dan permit sudah clear sebelum tanggal dibutuhkan? |
| Predecessor | Apakah pekerjaan sebelumnya benar-benar selesai, bukan hampir selesai? |
| Manpower | Apakah jumlah crew yang dikonfirmasi sudah sama dengan kebutuhan puncak? |
| Inspection | Apakah inspection sudah di-booking sesuai lead time-nya? |
| Interface | Apakah pihak di luar tim sudah mengonfirmasi tanggal dan status approval-nya? |
%%

# Review Critical Path — Data Date YYYY-MM-DD

> [!warning] Draft AI — belum direview
> Dibuat oleh AI dari data Project Alpha (fiktif) di vault ini. Cek setiap sumber sebelum dipakai. Ubah `reviewed` menjadi `true` setelah direview.

## Pertanyaan

<pertanyaan persis seperti yang diketik user>

## Ringkasan

- Constraint open di critical path: **N**
- Paling mendesak: **C-xxx · A-xxxx** · dibutuhkan YYYY-MM-DD · owner <Owner>

## Activity di Critical Path dengan Constraint Open

| # | Activity | Nama Activity | Constraint | Kategori | Owner | Dibutuhkan | Decision |
|---|---|---|---|---|---|---|---|
| 1 | A-xxxx | <nama> | C-xxx | <kategori> | <owner> | YYYY-MM-DD | D-xxx |

## Pertanyaan Review per Activity

### 1. A-xxxx — <nama activity>
- [ ] <pertanyaan review sesuai kategori>
- Constraint: C-xxx — <deskripsi dari Constraint Register>
- Decision: D-xxx — <isi decision dari Decision Log>, atau "Belum ada decision"
- Sumber: [[Constraint Register]], [[Decision Log]]

## Sumber yang Dikutip

- [[Constraint Register]] — constraint, kategori, owner, tanggal dibutuhkan, total float
- [[Decision Log]] — decision per constraint
- [[Project Alpha Schedule]] — nama activity
- [[Weekly Planning - Week 14]] — data date

## Catatan Review Planner

- Direview oleh:
- Tanggal review:
- Yang diubah atau tidak disetujui:
