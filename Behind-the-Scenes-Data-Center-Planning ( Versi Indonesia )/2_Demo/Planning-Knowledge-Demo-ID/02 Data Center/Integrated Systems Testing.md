---
type: concept
domain: data-center
status: evergreen
aliases:
  - IST
tags:
  - data-center
  - commissioning
  - readiness
references:
  - REF-025
  - REF-021
  - REF-020
updated: 2026-09-14
---

# Integrated Systems Testing

> **Intinya:** Integrated Systems Testing (IST) adalah commissioning Level 5 — system elektrikal, mekanikal dan kontrol dites bersama dengan beban IT simulasi dan skenario kegagalan yang direncanakan, untuk membuktikan fasilitas berperilaku sesuai desain — dan karena semua jalur bertemu di sini, readiness IST adalah masalah planning.

Bagian dari [[Beranda Pengetahuan Planning]]

## Definisi

IST mengetes fasilitas sebagai satu system utuh. Load bank menghasilkan panas dan beban listrik yang nantinya dihasilkan equipment IT, dan tim tes menjalankan skenario sesuai script sambil memantau power, cooling, kontrol dan kondisi ruangan. IST adalah level terakhir dari [[Commissioning Levels]].

IST tidak sama dengan "full load test". Load test membuktikan kapasitas; IST membuktikan perilaku — bagaimana system merespons kejadian dan saling merespons.

Kelompok skenario yang umum (daftar sebenarnya berasal dari desain, OPR dan script yang disetujui):

- **Kehilangan suplai utility** — generator menyala dan mengambil beban, UPS memikul beban kritis selama transisi, cooling tetap jalan, dan fasilitas kembali ke suplai utility dengan mulus.
- **Kejadian pada generator** — generator gagal menyala atau trip, dan unit redundan menutupinya sesuai desain.
- **Kejadian pada UPS** — modul gagal, transfer ke bypass dan kembali, serta operasi maintenance.
- **Respons cooling** — chiller, pompa atau CRAH gagal; restart setelah power terputus; kondisi ruangan tetap dalam batas desain.
- **Monitoring** — alarm BMS dan EPMS, log event dan time-stamp sesuai dengan yang benar-benar terjadi.
- **Skenario maintenance** — kalau desain mengklaim concurrent maintainability, equipment bisa diisolasi tanpa menjatuhkan beban.

## Kenapa Penting

Di IST, redundancy berhenti menjadi gambar dan berubah menjadi bukti. IST juga titik di mana masalah tersembunyi dari semua tahap sebelumnya muncul bersamaan: setting yang salah, sequence kontrol, celah interface. Owner dan operator mengandalkan IST untuk menerima fasilitas.

## Sudut Pandang Planner

Kenapa saya memperlakukan readiness IST sebagai masalah planning:

- **Semua jalur bertemu.** Jalur elektrikal, mekanikal, generator dan kontrol semuanya bergabung ke IST. Satu prerequisite yang kurang akan menghentikannya.
- **Biaya menunggu.** Load bank, engineer vendor, saksi dan staf operasi dimobilisasi bersamaan; start yang gagal itu mahal.
- **Persiapan dengan lead time panjang.** Script harus ditulis, direview dan disetujui; sewa dan penempatan load bank diatur; izin untuk menjalankan generator dalam waktu lama dicek.
- **Gagal itu normal.** Beberapa skenario pasti gagal dan butuh perbaikan serta tes ulang. Saya merencanakan jendela waktu tes ulang, bukan mengasumsikan semuanya lancar.

Prerequisite yang saya pantau: L4 selesai untuk semua system dalam scope, open issue ditutup atau diterima secara formal, script disetujui, permanent power, BMS/EPMS terintegrasi, load bank sudah ditempatkan dan dikabel, rencana keselamatan dan pengaturan LOTO, dan semua yang perlu menyaksikan sudah dijadwalkan.

## Contoh Praktis

Di [[Gambaran Umum Project Alpha|Project Alpha]], IST untuk Data Hall 1 (A-5050) punya empat predecessor commissioning: start-up dan functional testing elektrikal (A-5010), mekanikal (A-5020), load bank testing generator (A-5030) dan integrasi BMS/EPMS (A-5040). Persetujuan script IST dan area penempatan load bank untuk testing generator dipantau di [[Constraint Register]], dan points list EPMS yang belum selesai mengancam jalur integrasi. Salah satu saja bisa menahan IST.

## Kesalahan yang Sering Terjadi

- Memakai jendela waktu IST sebagai buffer schedule.
- Memulai IST dengan issue L4 yang masih terbuka "supaya hemat waktu".
- Meremehkan logistik load bank — power, kabel, penempatan, panas.
- Tidak ada jendela waktu tes ulang.
- Staf operasi tidak dilibatkan, sehingga transfer pengetahuan harus diulang saat handover.

## Konsep Terkait

- [[Commissioning Levels]] — IST adalah Level 5, hanya boleh dimasuki setelah L4 selesai.
- [[Handover]] — hasil IST dan item yang masih terbuka menjadi masukan handover.
- [[Critical Path]] — IST adalah titik temu di mana banyak jalur bergabung.
- [[Cek Readiness Sebelum Mulai]] — lesson learned yang paling mahal kalau diabaikan saat IST.

## Referensi

- [[REF-025 Data Center Commissioning Levels|REF-025]] — IST sebagai Level 5 dalam commissioning level.
- [[REF-021 ASHRAE Guideline 0 Commissioning Process|REF-021]] — verifikasi terhadap kebutuhan proyek owner.
- [[REF-020 Uptime Institute Tier Standard|REF-020]] — tujuan topologi (redundancy, concurrent maintainability) yang dibuktikan IST.
