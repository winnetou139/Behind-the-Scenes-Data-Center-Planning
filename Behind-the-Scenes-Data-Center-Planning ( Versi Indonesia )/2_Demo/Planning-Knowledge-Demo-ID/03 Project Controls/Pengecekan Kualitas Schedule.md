---
type: concept
domain: project-controls
status: evergreen
aliases:
  - DCMA 14-Point Assessment
  - Schedule Health Check
tags:
  - schedule-quality
  - project-controls
  - cpm
references:
  - REF-001
updated: 2026-09-14
---

# Pengecekan Kualitas Schedule
> **Intinya:** Schedule quality check, seperti DCMA 14-point assessment, menguji apakah schedule disusun cukup baik untuk dipercaya — hasilnya menandai masalah struktur yang perlu diselidiki, tapi itu indikator, bukan vonis apakah rencananya realistis.

Bagian dari [[Beranda Pengetahuan Planning]]

## Definisi

Schedule quality check adalah pengujian terstruktur terhadap susunan dan integritas schedule. Yang paling dikenal adalah **DCMA 14-point assessment**, dari pamflet DCMA tahun 2012 yang dibuat untuk schedule kontraktor pertahanan AS dan sekarang dipakai jauh lebih luas. GAO Schedule Assessment Guide (REF-001) lebih luas lagi: sepuluh best practice yang dikelompokkan dalam empat karakteristik schedule yang andal — komprehensif, tersusun dengan baik, kredibel, dan terkendali.

Metrik DCMA berlaku untuk task yang belum selesai (task yang sudah selesai, level-of-effort, summary, dan milestone tidak dihitung). Threshold di bawah sesuai pamflet; kontrak atau client bisa menetapkan threshold sendiri.

| # | Check | Yang dicari | Threshold di pamflet |
|---|---|---|---|
| 1 | Logic | Task tanpa predecessor dan/atau successor | ≤ 5% |
| 2 | Leads | Lag negatif | Tidak ada |
| 3 | Lags | Relationship dengan lag positif | ≤ 5% |
| 4 | Relationship types | Porsi relationship finish-to-start | FS ≥ 90%; start-to-finish hanya sesekali, dengan justifikasi |
| 5 | Hard constraints | Constraint must-start-on, must-finish-on, start/finish-no-later-than | ≤ 5% |
| 6 | High float | Total float di atas 44 hari kerja (sekitar dua bulan) | ≤ 5% |
| 7 | Negative float | Total float di bawah nol | Idealnya tidak ada; masing-masing dijelaskan dengan rencana perbaikan |
| 8 | High duration | Durasi baseline di atas 44 hari kerja | ≤ 5% |
| 9 | Invalid dates | Tanggal forecast sebelum status date; tanggal actual sesudahnya | Tidak ada |
| 10 | Resources | Task yang punya durasi tapi tanpa jam atau biaya, kalau schedule-nya resource-loaded | Tanpa threshold angka |
| 11 | Missed tasks | Task yang selesai setelah baseline finish, dari task yang di-baseline selesai sebelum status date | ≤ 5% |
| 12 | Critical path test | Tambahkan keterlambatan ke task critical: apakah completion ikut mundur sebesar itu? | Pass/fail |
| 13 | Critical Path Length Index (CPLI) | (Panjang critical path + total float) ÷ panjang critical path | Di bawah 0,95 jadi tanda |
| 14 | Baseline Execution Index (BEI) | Task yang selesai ÷ task yang di-baseline untuk selesai | Di bawah 0,95 jadi tanda |

## Kenapa Penting

Forecast hanya sebaik model yang menghasilkannya. Open end merusak perhitungan Critical Path Method, dan hard constraint membuat tanggal tidak merespons progress. Akibatnya, schedule yang cacat bisa menunjukkan finish yang aman padahal tidak akan tercapai sekeras apa pun usaha di site.

## Sudut Pandang Planner

**Indikator, bukan vonis.** Pamflet itu sendiri memperlakukan metrik merah sebagai tanda untuk diselidiki, bukan kegagalan otomatis. Sebagian lag memang wajar; sebagian high float memang nyata. Sebaliknya, schedule bisa lolos semua check padahal durasinya tidak realistis atau logic-nya salah secara teknis — tidak ada check yang tahu bahwa functional testing mekanikal butuh permanent power.

Yang saya lakukan:

- Menjalankan check sebelum setiap submission dan memantau trennya dari update ke update.
- Untuk setiap tanda: perbaiki, atau catat kenapa itu bisa diterima.
- Menelusuri logic per disiplin — check menguji struktur; orang yang menguji isinya.

## Contoh Praktis

Di [[Project Alpha Schedule]] yang fiktif, cable pulling (A-3040) mengikuti equipment installation (A-3030) dengan relationship start-to-start dan lag, jadi terhitung di check lags dan relationship types. Itu bisa diterima — cable pulling bisa mulai begitu section switchboard pertama sudah terpasang — dan saya catat alasannya. Check yang lebih penting justru tidak dijalankan tool mana pun: apakah functional testing chiller dan CRAH (A-5020) sudah di-link ke energization permanent power (A-4020)?

## Kesalahan yang Sering Terjadi

- Menganggap lolos check berarti schedule-nya realistis.
- Mengakali metrik, misalnya menambah link hanya supaya open end hilang.
- Memperlakukan threshold di pamflet sebagai persyaratan kontrak padahal kontraknya tidak mengatur.

## Konsep Terkait

- [[Hubungan Antar Activity]] — logic, lead, lag, dan relationship type dicek langsung.
- [[Total Float]] — check high float dan negative float membaca schedule lewat float.
- [[Critical Path]] — critical path test mengecek apakah path-nya tidak terputus.
- [[Baseline]] — missed tasks dan BEI membandingkan progress dengan baseline.
- [[Forecasting]] — forecast hanya kredibel kalau schedule di belakangnya sehat.

## Referensi

- [[REF-001 GAO Schedule Assessment Guide|REF-001]] — sepuluh best practice dan empat karakteristik schedule yang andal; high float sebagai tanda logic yang hilang.
