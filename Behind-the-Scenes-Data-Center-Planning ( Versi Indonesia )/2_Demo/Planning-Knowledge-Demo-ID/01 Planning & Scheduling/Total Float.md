---
type: concept
domain: planning
status: evergreen
aliases:
  - Float
tags:
  - scheduling
  - float
  - cpm
references:
  - REF-001
updated: 2026-09-14
---

# Total Float

> **Intinya:** Total float adalah berapa lama sebuah activity bisa terlambat tanpa menggeser finish project atau milestone yang di-constraint; free float adalah berapa lama activity bisa slip tanpa menggeser successor mana pun.

Bagian dari [[Planning & Scheduling MOC]]

## Definisi
- **Total float** = Late Finish − Early Finish (atau Late Start − Early Start), dalam hari kerja pada calendar activity tersebut. "Slack" adalah sinonim yang umum.
- **Free float** = waktu sebuah activity bisa slip tanpa menggeser early start successor mana pun. Nilainya tidak pernah lebih besar dari total float.
- **Float negatif** biasanya muncul saat early date hasil hitungan lebih lambat dari yang diizinkan date constraint atau tanggal must-finish; progress out-of-sequence juga bisa menghasilkannya. Artinya schedule sedang bilang: dengan logic saat ini, tanggal ini tidak bisa dicapai, kurang sekian hari.

Float dimiliki oleh sebuah **path**, bukan hanya satu activity. Kalau activity di awal memakai lima hari float, setiap activity berikutnya di path itu kehilangan lima hari yang sama.

P6 membiarkan kita memilih cara menghitung total float (start float, finish float, atau yang lebih kecil dari keduanya) dan apakah activity dengan open end dipaksa jadi critical. Pahami setting-nya sebelum membandingkan float antar schedule. (Lihat Critical Path Method untuk perhitungannya.)

## Pemakaian dan Erosi Float
Pemakaian float itu normal: activity slip dan float menyerapnya. **Erosi float** — float di sebuah path yang terus turun dari update ke update — adalah salah satu peringatan dini terbaik yang saya punya. Tanggal finish bisa tetap tidak berubah selama berminggu-minggu sementara float yang melindunginya terus menghilang. Begitu tanggalnya bergeser, opsi recovery yang murah sudah habis.

## Siapa Pemilik Float?
Itu pertanyaan kontrak, bukan pertanyaan scheduling. Ada kontrak yang memberikan float ke project, ada yang ke contractor, ada yang tidak mengaturnya, dan ada yang menanganinya lewat aturan extension of time. SCL Protocol memberikan posisi yang direkomendasikan, tapi itu panduan, bukan klausul kontrak. Saya tidak memberi pendapat soal kepemilikan float; saya memastikan float ditampilkan dengan jelas dan tim kontrak membaca kontraknya.

## Kenapa Penting
Float menunjukkan di mana schedule punya ruang dan di mana tidak. Float menentukan apakah sebuah delay critical, apakah recovery dibutuhkan, dan ke mana resource bisa dipindahkan tanpa merugikan. Float yang tinggi secara tidak wajar biasanya berarti logic yang hilang, bukan fleksibilitas.

## Sudut Pandang Planner
Saya melaporkan tren float, bukan hanya nilai float. Grafik sederhana float di beberapa path teratas selama beberapa update terakhir memberi tahu manajemen lebih banyak daripada bar chart apa pun. Kalau ada yang bilang "kita masih punya float", saya tanya: float ke milestone mana, di calendar apa, setelah constraint apa?

## Contoh Praktis
Di project fiktif ini, pengiriman standby generator slip. Slip itu memakan float di path-nya — setting generator dan load bank testing — tapi path itu tidak critical, jadi finish tidak bergeser. Instalasi electrical Area A, yang ada di critical path, tidak punya bantalan seperti itu. Kedua fakta ini hanya terlihat dengan membaca float, bukan tanggal. Lihat [[Project Alpha Schedule]] dan [[Pantau Float, Bukan Hanya Tanggal]].

## Kesalahan yang Sering Terjadi
- Menganggap float sebagai waktu cadangan yang bebas dipakai pihak mana pun.
- Membandingkan float antar schedule dengan setting perhitungan atau calendar yang berbeda.
- Menyembunyikan float negatif dengan constraint, atau dengan memperpendek duration tanpa bukti.
- Menerima float besar yang sebenarnya karena successor yang hilang.
- Hanya memantau tanggal finish dan melewatkan erosi float.

## Konsep Terkait
- [[Critical Path]] — path dengan float paling kecil.
- [[Schedule Delay]] — delay memakan float dulu sebelum menggeser finish.
- [[Schedule Recovery]] — recovery bertujuan memulihkan float di driving path.
- [[Acceleration]] — salah satu cara membeli kembali float, dengan biaya.
- [[Forecasting]] — tren float menjadi input forecast milestone.
- [[Pantau Float, Bukan Hanya Tanggal]] — lesson learned bahwa erosi float adalah peringatan dini.

## Referensi
- [[REF-001 GAO Schedule Assessment Guide|REF-001]] — definisi float dan float yang wajar sebagai best practice.
