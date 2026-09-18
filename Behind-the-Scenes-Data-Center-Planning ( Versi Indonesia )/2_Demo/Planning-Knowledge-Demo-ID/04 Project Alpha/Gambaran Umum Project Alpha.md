---
type: project-view
domain: project-alpha
project: Project Alpha
fictional: true
tags:
- project-alpha
- fictional
data_date: 2030-04-08
---
# Gambaran Umum Project Alpha
> [!warning] Data proyek fiktif
> Semua nama proyek, activity, tanggal, quantity, issue dan informasi proyek di Project Alpha adalah fiktif dan dibuat khusus untuk demonstrasi.

Bagian dari [[Beranda Pengetahuan Planning]]

## Identitas
| Kolom | Isi |
|---|---|
| Nama | Project Alpha |
| Nama lengkap | Project Alpha — Hypothetical Data Center Development |
| Lingkup yang ditampilkan | Potongan demonstrasi Phase 1 — pekerjaan yang dibutuhkan untuk membawa Data Hall 1 di sebuah gedung data center hipotetis sampai Ready for Service. Sengaja disederhanakan: sekitar 30 activity, bukan ribuan seperti di program nyata. |
| Tipe fasilitas | Data center tipe colocation (hipotetis) |
| Kapasitas IT Phase 1 | Beban IT 4 MW (fiktif) |
| Konsep redundansi | N+1 mekanikal, distribusi UPS 2N (hanya ilustrasi) |
| Start proyek | 2030-01-07 |
| Data date | 2030-04-08 (Week 14) |
| Ready for Service — baseline | 2030-07-03 |
| Ready for Service — forecast saat ini | 2030-07-03 |
| Kalender | Kalender site enam hari (Sen, Sel, Rab, Kam, Jum, Sab); durasi dalam hari kerja |

## Area
| Area | Nama | Deskripsi |
|---|---|---|
| [[Area A - LV Electrical Room\|Area A]] | LV Electrical Room | Berisi LV main switchboard dan modul UPS yang menyuplai Data Hall 1. |
| Area B | Data Hall 1 | White space dengan unit CRAH, busway dan distribusi daya rack. |
| Area C | Mechanical Plant Yard | Air-cooled chiller, pompa dan header chilled water. |
| Area D | Generator Yard | Standby diesel generator dan sistem bahan bakar. |
| Off-site | Factory / Supplier Works | Manufaktur dan factory acceptance testing. |
| Site-wide | Site-wide | Activity yang tidak terikat pada satu area. |

## Sistem
**Elektrikal**: LV main switchboard (MSB); modul UPS dan kabinet baterai; busway dan kabel LV ke Data Hall 1; standby diesel generator; EPMS (electrical power monitoring system)

**Mekanikal & kontrol**: Air-cooled chiller; pipa dan pompa chilled water; unit CRAH di Data Hall 1; BMS (building management system)

## Ringkasan Schedule
| Ukuran | Nilai |
|---|---|
| Activity (termasuk milestone) | 30 |
| Complete / In Progress / Not Started | 9 / 3 / 18 |
| Critical path (total float ≤ 0) | [[Electrical Equipment Installation - Area A\|A-3030]] → A-3040 → A-3050 → A-4010 → A-4020 → A-5010 → A-5020 → A-5050 → A-6010 → M-9000 |
| Open constraint | 10 dari 14 |
| Open issue | 5 dari 6 |
| Decision tercatat | 6 |
| Lesson learned proyek tercatat | 5 |

## Siklus Proyek
| Fase | Nama | Deskripsi | Activity |
|---|---|---|---|
| ENG | Engineering | Desain IFC, shop drawing dan approval. | 4 |
| PROC | Procurement | Manufaktur, factory acceptance testing (Level 1) dan delivery. | 5 |
| CON | Construction | Finishing ruangan, containment, setting equipment, piping, cabling. | 9 |
| INSP | Inspection & Testing | Pre-energization inspection, pressure testing, point-to-point check (Level 2). | 4 |
| CX | Commissioning | Start-up dan functional testing (Level 3–4) serta Integrated Systems Testing (Level 5). | 5 |
| HO | Handover | Closeout punch list, dokumentasi O&M, training, Ready for Service. | 3 |

## Asumsi
- Activity yang sudah complete diasumsikan start dan finish sesuai tanggal baseline, kecuali ada catatan.
- Semua relationship adalah Finish-to-Start kecuali disebutkan lain (SS = Start-to-Start dengan lag dalam hari kerja).
- Total float diukur terhadap baseline finish M-9000 (target Ready for Service).
- Level commissioning mengikuti konvensi umum L1–L5; penamaannya bisa berbeda antar organisasi.
- Constraint status pada activity DITURUNKAN dari constraints.csv, tidak pernah disimpan di activities.csv.

## View Project Alpha
- [[Project Alpha Schedule]] — semua activity, logic, float dan tampilan Gantt
- [[Area A - LV Electrical Room]] dan [[Electrical Equipment Installation - Area A]] — area dan activity utama
- [[Constraint Register]] · [[Weekly Planning - Week 14]] · [[Notulen Rapat Koordinasi Mingguan - Week 13]]
- [[Issue Log]] · [[Decision Log]] · [[Project Alpha Lessons Learned]]

## Interpretasi

Project Alpha adalah sandbox saya: potongan kecil dan fiktif dari proyek data center, sengaja dibuat untuk menguji ide planning tanpa menyentuh informasi proyek nyata.

Yang diilustrasikan:

- Schedule adalah model tentang *bagaimana pekerjaan menjadi bisa dikerjakan*, bukan sekadar daftar tanggal.
- Path menuju Ready for Service melewati energization dan commissioning. Jadi readiness elektrikal menggerakkan semua pekerjaan di hilirnya — lihat [[Critical Path]] dan [[Commissioning]].
- Sebagian besar upaya planning mingguan dipakai untuk menghilangkan [[Constraints]], bukan menggambar ulang bar.

Mulai dari [[Electrical Equipment Installation - Area A]] — activity yang dipakai dalam presentasi.
