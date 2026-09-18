---
type: concept
domain: data-center
status: evergreen
tags:
  - handover
  - data-center
  - commissioning
references:
  - REF-021
  - REF-025
updated: 2026-09-14
---

# Handover

> **Intinya:** Handover adalah penyerahan formal fasilitas yang sudah di-commissioning kepada owner dan operator — punch list ditutup atau disepakati, manual O&M dan as-built diserahkan, operator dilatih, garansi sudah berlaku — sehingga fasilitas bisa dinyatakan Ready for Service.

Bagian dari [[Beranda Pengetahuan Planning]]

## Definisi

Handover adalah titik di mana tanggung jawab atas fasilitas berpindah dari tim pelaksana ke orang-orang yang akan menjalankannya. Di data center, ini biasanya bersamaan dengan **Ready for Service (RFS)**: fasilitas, atau satu data hall, sudah bisa menerima beban IT pelanggan.

Yang biasanya harus diserahkan:

| Deliverable | Apa itu |
|---|---|
| Penutupan punch list | Defect yang tersisa sudah ditutup, atau ada daftar sisa yang disepakati lengkap dengan penanggung jawab dan tanggal |
| Manual O&M | Informasi operasi dan maintenance untuk setiap system dan equipment utama |
| Gambar as-built | Gambar yang diperbarui sesuai dengan yang benar-benar terpasang |
| Catatan tes dan commissioning | Laporan FAT, catatan L2, start-up, functional dan IST |
| Pelatihan | Operator dilatih untuk system yang terpasang, sering bersama vendor |
| Garansi dan spare part | Sertifikat garansi, tanggal mulai, spare part dan alat khusus |
| Sertifikat dan persetujuan | Pengesahan dari otoritas dan peraturan yang wajib untuk menempati dan mengoperasikan |

Scope persisnya, dan perbedaan antara practical completion, handover dan RFS, tergantung kontrak.

## Kenapa Penting

RFS adalah milestone bisnis — saat itulah pendapatan bisa mulai masuk. Tapi operator tidak bisa menjalankan fasilitas mission-critical dengan aman tanpa dokumentasi, pelatihan dan daftar yang jelas tentang apa yang masih terbuka. Handover yang terburu-buru memindahkan risiko dari tim konstruksi ke tim operasi, tepat saat fasilitas mulai memikul beban live.

## Sudut Pandang Planner

Yang saya pantau di bagian handover dalam schedule:

- **Dokumen sebagai deliverable bertahap.** Manual O&M dan as-built dibuat selama konstruksi dan commissioning, dengan siklus review, bukan disusun di minggu-minggu terakhir.
- **Tren punch list.** Item baru yang muncul selama functional testing dan IST, item yang ditutup per minggu, dan item yang menghalangi RFS.
- **Logic pelatihan.** Pelatihan butuh system dalam konfigurasi final dan operator yang tersedia — jadi pelatihan menyusul commissioning, tapi pemesanan jadwal dan materinya tidak boleh menunggu.
- **Mulai berlakunya garansi.** Kapan garansi mulai tergantung kontrak; saya pastikan tanggal handover yang dicatat adalah tanggal yang dipakai kontrak.
- **Handover bertahap.** Kalau data hall berikutnya dibangun di sebelah hall yang sudah live, setiap handover mengubah aturan akses dan izin di site.

## Contoh Praktis

Di [[Gambaran Umum Project Alpha|Project Alpha]], setelah Integrated Systems Testing untuk Data Hall 1 (A-5050), dua activity handover berjalan paralel: penutupan punch list dan dokumentasi O&M (A-6010), serta pelatihan operator dan dokumentasi handover (A-6020). Keduanya menjadi masukan milestone Data Hall 1 Ready for Service (M-9000). Handover juga momen yang pas untuk mencatat pelajaran di [[Project Alpha Lessons Learned]].

## Kesalahan yang Sering Terjadi

- Manual O&M dan as-built baru dikerjakan setelah IST.
- Pelatihan diberikan sebelum setting dan sequence final.
- Punch item yang muncul saat IST tidak dikategorikan, sehingga tidak jelas mana yang menghalangi RFS.
- Menyatakan RFS dengan item terbuka yang tidak dicatat.
- Staf operasi baru pertama kali melihat fasilitas saat handover.

## Konsep Terkait

- [[Integrated Systems Testing]] — hasil IST dan item yang masih terbuka menjadi masukan handover.
- [[Commissioning]] — catatan commissioning dan pelatihan adalah deliverable handover.
- [[Data Center Project Lifecycle]] — handover adalah kondisi akhir yang menjadi tujuan perencanaan lifecycle.

## Referensi

- [[REF-021 ASHRAE Guideline 0 Commissioning Process|REF-021]] — scope commissioning yang berlanjut melewati konstruksi sampai masa hunian dan garansi.
- [[REF-025 Data Center Commissioning Levels|REF-025]] — handover setelah seluruh commissioning level selesai.
