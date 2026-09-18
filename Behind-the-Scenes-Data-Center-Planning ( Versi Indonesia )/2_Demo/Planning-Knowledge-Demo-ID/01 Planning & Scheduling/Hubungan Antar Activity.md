---
type: concept
domain: planning
status: evergreen
aliases:
  - Relationships
  - Schedule Logic
tags:
  - scheduling
  - cpm
  - schedule-quality
references:
  - REF-001
updated: 2026-09-14
---

# Hubungan Antar Activity
> **Intinya:** Activity relationship (logic schedule) menentukan bagaimana activity saling bergantung — finish-to-start, start-to-start, finish-to-finish atau start-to-finish, dengan lag bila perlu — supaya tanggal dihitung oleh network, bukan diketik manual.

Bagian dari [[Planning & Scheduling MOC]]

## Definisi

| Tipe | Arti | Penggunaan umum |
|---|---|---|
| Finish-to-Start (FS) | Successor bisa mulai setelah predecessor selesai | Sebagian besar urutan pekerjaan konstruksi |
| Start-to-Start (SS) | Successor bisa mulai setelah predecessor sudah mulai (sering dengan lag) | Pekerjaan yang tumpang tindih, misalnya cable pulling setelah section switchboard pertama terpasang |
| Finish-to-Finish (FF) | Successor bisa selesai setelah predecessor selesai | Pekerjaan susulan, misalnya labelling yang baru bisa selesai kalau termination sudah selesai |
| Start-to-Finish (SF) | Successor bisa selesai setelah predecessor mulai | Jarang; misalnya cooling sementara tidak boleh dibongkar sebelum cooling permanen mulai beroperasi |

**Lag** adalah waktu tunggu di antara dua titik yang di-link; **lead** adalah lag negatif. Lag dihitung berdasarkan calendar, dan P6 membiarkan kita memilih calendar yang mana — ini sering bikin kaget kalau activity 6 hari kerja di-link ke activity 5 hari kerja.

**Open end** adalah activity tanpa predecessor (open start) atau tanpa successor (open finish), selain milestone start dan finish project. Open end merusak perhitungan float: activity tanpa successor bisa menunjukkan float besar yang tidak ada artinya.

## Kenapa Logic Lebih Baik daripada Date Constraint
Hard date constraint — seperti Mandatory Start atau Finish On or Before — mengunci atau membatasi tanggal apa pun yang terjadi pada predecessor. Akibatnya schedule bisa menampilkan tanggal yang secara fisik sudah tidak mungkin, dan float jadi terdistorsi. Soft constraint seperti "Start On or After", kalau dipakai untuk menggantikan predecessor yang hilang, juga menyembunyikan ketergantungan yang sebenarnya: kalau predecessor aslinya slip, tidak ada yang bergeser. Logic menggeser activity saat predecessor-nya bergeser, sehingga delay merambat dan schedule menunjukkan kondisi yang sebenarnya. Date constraint tetap ada tempatnya — milestone kontrak, tanggal eksternal — tapi jumlahnya harus sedikit dan ada alasannya. Lihat [[Constraints]] untuk dua arti dari kata tersebut.

## Kenapa Penting
Logic adalah yang membuat Critical Path Method bisa bekerja. Tanpa logic yang lengkap, tidak ada [[Critical Path]] yang bisa dipercaya, tidak ada [[Total Float]] yang bermakna, dan tidak ada analisis delay yang kredibel. Karena itu assessment gaya DCMA mengecek missing logic, lead, lag, tipe relationship dan hard constraint.

## Sudut Pandang Planner
Saat mereview schedule orang lain, saya cek logic dulu sebelum tanggal:
- Apakah setiap activity punya minimal satu predecessor dan satu successor?
- Apakah ada link SS tanpa apa pun yang mengontrol finish successor-nya, sehingga activity itu "mengambang"?
- Apakah ada lag yang sebenarnya mewakili pekerjaan atau waktu tunggu — curing, approval, inspeksi? Kalau ada orang yang harus mengelolanya, saya jadikan activity.
- Apakah ada lead? Hampir selalu saya hapus.
- Apakah logic lintas disiplin sudah ada di tempat yang memang pekerjaannya saling bergantung?

## Contoh Praktis
Di [[Project Alpha Schedule]] (fiktif), mechanical functional testing (A-5020) punya ketergantungan finish-to-start ke energization permanent power (A-4020). Satu link lintas disiplin itulah yang membuat masalah akses di electrical room Area A bisa berdampak ke testing chiller dan CRAH. Tanpa link itu, tim mechanical akan mengira mereka punya float yang sebenarnya tidak ada. Lihat [[Schedule Paling Sering Pecah di Interface]].

## Kesalahan yang Sering Terjadi
- Memakai constraint "Start On or After" alih-alih me-link ke predecessor yang sebenarnya.
- Rantai yang hanya pakai SS dengan finish yang terbuka.
- Lag panjang yang menyembunyikan approval atau inspeksi, lalu tidak ada yang mengelolanya.
- Link berlebih (A→B→C ditambah A→C) yang membuat network berantakan dan review jadi lebih sulit.
- Hanya me-link di dalam satu disiplin dan melewatkan interface dengan trade lain, utilitas dan commissioning.

## Konsep Terkait
- [[Total Float]] — open end dan date constraint mendistorsi float.
- [[Constraints]] — date constraint vs logic, dan readiness constraint.
- [[Critical Path]] — logic yang rusak menghasilkan critical path yang salah.
- [[Pengecekan Kualitas Schedule]] — pengecekan logic dalam assessment gaya DCMA.
- [[Schedule Paling Sering Pecah di Interface]] — link lintas disiplin adalah tempat logic paling sering hilang.

## Referensi
- [[REF-001 GAO Schedule Assessment Guide|REF-001]] — mengurutkan semua activity dengan logic, bukan dengan constraint.
