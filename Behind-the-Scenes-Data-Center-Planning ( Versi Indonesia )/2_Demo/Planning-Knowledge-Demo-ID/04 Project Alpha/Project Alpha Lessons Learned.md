---
type: project-view
domain: project-alpha
project: Project Alpha
fictional: true
tags:
- project-alpha
- fictional
- lessons-learned
data_date: 2030-04-08
---
# Project Alpha Lessons Learned

> [!warning] Data proyek fiktif
> Semua nama proyek, activity, tanggal, quantity, issue dan informasi proyek di Project Alpha adalah fiktif dan dibuat khusus untuk demonstrasi.

Bagian dari [[Gambaran Umum Project Alpha]]

## L-001 — Pastikan akses sebelum me-release instalasi
| Kolom | Isi |
|---|---|
| Yang terjadi | Instalasi Area A sudah punya drawing approved, material sudah delivery, crew sudah mobilisasi dan predecessor sudah selesai — tapi rigging route terhalang scaffold dan lifting permit masih pending. |
| Dampak | Instalasi tidak bisa di-release pada start yang direncanakan, walaupun sebagian besar prerequisite sudah ready. |
| Pelajaran | Readiness akses (rute, rigging, permit) harus diverifikasi sebelum activity instalasi di-release — bukan hanya drawing, material, manpower dan predecessor. |
| Praktik yang disarankan | Masukkan akses dan permit sebagai kolom tersendiri di readiness check untuk setiap activity yang masuk lookahead tiga minggu. |
| Terkait | I-001 · C-003 · [[Electrical Equipment Installation - Area A\|A-3030]] |
| Dinaikkan ke evergreen knowledge | [[Cek Readiness Sebelum Mulai]] |
| Dicatat | 2030-04-06 oleh Project Planner |

## L-002 — Booking inspection di luar window tiga minggu
| Kolom | Isi |
|---|---|
| Yang terjadi | Inspection pihak ketiga sebelum energization butuh pemberitahuan minimal sepuluh hari kerja. Tanggal trigger-nya berada di luar lookahead tiga minggu. |
| Dampak | Booking yang terlambat akan membuat energization menunggu jadwal inspector. |
| Pelajaran | Action yang punya lead time (booking, permit, approval) harus ditarik lebih awal dari horizon yang lebih panjang daripada lookahead tiga minggu. |
| Praktik yang disarankan | Pertahankan lookahead enam minggu untuk trigger lead time, dan pantau tanggal booking sebagai constraint. |
| Terkait | C-009 · A-4010 |
| Dinaikkan ke evergreen knowledge | [[Lookahead Planning]] |
| Dicatat | 2030-04-06 oleh Project Planner |

## L-003 — Sepakati interface vendor sebelum integrasi masuk lookahead
| Kolom | Isi |
|---|---|
| Yang terjadi | Vendor switchboard dan BMS Contractor belum menyepakati EPMS points list, padahal point-to-point check sudah dekat. |
| Dampak | Point-to-point check dan integrasi BMS/EPMS terekspos di path yang float-nya sangat kecil. |
| Pelajaran | Interface antar paket pekerjaan butuh owner dan deliverable yang disepakati sebelum activity testing yang bergantung padanya masuk lookahead. |
| Praktik yang disarankan | Daftarkan deliverable interface (points list, protokol, batas lingkup) di constraint register dengan owner yang jelas. |
| Terkait | I-005 · C-011 · A-4040, A-5040 |
| Dinaikkan ke evergreen knowledge | [[Schedule Paling Sering Pecah di Interface]] |
| Dicatat | 2030-04-06 oleh Project Planner |

## L-004 — Sudah delivery belum berarti siap dipasang
| Kolom | Isi |
|---|---|
| Yang terjadi | Pintu panel UPS yang rusak ditemukan saat receiving inspection, tidak lama sebelum instalasi. |
| Dampak | Penggantinya terpasang tepat waktu, tapi menghabiskan sisa margin sebelum instalasi. |
| Pelajaran | Receiving inspection dan perbaikan kerusakan butuh waktu di schedule antara delivery dan instalasi. |
| Praktik yang disarankan | Jadwalkan receiving inspection secara eksplisit, dan perlakukan equipment yang sudah delivery tapi belum diinspeksi sebagai material constraint. |
| Terkait | I-006 · C-005 · A-2030, [[Electrical Equipment Installation - Area A\|A-3030]] |
| Dinaikkan ke evergreen knowledge | [[Terpasang Belum Tentu Commissioned]] |
| Dicatat | 2030-04-06 oleh Project Planner |

## L-005 — Laporkan pemakaian float walaupun tanggal finish tidak bergeser
| Kolom | Isi |
|---|---|
| Yang terjadi | Keterlambatan delivery generator tidak menggeser Ready for Service, tapi memakan float di path generator. |
| Dampak | Tanpa pelaporan, path tersebut bisa menjadi critical tanpa ada peringatan ke tim. |
| Pelajaran | Pemakaian float adalah sinyal peringatan dini dan harus dilaporkan bersama selisih tanggal. |
| Praktik yang disarankan | Tampilkan tren float untuk path near-critical di setiap catatan weekly planning. |
| Terkait | I-002 · C-002 · A-2050, A-3080 |
| Dinaikkan ke evergreen knowledge | [[Pantau Float, Bukan Hanya Tanggal]] |
| Dicatat | 2030-04-06 oleh Project Planner |

## Dari Pelajaran Proyek ke Evergreen Knowledge

Setiap pelajaran di sini spesifik untuk Project Alpha. Catatan evergreen yang di-link membuatnya lebih umum, sehingga bisa diterapkan di proyek mana pun:

**Pengalaman proyek → pelajaran yang digeneralisasi → evergreen knowledge**

Lihat [[Cek Readiness Sebelum Mulai]] dan [[Pantau Float, Bukan Hanya Tanggal]].
