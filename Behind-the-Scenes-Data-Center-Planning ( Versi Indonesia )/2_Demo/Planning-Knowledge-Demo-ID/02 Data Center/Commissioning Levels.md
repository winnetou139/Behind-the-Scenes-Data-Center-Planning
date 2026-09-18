---
type: concept
domain: data-center
status: evergreen
aliases:
  - L1-L5
  - Commissioning Level
tags:
  - data-center
  - commissioning
  - testing
references:
  - REF-025
  - REF-021
updated: 2026-09-14
---

# Commissioning Levels

> **Intinya:** Commissioning level L1–L5 membagi testing data center menjadi tahapan, mulai dari tes di pabrik sampai Integrated Systems Testing. Setiap level mengasumsikan level sebelumnya sudah selesai untuk system tersebut. Ini konvensi yang umum dipakai, tapi definisi persisnya berbeda-beda antar organisasi.

Bagian dari [[Beranda Pengetahuan Planning]]

## Definisi

Konvensi lima level yang umum, seperti yang saya pakai:

| Level | Nama umum | Activity yang biasa dilakukan | Bukti yang biasa diminta |
|---|---|---|---|
| L1 | Factory witness testing | FAT untuk equipment utama (switchboard, UPS, generator, chiller) sebelum dikirim | Laporan FAT yang disaksikan |
| L2 | Installation verification | Checklist setelah instalasi untuk memastikan pekerjaan sesuai gambar; di banyak proyek juga termasuk receiving inspection, IR testing, pressure testing, flushing dan point-to-point check | Checklist yang sudah ditandatangani, catatan tes |
| L3 | Start-up | Checklist start-up dan functional dari pabrikan untuk tiap equipment; energization atau running pertama; setting awal | Laporan start-up, checklist lengkap |
| L4 | System testing | Tiap system dites sendiri-sendiri melalui mode operasi, sequence dan alarm — misalnya load bank test untuk generator, UPS dan baterai | Script functional test yang sudah lengkap |
| L5 | Integrated Systems Testing | Semua system dites bersamaan dengan beban simulasi dan skenario kegagalan | Laporan IST |

**Penamaan tidak seragam** — REF-025 sendiri menyebutkan bahwa tiap organisasi mendefinisikan level secara berbeda. Ada yang mendefinisikan L1 sebagai review desain dan submittal, bukan FAT. Ada yang menggabungkan L3 dan L4 menjadi satu tahap "start-up dan functional". Ada yang memberi tag warna untuk tiap level, tapi warnanya tidak standar. Level ini adalah konvensi, bukan satu standar wajib — jadi saya selalu cek definisinya di commissioning plan proyek sebelum saya memberi kode di schedule.

## Kenapa Penting

Level memberi commissioning struktur yang bisa dijadwalkan dan diukur oleh planner. Setiap level adalah gate (pintu pemeriksaan): L4 pada suatu system tidak boleh mulai sebelum L3 system itu selesai, dan L5 tidak boleh mulai sebelum L4 selesai untuk semua system dalam scope. Hasilnya: logic yang jelas, kriteria readiness yang jelas, dan cara yang jelas untuk melaporkan progress. REF-025 juga menegaskan bahwa ketelitian commissioning tidak ada hubungannya dengan Tier rating: scope-nya mungkin lebih kecil di fasilitas yang lebih sederhana, tapi testing-nya harus tetap sama teliti.

## Sudut Pandang Planner

- Saya menambahkan activity code untuk commissioning level, supaya schedule bisa difilter dan dikelompokkan per level.
- Saya memantau **matriks system × level**: baris adalah system, kolom adalah L1 sampai L5. Dari situ langsung kelihatan system mana yang menahan level berikutnya.
- Saya cek logic per system: setiap activity L3 harus terhubung ke inspeksi L2-nya, setiap L4 ke L3-nya.
- Level 2 tumpang tindih dengan konstruksi; saya tidak membiarkan progress konstruksi dianggap sebagai bukti L2.
- Kalau level digabung (misalnya L3/L4), saya tetap tanya bukti start-up apa yang sudah ada sebelum functional testing dimulai.

## Contoh Praktis

[[Project Alpha Schedule]] (fiktif) memakai konvensi ini dengan L3 dan L4 digabung. L1 adalah factory testing untuk LV switchboard dan UPS (A-2010, A-2020). L2 mencakup pre-energization inspection dan IR testing (A-4010) serta pressure testing dan flushing chilled water (A-4030), dengan BMS/EPMS point-to-point check (A-4040) di fase inspeksi yang sama. L3/L4 adalah start-up dan functional testing untuk UPS dan switchboard, chiller dan CRAH, serta load bank testing generator (A-5010, A-5020, A-5030). L5 adalah Integrated Systems Testing untuk Data Hall 1 (A-5050).

## Kesalahan yang Sering Terjadi

- Mengira semua orang di proyek punya pengertian yang sama tentang "L3".
- Melewati atau menggabungkan level di tengah proyek untuk mengejar waktu, lalu defect baru ketahuan saat IST.
- Melaporkan satu level selesai untuk suatu area padahal ada satu system di dalamnya yang masih tertinggal.
- Tidak ada kode level di schedule, sehingga matriks harus dibuat ulang manual setiap minggu.

## Konsep Terkait

- [[Commissioning]] — proses yang distrukturkan oleh level-level ini.
- [[Integrated Systems Testing]] — Level 5, gate terakhir sebelum handover.
- [[Project Alpha Schedule]] — schedule fiktif yang diberi kode L1 sampai L5.

## Referensi

- [[REF-025 Data Center Commissioning Levels|REF-025]] — konvensi L1–L5 dan scope yang biasa untuk tiap level.
- [[REF-021 ASHRAE Guideline 0 Commissioning Process|REF-021]] — proses commissioning secara umum yang menjadi wadah level-level ini.
