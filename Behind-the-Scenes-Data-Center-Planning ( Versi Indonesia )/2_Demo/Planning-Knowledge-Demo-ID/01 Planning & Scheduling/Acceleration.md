---
type: concept
domain: planning
status: evergreen
tags:
  - recovery
  - delay
  - scheduling
references:
  - REF-001
updated: 2026-09-14
---

# Acceleration

> **Intinya:** Acceleration berarti mengerjakan pekerjaan lebih cepat dari rencana saat ini — biasanya dengan tambahan resource, jam kerja lebih panjang atau shift tambahan — untuk selesai lebih awal atau mengejar delay, dan hampir selalu membawa konsekuensi biaya, produktivitas dan kontrak.

Bagian dari [[Planning & Scheduling MOC]]

## Definisi
Acceleration memperpendek waktu yang dibutuhkan untuk sisa pekerjaan dibandingkan rencana saat ini. Dalam istilah scheduling, ini beririsan dengan schedule compression: **crashing** (menambah resource pada activity driving) dan kerja dengan jam lebih panjang atau shift lebih banyak. **Fast-tracking** (menumpangtindihkan pekerjaan yang direncanakan berurutan) kadang dikelompokkan bersama, walaupun yang diubah adalah logic, bukan kecepatan kerja.

Kata ini dipakai dalam dua arti, jadi saya selalu menyebut arti yang mana. Dalam arti scheduling (seperti di panduan GAO), acceleration adalah memperpendek sisa schedule. Dalam arti kontrak (seperti di terminologi AACE), acceleration adalah tindakan owner yang menuntut penyelesaian lebih awal dari jadwal — lihat directed vs constructive di bawah.

Acceleration tidak sama dengan [[Schedule Recovery]]. Recovery adalah rencana untuk merebut kembali waktu; acceleration adalah salah satu cara menjalankannya. Recovery yang menyelesaikan constraint atau me-resequence pekerjaan bisa saja sama sekali tidak melibatkan acceleration.

## Directed vs Constructive Acceleration
Ini istilah kontrak. Perlakuannya berbeda-beda tergantung kontrak dan yurisdiksi, jadi mintalah saran ahli. Secara garis besar:
- **Directed (instructed) acceleration** — client atau perwakilannya menginstruksikan contractor untuk mempercepat, biasanya dengan biaya yang disepakati atau dinilai sesuai kontrak.
- **Constructive acceleration** — tidak ada instruksi formal, tapi contractor secara efektif terpaksa mempercepat, misalnya karena hak atas tambahan waktu diperdebatkan atau tidak diberikan sementara tanggal awal tetap diberlakukan.

SCL Protocol mendorong para pihak menyepakati dasar pembayaran sebelum acceleration dimulai, bukan berdebat setelahnya. Peran saya sebagai planner adalah memastikan schedule, instruksi (atau ketiadaannya) dan perubahan yang terjadi tercatat dengan jelas.

## Dampak ke Biaya dan Produktivitas
Acceleration jarang linear — menggandakan crew tidak membuat duration jadi setengah. Dampak yang umum dilaporkan dalam praktik industri antara lain:
- Tarif premium untuk lembur dan kerja shift.
- Penurunan produktivitas akibat lembur berkepanjangan dan kelelahan.
- Kepadatan dan penumpukan trade di ruang sempit seperti electrical room dan data hall.
- Tambahan supervisi, quality, inspeksi dan pengawasan keselamatan, terutama di malam hari.
- Masa adaptasi untuk crew tambahan yang baru di site.

Besarnya dampak ini tergantung pekerjaan dan kondisinya. Saya menghindari mengutip persentase umum dan memakai data produktivitas project sendiri kalau ada.

## Kenapa Penting
Acceleration bisa melindungi tanggal yang critical, tapi hanya kalau diterapkan di [[Critical Path]], dijalankan dalam periode yang realistis, dan dibayar oleh pihak yang sudah setuju untuk membayar. Kalau tidak, uang habis tanpa menggeser forecast.

## Sudut Pandang Planner
Sebelum merekomendasikan acceleration, saya cek empat hal: apakah activity-nya benar-benar driving; apakah ada ruang fisik untuk tambahan orang; apakah supervisi dan inspeksi tersedia di jam-jam itu; dan berapa lama pola kerja itu bisa dipertahankan? Dorongan singkat yang terarah lebih efektif daripada lembur tanpa batas waktu. Saya juga memodelkan rencana acceleration dan mengecek apa yang jadi critical berikutnya — path kedua sering membatasi hasil yang bisa didapat.

## Contoh Praktis
Di project fiktif ini, tim menyiapkan contingency untuk menjalankan cable pulling dengan jam kerja diperpanjang atau shift kedua kalau start equipment Area A slip. Itu adalah acceleration yang terarah: di critical path electrical menuju energization, [[Commissioning]] dan IST, pada pekerjaan yang tambahan jamnya realistis bisa berubah jadi progress. Apakah dan kapan dijalankan, serta atas instruksi siapa, adalah jenis keputusan yang dicatat di [[Decision Log]].

## Kesalahan yang Sering Terjadi
- Menyebut setiap recovery plan "acceleration", atau sebaliknya.
- Mempercepat pekerjaan yang tidak critical.
- Mengasumsikan hasil linear dari tambahan crew atau jam kerja.
- Memulai pekerjaan yang dipercepat tanpa instruksi atau kesepakatan biaya yang tercatat.
- Lupa tambahan resource inspeksi, supervisi dan commissioning yang dibutuhkan untuk mengimbangi kecepatan.

## Konsep Terkait
- [[Schedule Recovery]] — acceleration adalah salah satu cara menjalankan recovery plan.
- [[Schedule Delay]] — delay biasanya yang memicu acceleration.
- [[Critical Path]] — acceleration hanya membantu di activity driving.
- [[Total Float]] — acceleration membeli kembali float, dengan biaya.
- [[Forecasting]] — menunjukkan apakah acceleration benar-benar berubah jadi progress.
- [[Decision Log]] — tempat keputusan acceleration dicatat di project fiktif ini.

## Referensi
- [[REF-001 GAO Schedule Assessment Guide|REF-001]] — acceleration sebagai pengurangan durasi schedule, serta teknik compression seperti crashing, fast tracking dan lembur yang fokus pada activity critical.
