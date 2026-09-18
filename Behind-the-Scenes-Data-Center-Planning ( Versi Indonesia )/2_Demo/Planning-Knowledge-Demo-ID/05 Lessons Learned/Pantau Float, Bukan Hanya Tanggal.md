---
type: lesson
domain: planning
status: evergreen
aliases:
  - Float Erosion Is an Early Warning
tags:
  - lessons-learned
  - float
  - forecasting
references:
  - REF-001
updated: 2026-09-14
---

# Pantau Float, Bukan Hanya Tanggal
> **Intinya:** Delay yang tidak menggeser tanggal finish tetap bisa memakan float — dan float yang terpakai adalah peringatan paling awal bahwa sebuah path mulai menjadi critical.

Bagian dari [[Beranda Pengetahuan Planning]]

## Pelajarannya

Saat activity yang tidak critical mundur, tanggal finish project sering tetap sama. Godaannya adalah melaporkan "tidak ada dampak". Padahal keterlambatan itu sudah memakai sebagian [[Total Float]] di path tersebut. Kalau terulang beberapa kali, path yang tadinya longgar diam-diam menjadi near-critical, lalu critical — tanpa ada laporan yang menunjukkan perubahan tanggal sampai semuanya sudah terlambat.

## Kenapa Berlaku di Project Lain

- Laporan variance tanggal membandingkan tanggal; laporan itu tidak menunjukkan *sisa margin*.
- Beberapa path near-critical sekaligus bisa lebih berisiko daripada satu critical path.
- Float dipakai oleh semua pihak di satu path, jadi pihak pertama yang memakainya jarang merasakan akibatnya.

## Asal Pelajaran Ini

Di Project Alpha yang fiktif, delivery generator mundur setelah ada QA hold dari supplier. Ready for Service tidak bergeser, dan tim memutuskan untuk tidak melakukan acceleration — tapi keterlambatan itu memakan float di path generator, sementara path chiller sudah near-critical. Lihat lesson L-005 di [[Project Alpha Lessons Learned]], decision D-005 di [[Decision Log]], dan float watch di [[Weekly Planning - Week 14]].

## Cara Saya Menerapkannya

- Sertakan **float watch** di setiap update: activity dengan total float di bawah atau sama dengan threshold tertentu, dikelompokkan per path.
- Laporkan **tren float** per path (update ini vs update sebelumnya), bukan hanya variance finish.
- Anggap negative float sebagai masalah forecast yang harus dijelaskan, bukan angka untuk disembunyikan dengan constraint.
- Saat melakukan recovery waktu, cek bahwa recovery itu tidak sekadar memindahkan status critical ke path lain.

| Laporan bilang | Yang juga saya tanyakan |
|---|---|
| "Finish tidak berubah" | Path mana yang kehilangan float, dan berapa banyak? |
| "Activity tidak critical" | Seberapa dekat ke critical — dan trennya ke arah mana? |
| "Recovery dua minggu" | Path lain mana yang jadi critical akibatnya? |

## Konsep Terkait

- [[Total Float]] — ukuran yang dipantau
- [[Critical Path]] — path near-critical bisa mengambil alih
- [[Forecasting]] — tren float membantu forecast yang kredibel
- [[Schedule Delay]] — delay di activity non-critical tetap penting
- [[Schedule Recovery]] — recovery bisa memindahkan status critical

## Referensi

- [[REF-001 GAO Schedule Assessment Guide|REF-001]] — total float, critical path, dan memantau kesehatan schedule dari update ke update
