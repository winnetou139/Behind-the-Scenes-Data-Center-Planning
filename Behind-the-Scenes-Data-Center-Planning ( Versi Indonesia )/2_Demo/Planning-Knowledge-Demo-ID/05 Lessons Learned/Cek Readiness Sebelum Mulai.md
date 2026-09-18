---
type: lesson
domain: planning
status: evergreen
aliases:
  - Ready Means All Prerequisites
tags:
  - lessons-learned
  - readiness
  - constraints
references:
  - REF-009
  - REF-010
updated: 2026-09-14
---

# Cek Readiness Sebelum Mulai
> **Intinya:** Readiness harus dinilai untuk setiap prerequisite sebuah activity — bukan disimpulkan dari tanggal start activity itu, atau dari sebagian besar prerequisite yang sudah ready.

Bagian dari [[Beranda Pengetahuan Planning]]

## Pelajarannya

Tanggal di schedule menunjukkan kapan activity *seharusnya* mulai. Tanggal itu tidak menunjukkan apakah activity *bisa* mulai. Sebelum melepas pekerjaan, saya mengecek setiap prerequisite satu per satu:

| Prerequisite | Pertanyaan saya |
|---|---|
| Gambar | Apakah revisi yang sudah approved ada di site dan dipegang crew? |
| Material | Apakah sudah dikirim, diinspeksi, dan bisa dijangkau — bukan sekadar "sudah datang"? |
| Akses | Bisakah orang dan alat benar-benar mencapai lokasi kerja? Apakah permit sudah approved? |
| Predecessor | Apakah pekerjaan sebelumnya benar-benar selesai, bukan "hampir"? |
| Manpower | Apakah crew yang tepat sudah dikonfirmasi untuk hari yang tepat? |
| Inspeksi | Apakah hold point dan witness sudah dijadwalkan? |
| Interface | Apakah pihak lain sudah menyerahkan apa yang kita butuhkan? |

**Kalau empat dari lima prerequisite sudah ready, activity itu belum ready.** Readiness adalah logika AND, bukan rata-rata.

## Kenapa Berlaku di Project Lain

- Start yang baru sebagian ready biasanya berubah jadi activity yang jalan-berhenti: double handling, crew menganggur, dan produktivitas turun.
- Mulai "supaya kelihatan ada progress" bisa menyembunyikan constraint yang sebenarnya sampai constraint itu mengenai critical path.
- Waktu termurah untuk menghilangkan constraint adalah beberapa minggu sebelum tanggal start — dan itulah fungsi [[Lookahead Planning]].

## Asal Pelajaran Ini

Di Project Alpha yang fiktif, instalasi equipment Area A sudah punya gambar approved, equipment sudah dikirim, crew sudah mobilisasi, dan predecessor sudah selesai — tapi jalur rigging tertutup dan lifting permit masih pending. Lihat [[Electrical Equipment Installation - Area A]] dan lesson L-001 di [[Project Alpha Lessons Learned]].

## Cara Saya Menerapkannya

1. Setiap activity yang masuk ke lookahead tiga minggu dicek readiness-nya berdasarkan kategori di atas.
2. Apa pun yang "belum ready" menjadi constraint bernama, dengan owner dan tanggal required-by di constraint register.
3. Rapat koordinasi mingguan membahas constraint, bukan hanya progress.
4. Activity hanya dilepas kalau semua prerequisite sudah ready — atau kalau ada partial scope yang aman, terdokumentasi, dan sudah disepakati.

## Konsep Terkait

- [[Constraints]] — kategori yang dipakai dalam readiness check
- [[Lookahead Planning]] — rentang waktu tempat readiness dicek
- [[Critical Path]] — kenapa "belum ready" di satu lokasi bisa menjadi delay project
- [[Schedule Recovery]] — menghilangkan constraint sejak awal sering jadi recovery termurah

## Referensi

- [[REF-009 LCI Last Planner System|REF-009]] — make-ready planning dan analisis constraint dalam lookahead planning
- [[REF-010 Ballard 2000 Last Planner Thesis|REF-010]] — asal proses make-ready dan penyaringan penugasan sebelum dilepas
