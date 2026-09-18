---
type: concept
domain: planning
status: evergreen
aliases:
  - Lookahead
tags:
  - lookahead
  - constraints
  - readiness
references:
  - REF-009
  - REF-010
updated: 2026-09-14
---

# Lookahead Planning

> **Intinya:** Lookahead planning mengambil beberapa minggu ke depan dari master schedule, memecahnya jadi tugas yang bisa dikerjakan, menyaring setiap tugas dari constraint dan menyiapkannya, supaya hanya pekerjaan yang benar-benar siap yang masuk ke weekly work plan.

Bagian dari [[Planning & Scheduling MOC]]

## Definisi
Lookahead adalah rencana jangka pendek yang bergulir, diturunkan dari master schedule. Lookahead bukan sekadar filter tanggal — melainkan proses menyiapkan pekerjaan. Dalam Last Planner System, lookahead berada di antara phase schedule dan weekly work plan, dan kegiatan utamanya adalah **make-ready**: mengidentifikasi dan menyelesaikan [[Constraints|readiness constraint]] sebelum pekerjaan dijadwalkan mulai.

| Horizon | Cara saya memakainya |
|---|---|
| 3 minggu | Koordinasi level tugas dengan supervisor dan mandor: crew, material di lokasi kerja, akses, izin untuk beberapa hari ke depan. |
| 6 minggu | Screening constraint dan make-ready: drawing, pengiriman, inspeksi, shutdown, interface dengan trade lain. |

Panjang window berbeda-beda per project dan organisasi: terminologi AACE menggambarkan look-ahead schedule sebagai tampilan pendek dua sampai tiga minggu, sementara panduan Last Planner dari LCI umumnya memakai lookahead enam minggu yang di-update mingguan. Yang penting, window-nya cukup panjang untuk menyelesaikan constraint yang ada di dalamnya.

## Siklus Mingguan

```mermaid
flowchart LR
    MS[Master schedule] --> LA[Window lookahead]
    LA --> CS[Screening constraint]
    CS --> MR[Tindakan make-ready]
    MR --> WWP[Weekly work plan]
    WWP --> RV[Review penyelesaian dan penyebab]
    RV --> LA
```

Last Planner membingkainya sebagai **should** (apa kata schedule), **can** (apa yang bebas constraint), **will** (apa yang tim komitmenkan) dan **did** (apa yang benar-benar selesai). Memantau porsi komitmen yang selesai — sering dilaporkan sebagai Percent Plan Complete — beserta alasan yang tidak tercapai adalah cara proses ini belajar.

## Kenapa Penting
Master schedule gagal di titik bertemunya dengan site. Sebagian besar delay "mendadak" yang saya lihat dalam seminggu sebenarnya adalah constraint yang sudah terlihat berminggu-minggu sebelumnya tapi tidak ada yang memilikinya. Lookahead membuat kepemilikan itu eksplisit, dan di sinilah tindakan [[Schedule Recovery]] benar-benar dijalankan.

## Sudut Pandang Planner
Aturan pertama: tidak ada yang masuk weekly work plan kecuali sudah lolos cek readiness. Mengomitmenkan crew ke pekerjaan yang belum siap berarti waktu menganggur, produktivitas hilang, dan rencana yang tidak dipercaya siapa pun.

Aturan kedua: ketahui apa yang ada di luar window. Lead time equipment, booking inspeksi pihak ketiga, dan approval utilitas atau instansi sering butuh tindakan jauh sebelum tugasnya muncul di tampilan tiga minggu. Saya menyimpan daftar terpisah untuk tindakan long-lead yang menjadi input lookahead.

Aturan ketiga: lookahead harus sinkron dengan master schedule. Kalau keduanya bercerita berbeda, salah satunya salah.

## Contoh Praktis
Di [[Weekly Planning - Week 14]] (fiktif), A-3030 di-screening dan dinyatakan siap dari sisi drawing, material, manpower dan predecessor — tapi tidak dari sisi akses. Itulah persis yang seharusnya dimunculkan lookahead sebelum tanggal start. Review yang sama juga menunjukkan bahwa booking inspektor pihak ketiga untuk inspeksi pre-energization butuh lead time lebih panjang dari yang terlihat di window tiga minggu — constraint yang hanya tertangkap oleh tampilan yang lebih panjang.

## Kesalahan yang Sering Terjadi
- Membuat lookahead hanya sebagai filter tanggal di P6 tanpa screening constraint.
- Membiarkan lookahead menjauh dari master schedule.
- Window terlalu pendek untuk menangkap lead time inspeksi, izin dan pengiriman.
- Mengomitmenkan crew ke pekerjaan yang "hampir siap".
- Mencatat komitmen yang tidak tercapai tanpa alasan, sehingga tidak ada yang dipelajari.

## Konsep Terkait
- [[Constraints]] — apa yang di-screening dan diselesaikan oleh lookahead.
- [[Schedule Recovery]] — tindakan recovery disiapkan dan dipantau lewat lookahead.
- [[Cek Readiness Sebelum Mulai]] — lesson learned tentang tidak memulai pekerjaan yang belum siap.
- [[Weekly Planning - Week 14]] — contoh lookahead fiktif dalam praktik.

## Referensi
- [[REF-009 LCI Last Planner System|REF-009]] — lookahead planning, make-ready, analisis constraint dan weekly work planning.
- [[REF-010 Ballard 2000 Last Planner Thesis|REF-010]] — asal mula Last Planner System dan proses make-ready.
