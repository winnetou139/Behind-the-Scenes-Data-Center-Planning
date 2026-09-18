---
type: concept
domain: planning
status: evergreen
aliases:
  - Constraint Management
  - Readiness Constraints
tags:
  - constraints
  - readiness
  - lookahead
references:
  - REF-009
  - REF-010
updated: 2026-09-14
---

# Constraints

> **Intinya:** "Constraint" punya dua arti dalam planning — readiness constraint adalah apa pun yang menghalangi pekerjaan mulai atau berjalan di site, sedangkan date constraint adalah setting di software scheduling yang mengunci atau membatasi tanggal activity — dan keduanya tidak boleh tertukar.

Bagian dari [[Planning & Scheduling MOC]]

## Definisi

### 1. Readiness constraint (arti di site)
Kondisi yang harus terpenuhi sebelum sebuah activity bisa dikerjakan dengan aman dan produktif. Kategori yang saya screening:

| Kategori | Pertanyaan | Contoh di data center |
|---|---|---|
| Drawing / informasi | Apakah desain terbaru yang sudah approved tersedia? | IFC dan shop drawing switchboard yang sudah approved |
| Material | Apakah sudah di site, sudah diinspeksi dan bisa dijangkau? | Section switchboard sudah diterima dan diinspeksi |
| Akses | Apakah crew dan alat bisa benar-benar mencapai area kerja? | Jalur rigging bersih, izin lifting, ruangan sudah diserahkan |
| Predecessor | Apakah pekerjaan sebelumnya sudah selesai sesuai standar? | Containment terpasang, finishing ruangan selesai |
| Manpower | Apakah ada crew yang kompeten lengkap dengan alatnya? | Crew instalasi electrical dan crew rigging |
| Inspeksi / izin | Apakah inspeksi, izin dan witness sudah dijadwalkan? | Inspektor pihak ketiga, permit to work |
| Interface | Apakah trade lain, utilitas atau sistem lain sudah dikoordinasikan? | Scaffold façade, pekerjaan mechanical, sambungan utilitas |

Constraint management artinya mengidentifikasi hal-hal ini di [[Lookahead Planning|lookahead]], memberi setiap item owner dan tanggal need-by, lalu memantaunya di register sampai constraint itu hilang.

### 2. Date constraint (arti di software)
Setting yang meng-override atau membatasi perhitungan CPM — di P6: Start On, Start On or After, Finish On or Before, Mandatory Start, Mandatory Finish, As Late As Possible dan lainnya. Date constraint punya kegunaan yang sah (milestone kontrak, window pengiriman, tanggal outage utilitas), tapi mengubah [[Total Float]] dan bisa menyembunyikan masalah logic. Hard constraint, yang mengunci atau membatasi tanggal (Mandatory Start atau Finish, Finish On or Before), paling merusak — karena itu schedule assessment menandainya. Soft constraint seperti Start On or After masih membiarkan logic mendorong activity ke tanggal yang lebih lambat.

### Kenapa mencampur keduanya membingungkan
"Activity ini ada constraint-nya" punya arti berbeda bagi site manager dan bagi scheduler. Izin yang terlambat adalah readiness constraint; mengetik tanggal "Start On or After" untuk itu sama saja membekukan tebakan ke dalam model. Modelkan sebagai [[Hubungan Antar Activity|logic]] — milestone izin sebagai predecessor — dan kelola di register. Saya selalu bilang "readiness constraint" atau "date constraint", tidak pernah hanya "constraint".

## Cek Readiness
Contoh: A-3030 (fiktif).

| Prerequisite | Siap? |
|---|---|
| Drawing | Ya |
| Material | Ya |
| Manpower | Ya |
| Predecessor | Ya |
| Akses | **Tidak** |
| **Apakah activity bisa mulai?** | **Tidak** |

Readiness bukan rata-rata. Kalau empat dari lima prerequisite siap, activity itu **belum** siap — yang kurang satu itulah yang menentukan kapan bisa mulai. "Siap 80%" adalah angka yang menenangkan untuk pekerjaan yang sebenarnya belum bisa dimulai.

## Kenapa Penting
Readiness constraint yang tidak diselesaikan membuat rencana mulai berubah jadi crew yang menganggur dan finish yang terlambat. Date constraint tanpa alasan membuat schedule tidak lagi jujur soal float.

## Sudut Pandang Planner
Saya screening readiness constraint di enam minggu sebelumnya, lalu lagi di tiga minggu. Setiap item yang masih terbuka diberi owner dan tanggal need-by, yang ditetapkan lebih awal dari start activity sebesar waktu yang dibutuhkan untuk menyelesaikan masalahnya. Constraint akses dan interface paling sering bikin orang kaget, karena itu ada di scope pihak lain.

## Contoh Praktis
Untuk A-3030, jalur rigging terhalang scaffold façade dan izin lifting masih pending. Di atas kertas activity-nya tampak siap; secara fisik belum bisa mulai. Lihat [[Electrical Equipment Installation - Area A]], [[Constraint Register]] dan [[Cek Readiness Sebelum Mulai]].

## Kesalahan yang Sering Terjadi
- Bilang "constraint" tanpa menyebut jenisnya.
- Memasukkan masalah readiness sebagai date constraint di P6.
- Melaporkan readiness dalam bentuk persentase.
- Memantau constraint tanpa owner atau tanggal need-by.
- Hanya mengecek drawing dan material, lalu melewatkan akses, inspeksi dan interface.

## Konsep Terkait
- [[Lookahead Planning]] — tempat readiness constraint di-screening dan diselesaikan.
- [[Hubungan Antar Activity]] — logic adalah alternatif dari date constraint.
- [[Total Float]] — date constraint mendistorsi float.
- [[Schedule Recovery]] — menyelesaikan constraint lebih awal sering jadi recovery yang paling murah.
- [[Cek Readiness Sebelum Mulai]] — lesson learned tentang tidak memulai pekerjaan yang belum siap.
- [[Schedule Paling Sering Pecah di Interface]] — constraint interface antar trade.
- [[Constraint Register]] — register fiktif untuk Project Alpha.

## Referensi
- [[REF-009 LCI Last Planner System|REF-009]] — analisis constraint dan make-ready dalam lookahead planning.
- [[REF-010 Ballard 2000 Last Planner Thesis|REF-010]] — asal mula constraint screening dalam Last Planner System.
