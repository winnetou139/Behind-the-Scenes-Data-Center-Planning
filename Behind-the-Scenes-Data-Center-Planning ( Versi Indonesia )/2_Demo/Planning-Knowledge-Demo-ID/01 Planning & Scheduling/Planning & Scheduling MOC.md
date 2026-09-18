---
type: moc
domain: planning
status: evergreen
tags:
  - planning
  - scheduling
updated: 2026-09-14
---

# Planning & Scheduling MOC

> **Intinya:** Peta note planning dan scheduling saya — bagaimana schedule dibangun, dianalisis, dijaga tetap hidup, dan apa yang dilakukan saat ada masalah.

Kembali ke: [[Beranda Pengetahuan Planning]]

Note-note ini adalah inti cara kerja saya sebagai planner di proyek konstruksi data center. Kurang lebih bisa dibaca sesuai urutan di bawah, tapi setiap note bisa berdiri sendiri. Kalau sebuah konsep muncul di Project Alpha (fiktif), note-nya memberi link ke tampilan project, bukan mengulang fakta project.

## Dasar-Dasar
- [[Baseline]] — rencana yang sudah approved dan dibekukan, sebagai acuan untuk mengukur progress dan delay.

## Logic & Analisis Schedule
- [[Hubungan Antar Activity]] — FS, SS, FF, SF, lag dan lead, serta kenapa logic lebih baik daripada date constraint.
- [[Critical Path]] — longest path vs total float terendah, near-critical path, dan kenapa "critical" tidak sama dengan "penting".
- [[Total Float]] — total float dan free float, float negatif, dan erosi float sebagai peringatan dini.

## Menjaga Schedule Tetap Hidup
- [[Lookahead Planning]] — horizon tiga dan enam minggu, make-ready dan weekly work plan.
- [[Constraints]] — readiness constraint vs date constraint di software, dan cek readiness.

## Saat Ada Masalah
- [[Schedule Delay]] — delay vs disruption, delay critical vs non-critical, dan kenapa catatan itu penting.
- [[Schedule Recovery]] — pendekatan recovery utama dan cara saya mereview recovery plan.
- [[Acceleration]] — mengerjakan pekerjaan lebih cepat dari rencana, serta pertanyaan biaya dan kontrak yang muncul.

## Bagaimana Konsep Inti Saling Terhubung

```mermaid
flowchart LR
    CPM["Critical Path Method"] --> CP["Critical Path"]
    CP --> TF["Total Float"]
    TF --> SD["Schedule Delay"]
    SD --> SR["Schedule Recovery"]
    SR --> ACC["Acceleration"]
```

Cara saya membaca rantai ini: CPM menghitung critical path; total float menunjukkan seberapa dekat path lain dengan critical path; delay memakan float dan, begitu float habis, menggeser finish; recovery adalah rencana untuk merebut kembali waktu itu; acceleration adalah salah satu cara — biasanya mahal — untuk menjalankan rencana tersebut.

## Di Bagian Lain Vault
- [[Beranda Pengetahuan Planning]] — halaman awal untuk seluruh vault.
