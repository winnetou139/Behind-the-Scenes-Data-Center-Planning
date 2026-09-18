---
type: concept
domain: planning
status: evergreen
aliases:
  - Delay
tags:
  - delay
  - float
  - scheduling
references:
updated: 2026-09-14
---

# Schedule Delay

> **Intinya:** Schedule delay adalah pekerjaan yang mulai atau selesai lebih lambat dari rencana; delay baru menggeser finish project atau milestone penting kalau melebihi float yang tersedia di path-nya.

Bagian dari [[Planning & Scheduling MOC]]

## Definisi
- **Delay** — activity atau milestone yang terjadi lebih lambat dari rencana, diukur terhadap [[Baseline]] atau update sebelumnya.
- **Disruption** — hilangnya produktivitas: pekerjaan berjalan kurang efisien dari rencana, walaupun tanggal belum langsung bergeser. Disruption sering berujung pada delay, tapi cara menganalisis keduanya berbeda.
- **Critical delay** — delay di [[Critical Path]], atau delay yang cukup besar sampai menghabiskan seluruh [[Total Float]] di path-nya, sehingga finish atau milestone penting bergeser.
- **Non-critical delay** — delay yang terserap oleh float. Finish tetap, tapi float sudah terpakai dan tidak tersedia lagi untuk nanti.
- **Concurrent delay** — secara umum, delay yang disebabkan pihak berbeda yang memengaruhi tanggal penyelesaian yang sama pada waktu yang sama. SCL Protocol membatasi concurrency "sejati" untuk kondisi di mana risk event dari employer dan risk event dari contractor sama-sama secara efektif menyebabkan delay penyelesaian. Perlakuannya sangat tergantung kontrak dan yurisdiksi; sebagai planner, saya mencatat faktanya, bukan memutuskannya.

Mengelompokkan delay berdasarkan siapa yang menanggung risiko (employer, contractor, netral) adalah alokasi kontraktual, bukan penilaian scheduling.

## Catatan yang Dibuat Saat Kejadian Paling Penting
Pertanyaan soal delay biasanya muncul berbulan-bulan setelah kejadian. Yang tersisa hanyalah apa yang ditulis pada saat itu:
- Update schedule yang tersimpan beserta narasinya.
- Daily report, buku harian site dan foto bertanggal.
- Constraint register, RFI dan tanggal responsnya.
- Notulen meeting, issue log dan decision log.
- Instruksi, notice dan korespondensi.

SCL Protocol sangat menekankan pentingnya programme yang rutin di-update dan catatan yang baik. Tanpa itu, delay yang benar-benar terjadi pun sulit dibuktikan.

## Analisis Forensik adalah Pekerjaan Spesialis
Analisis delay untuk menentukan hak (entitlement) — perbandingan as-planned vs as-built, windows analysis, time impact analysis dan lainnya — punya taksonomi yang diakui dalam recommended practice AACE tentang forensic schedule analysis, dan setiap metode punya jebakannya sendiri. Metode yang tepat tergantung kontrak, catatan yang tersedia dan tujuannya. Tugas saya sebagai project planner adalah segera menandai delay dan menjaga schedule serta catatan dalam kondisi yang bisa dipakai spesialis — bukan bertindak sebagai ahlinya.

## Kenapa Penting
Mengenali sejak awal apakah sebuah delay critical menentukan responsnya: monitor, mitigasi atau recovery. Mencatatnya dengan benar menentukan apakah konsekuensi waktu dan biayanya nanti bisa diselesaikan secara adil.

## Sudut Pandang Planner
Saat ada delay yang dilaporkan, saya ajukan empat pertanyaan: apa yang terjadi, kapan mulainya, di path mana, dan berapa float yang dimiliki path itu? Lalu jawabannya saya masukkan ke narasi update minggu itu. Ingatan bukan catatan.

Saya juga mewaspadai disruption yang belum terlihat di tanggal — crew yang bekerja memutari halangan, remobilisasi berulang. Biasanya itu akan jadi delay di kemudian hari.

## Contoh Praktis
Project fiktif ini punya dua kasus yang kontras. Slip pengiriman generator memakan float di path non-critical; finish tidak bergeser. Masalah akses Area A, kalau tidak diselesaikan, akan men-delay activity di critical path electrical — dan lewat ketergantungan permanent power, juga mechanical functional testing dan IST. [[Issue Log]] dan [[Decision Log]] adalah tempat fakta-fakta itu dicatat saat terjadi.

## Kesalahan yang Sering Terjadi
- Menganggap setiap activity yang terlambat sebagai delay project tanpa mengecek float.
- Mengandalkan ingatan, bukan catatan yang dibuat saat kejadian.
- Menimpa update sebelumnya, sehingga jejak bukti hilang.
- Memakai "delay" dan "disruption" seolah sama.
- Melakukan analisis klaim informal di weekly report tanpa metode atau keahlian yang tepat.

## Konsep Terkait
- [[Total Float]] — delay memakan float dulu sebelum menggeser finish.
- [[Critical Path]] — critical delay adalah delay di driving path.
- [[Schedule Recovery]] — respons terencana terhadap critical delay.
- [[Acceleration]] — salah satu respons yang mungkin, dengan implikasi biaya dan kontrak.
- [[Baseline]] — acuan untuk mengukur delay.

