---
type: concept
domain: data-center
status: evergreen
tags:
  - data-center
  - planning
  - commissioning
references:
  - REF-021
  - REF-025
updated: 2026-09-14
---

# Data Center Project Lifecycle

> **Intinya:** Data center bergerak melalui engineering, procurement, konstruksi, inspeksi dan testing, commissioning dan handover — fase-fase yang tumpang tindih per system dan bertemu pada satu tujuan: fasilitas yang terbukti Ready for Service.

Bagian dari [[Beranda Pengetahuan Planning]]

## Definisi

Lifecycle yang saya pakai saat merencanakan data center (atau satu data hall di dalamnya) punya enam fase:

| Fase | Apa yang terjadi | Apa yang diserahkan ke fase berikutnya |
|---|---|---|
| Engineering | Desain IFC, shop drawing, persetujuan submittal | Desain dan equipment yang sudah disetujui |
| Procurement | Pembuatan, factory acceptance testing (L1), pengiriman | Equipment yang sudah dites dan ada di site |
| Konstruksi | Finishing ruangan, containment, setting equipment, perpipaan, pengkabelan | System yang sudah terpasang |
| Inspeksi & testing | Pengecekan instalasi, IR testing, pressure testing, point-to-point (L2) | Bukti bahwa system aman untuk dinyalakan |
| Commissioning | Start-up dan functional testing (L3/L4), Integrated Systems Testing (L5) | Bukti bahwa system berfungsi, sendiri maupun bersama-sama |
| Handover | Penutupan punch list, dokumentasi O&M, pelatihan | Fasilitas yang bisa dijalankan operator |

Nama dan batas fase berbeda antar organisasi dan kontrak. Yang penting, setiap transisi ditentukan oleh bukti, bukan oleh tanggal.

## Kenapa Penting

Di banyak gedung komersial, commissioning adalah activity penyelesaian. Di data center, commissioning adalah produknya: klien membeli kapasitas yang tangguh, dan kapasitas itu belum ada sampai [[Commissioning]] membuktikannya. Ini memindahkan risiko schedule ke bagian akhir. Perubahan desain yang terlambat, equipment dengan lead time panjang, dan interface yang belum selesai semuanya muncul di fase-fase terakhir, tepat saat ruang untuk menyerapnya paling sempit.

Kebutuhan listrik data center yang terus naik, yang didokumentasikan untuk Amerika Serikat di laporan LBNL 2024, adalah salah satu alasan owner mendorong delivery yang cepat dan bertahap. Data hall berikutnya sering dibangun di sebelah hall yang sudah live, sehingga fase-fase akhir mendapat constraint operasional tambahan (akses, shutdown, izin).

## Sudut Pandang Planner

- Saya merencanakan mundur dari Ready for Service dan bertanya apa yang harus diserahkan setiap fase sebelum fase berikutnya bisa mulai.
- Saya menyusun Work Breakdown Structure supaya bisa melihat area (di mana pekerjaan terjadi) sekaligus system (apa yang di-commissioning).
- Durasi procurement mencakup FAT, perjalanan saksi, kemungkinan tes ulang di pabrik dan pengiriman — bukan hanya waktu pembuatan.
- Commissioning mendapat logic yang nyata dan durasi yang realistis, terhubung ke instalasi dan energization — tidak pernah hanya satu blok di akhir.
- Saya memperkirakan fase-fase akan tumpang tindih: satu system bisa sedang functional testing sementara system lain masih dipasang.

## Contoh Praktis

Potongan fiktif [[Gambaran Umum Project Alpha|Project Alpha]] mengikuti lifecycle ini untuk Data Hall 1. WBS-nya mencerminkan enam fase, dan ID activity-nya mengikuti fase tersebut (A-1xxx engineering sampai A-6xxx handover). LV switchboard dan UPS untuk Area A melewati setiap fase: persetujuan shop drawing (A-1020), factory testing (A-2010, A-2020), instalasi (A-3030), pre-energization inspection (A-4010), start-up dan functional testing (A-5010), lalu Integrated Systems Testing (A-5050) dan handover. Menelusuri satu keluarga equipment di sepanjang rantai adalah cara yang bagus untuk menemukan logic yang hilang.

## Kesalahan yang Sering Terjadi

- Menganggap commissioning sebagai ekor berdurasi tetap yang diam-diam menyerap keterlambatan dari hulu.
- WBS hanya disusun per area, sehingga system completion tidak terlihat.
- Durasi procurement yang mengabaikan FAT dan receiving inspection.
- Menunda dokumentasi handover sampai minggu-minggu terakhir.
- Menyatakan satu fase selesai tanpa bukti yang dibutuhkan fase berikutnya.

## Konsep Terkait

- [[Commissioning]] — fase yang mengubah fasilitas terpasang menjadi fasilitas terbukti.
- [[Handover]] — kondisi akhir yang menjadi tujuan perencanaan seluruh lifecycle.
- [[Gambaran Umum Project Alpha]] — proyek fiktif yang menjadi ilustrasi setiap fase.

## Referensi

- [[REF-021 ASHRAE Guideline 0 Commissioning Process|REF-021]] — commissioning sebagai proses yang mencakup seluruh proyek, bukan hanya bagian akhirnya.
- [[REF-025 Data Center Commissioning Levels|REF-025]] — pembagian L1–L5 yang dipakai untuk menamai fase-fase testing.
