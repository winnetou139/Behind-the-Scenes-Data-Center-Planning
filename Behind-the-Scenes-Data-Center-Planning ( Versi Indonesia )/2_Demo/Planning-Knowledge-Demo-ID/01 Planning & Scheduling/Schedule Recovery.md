---
type: concept
domain: planning
status: evergreen
aliases:
  - Recovery Plan
tags:
  - recovery
  - delay
  - float
  - scheduling
references:
  - REF-001
  - REF-009
updated: 2026-09-14
---

# Schedule Recovery

> **Intinya:** Schedule recovery adalah rencana yang disengaja dan berbasis bukti untuk merebut kembali waktu yang hilang di critical path dan near-critical path, dengan mengubah cara, waktu atau sumber daya untuk sisa pekerjaan — tanpa menciptakan risiko yang lebih besar dari delay itu sendiri.

Bagian dari [[Planning & Scheduling MOC]]

## Definisi
Recovery plan adalah respons terhadap [[Schedule Delay]] yang sudah memakan, atau diperkirakan akan memakan, [[Total Float]] yang melindungi milestone penting. Recovery plan mengubah sisa pekerjaan — logic, resource, metode, jam kerja atau pentahapan — supaya forecast kembali ke target, atau sedekat mungkin dengan yang disepakati para pihak.

Recovery adalah **rencananya**. [[Acceleration]] adalah salah satu cara menjalankannya: mengerjakan pekerjaan lebih cepat, biasanya dengan biaya tambahan. Banyak recovery sama sekali tidak butuh acceleration — menyelesaikan constraint dua minggu lebih awal bisa merebut kembali waktu dengan biaya hampir nol.

## Kenapa Penting
Hanya waktu yang direbut kembali di [[Critical Path]] yang menggeser forecast. Upaya di tempat lain terasa produktif tapi tidak mengubah apa-apa. Recovery plan yang tidak diuji dengan baik lebih buruk daripada tidak ada: menciptakan rasa aman palsu, menumpuk trade di satu area, dan diam-diam bisa membuat near-critical path jadi critical.

## Pendekatan Recovery Utama
1. **Resequence pekerjaan (ubah logic bila secara teknis valid)** — ubah urutan untuk membebaskan driving path. *Hati-hati:* menghapus preferential logic tanpa mengecek alasan teknis atau keselamatan kenapa logic itu dibuat.
2. **Kerjakan activity secara paralel (fast-tracking)** — tumpang-tindihkan pekerjaan yang direncanakan berurutan. *Hati-hati:* rework dan kepadatan saat pekerjaan yang ditumpuk butuh informasi atau ruang yang belum tersedia.
3. **Tambah resource atau crew (crashing)** — perpendek activity driving dengan lebih banyak orang atau alat. *Hati-hati:* hasil yang makin berkurang di ruangan sempit; electrical room hanya muat sejumlah crew tertentu.
4. **Jam kerja diperpanjang atau shift tambahan** — lebih banyak waktu kerja per hari kalender. *Hati-hati:* kelelahan, ketersediaan supervisi dan inspeksi, dan penurunan produktivitas kalau dilakukan terus-menerus.
5. **Selesaikan constraint lebih awal** — majukan izin, akses, inspeksi, pengiriman dan approval. *Hati-hati:* ketergantungan pada pihak ketiga; pastikan komitmennya, jangan diasumsikan.
6. **Rencanakan ulang duration — hanya dengan bukti** — revisi remaining duration kalau data produktivitas atau perubahan metode mendukungnya. *Hati-hati:* duration yang optimistis hanya merebut kembali waktu di atas kertas.
7. **Metode alternatif atau prefabrikasi** — perakitan di luar site, equipment skid-mounted, metode instalasi yang berbeda. *Hati-hati:* lead time desain, approval dan procurement yang lebih lama dari waktu yang dihemat.
8. **Pentahapan scope atau handover parsial berdasarkan kesepakatan** — tahapkan penyelesaian supaya area atau sistem prioritas selesai lebih dulu. *Hati-hati:* butuh persetujuan client dan batas commissioning yang jelas; bisa mempersulit testing dan handover.

Recovery plan yang nyata biasanya menggabungkan beberapa pendekatan. Saya mempertimbangkannya kurang lebih sesuai urutan ini: yang murah dan berisiko rendah dulu.

## Mereview Recovery Plan
- [ ] Logic masih valid secara teknis; tidak ada open end atau date constraint tanpa alasan yang ditambahkan.
- [ ] Resource realistis — crew, supervisi dan alat benar-benar tersedia, tidak ada penumpukan trade di satu area.
- [ ] Keselamatan sudah direview: kepadatan, lifting, kerja malam, kelelahan, izin.
- [ ] Persetujuan biaya dan komersial sudah didapat — siapa yang bayar, berdasarkan instruksi apa.
- [ ] Near-critical path dicek ulang: apakah recovery membuat path lain jadi critical?
- [ ] Asumsi terdokumentasi: tingkat produktivitas, pola shift, tanggal pengiriman dan akses.
- [ ] Milestone antara yang terukur sudah ditetapkan supaya progress bisa dipantau mingguan.
- [ ] Stakeholder berkomitmen: subcontractor, supplier, inspektor dan client sudah menyetujui bagian masing-masing.
- [ ] Sudah dibandingkan dengan [[Baseline]] dan update terakhir, dengan daftar perubahan.
- [ ] Risk register di-update untuk risiko yang muncul dari rencana itu sendiri.
- [ ] Dampak ke testing, [[Commissioning]] dan [[Integrated Systems Testing]] sudah dicek, bukan hanya konstruksi.
- [ ] Keputusan dan persetujuan sudah dicatat.

## Sudut Pandang Planner
Sebelum menyentuh schedule, saya bertanya apa penyebab delay dan apakah penyebab itu masih aktif. Merebut kembali waktu sementara constraint-nya masih ada hanya memindahkan masalah. Lalu saya cari waktu yang tidak butuh biaya — constraint dan urutan — sebelum mengusulkan crew atau shift.

Saya menyajikan beberapa opsi lengkap dengan trade-off-nya, bukan satu jawaban. Keputusan ada di tim project; tugas saya menunjukkan apa yang benar-benar didapat dari setiap opsi.

## Contoh Praktis
Di project fiktif ini, A-3030 tidak bisa mulai karena akses terhalang. Langkah pertama bukan acceleration, melainkan menyelesaikan constraint — membersihkan jalur rigging yang terhalang scaffold façade dan mengamankan izin lifting (lihat [[Cek Readiness Sebelum Mulai]] dan [[Constraint Register]]). Sebagai contingency, tim menyiapkan cable pulling dengan jam kerja diperpanjang atau shift kedua kalau start Area A slip, untuk melindungi energization dan IST. Pilihan itu dan pemicunya dicatat di [[Decision Log]]. Sebaliknya, path generator cukup dimonitor, tidak perlu recovery, karena slip-nya tidak menggeser finish ([[Pantau Float, Bukan Hanya Tanggal]]).

## Kesalahan yang Sering Terjadi
- Recovery di atas kertas dengan memperpendek duration tanpa bukti.
- Menyasar activity yang tidak ada di critical path.
- Menumpuk crew di satu ruangan dan kehilangan produktivitas lebih banyak dari yang didapat.
- Mengabaikan critical path baru yang tercipta akibat recovery.
- Tidak ada persetujuan, tidak ada asumsi yang dicatat, tidak ada milestone untuk memantau.

## Konsep Terkait
- [[Critical Path]] — recovery hanya ada hasilnya di driving path.
- [[Total Float]] — recovery bertujuan memulihkan float ke milestone penting.
- [[Schedule Delay]] — alasan recovery plan dibuat.
- [[Acceleration]] — salah satu cara menjalankan recovery, biasanya mahal.
- [[Constraints]] — menyelesaikan readiness constraint lebih awal sering jadi recovery yang paling murah.
- [[Lookahead Planning]] — tempat tindakan recovery disiapkan dan dipantau mingguan.
- [[Forecasting]] — menunjukkan apakah recovery benar-benar berhasil.
- [[Pantau Float, Bukan Hanya Tanggal]] — tren float menunjukkan kapan recovery dibutuhkan.

## Referensi
- [[REF-001 GAO Schedule Assessment Guide|REF-001]] — strategi recovery dan acceleration (crashing, fast tracking, lembur, review constraint dan lag, pengurangan scope), fokus pada activity critical.
- [[REF-009 LCI Last Planner System|REF-009]] — make-ready dan penyelesaian constraint sebagai tuas recovery yang praktis.
