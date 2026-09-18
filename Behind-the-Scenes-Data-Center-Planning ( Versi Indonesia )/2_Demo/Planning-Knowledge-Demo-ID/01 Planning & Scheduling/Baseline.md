---
type: concept
domain: planning
status: evergreen
aliases:
  - Schedule Baseline
tags:
  - scheduling
  - progress
  - schedule-quality
references:
  - REF-001
updated: 2026-09-14
---

# Baseline

> **Intinya:** Baseline adalah salinan schedule yang sudah approved dan dibekukan, sebagai acuan untuk mengukur progress, delay dan kinerja; baseline hanya berubah lewat re-baseline yang terkontrol.

Bagian dari [[Planning & Scheduling MOC]]

## Definisi
Baseline schedule merekam rencana yang disepakati pada satu titik waktu: activity, logic, duration, calendar, tanggal dan, kalau dipakai, resource dan biaya. Setelah approved, baseline tidak diedit. Schedule saat ini bergerak mengikuti progress; baseline tetap diam supaya variance bisa diukur.

Di P6, baseline adalah salinan project yang disimpan dan di-assign sebagai pembanding, sehingga schedule saat ini bisa menampilkan bar baseline dan kolom variance. Banyak project menyimpan beberapa baseline: baseline kontrak, snapshot berkala dan re-baseline yang sudah disetujui.

**Re-baseline** mengganti rencana acuan — biasanya setelah ada perubahan besar yang disetujui, atau saat baseline yang ada sudah tidak lagi mewakili rencana yang bisa dicapai. Re-baseline butuh persetujuan dan jejak audit: apa yang berubah, kenapa, dan siapa yang menyetujui.

## Kenapa Penting
- Tanpa baseline, kita bisa bilang posisi kita di mana, tapi tidak bisa bilang sudah menyimpang seberapa jauh.
- Diskusi delay dan recovery bergantung pada perbandingan antara rencana dan apa yang benar-benar terjadi.
- Report variance, indeks kinerja dan banyak mekanisme kontrak mengandalkan acuan yang stabil.

## Schedule Seperti Apa yang Layak Dibekukan
Sebelum membuat baseline, saya cek apakah schedule akan lolos review kualitas dasar: logic lengkap, date constraint sedikit dan ada alasannya, duration masuk akal, critical path yang logis, float yang realistis, dan procurement, testing serta commissioning sudah dimodelkan — bukan hanya konstruksi. Baseline yang buruk jadi alat ukur yang buruk untuk seluruh project.

## Sudut Pandang Planner
Baseline adalah file paling sensitif secara politis yang saya kelola. Saya simpan salinan yang tidak disentuh, saya export, dan saya catat persetujuannya. Kalau ada tekanan untuk "update saja baseline-nya" karena variance-nya terlihat jelek, saya jelaskan bahwa re-baseline menyembunyikan sejarah — tidak mengembalikan satu hari pun. Kalau rencananya memang benar-benar berubah, lakukan re-baseline secara formal dan simpan baseline lama sebagai referensi.

Di data center, saya pastikan baseline memuat urutan commissioning dengan tingkat detail yang nanti bisa dibandingkan. Satu bar commissioning saja membuat diskusi delay di kemudian hari hampir mustahil.

## Contoh Praktis
Di [[Project Alpha Schedule]] (fiktif), setiap activity membawa tanggal baseline di samping tanggal saat ini. Dari situlah tim bisa melihat path mana yang sudah menyimpang — misalnya path generator — dan apakah penyimpangan itu sudah sampai ke milestone finish. Baseline tidak pernah diedit saat update mingguan.

## Kesalahan yang Sering Terjadi
- Membuat baseline dari schedule yang penuh open end dan constraint, lalu mengukur terhadapnya selama bertahun-tahun.
- Menimpa baseline saat update.
- Re-baseline informal yang terlalu sering sehingga menghancurkan sejarah variance.
- Salah assign baseline di P6, sehingga kolom variance membandingkan dengan snapshot lama.
- Membiarkan procurement, testing dan commissioning belum dikembangkan saat baseline.

## Konsep Terkait
- [[Schedule Delay]] — delay diukur terhadap baseline dan update sebelumnya.
- [[Schedule Recovery]] — recovery plan dibandingkan dengan baseline sebelum disetujui.
- [[Pengecekan Kualitas Schedule]] — review kualitas yang harus dilewati sebelum dibekukan.

## Referensi
- [[REF-001 GAO Schedule Assessment Guide|REF-001]] — menjaga baseline di bawah configuration control, dengan basis document yang menjelaskan alasan constraint, lag dan duration panjang.
