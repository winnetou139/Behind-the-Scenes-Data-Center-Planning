---
type: concept
domain: planning
status: evergreen
tags:
  - scheduling
  - cpm
  - float
references:
  - REF-001
updated: 2026-09-14
---

# Critical Path

> **Intinya:** Critical path adalah rangkaian activity yang menentukan finish paling cepat dari project atau milestone penting — didefinisikan sebagai longest path di network atau sebagai activity dengan total float terendah. Dua sudut pandang ini biasanya sama, tapi tidak selalu.

Bagian dari [[Planning & Scheduling MOC]]

## Definisi
Ada dua definisi yang umum:

1. **Longest path** — rantai activity driving yang tidak terputus dari data date sampai finish project (atau milestone). Delay apa pun di rantai ini akan menggeser finish tersebut.
2. **Total float terendah** — activity yang [[Total Float]]-nya nol, atau sama dengan/di bawah batas yang dipilih.

Di network sederhana dengan satu calendar dan tanpa date constraint, keduanya memberi jawaban yang sama. Di P6 kita memilih aturan mana yang menandai activity sebagai critical: total float kurang dari atau sama dengan nilai tertentu, atau longest path.

### Kenapa dua sudut pandang ini bisa berbeda
- **Date constraint** — milestone yang di-constraint lebih awal dari tanggal hasil hitungan akan menciptakan float negatif di rantai yang mengarah ke sana. Tampilan float terendah akan menyorot rantai itu, walaupun rantai lain yang sebenarnya menentukan finish project. Tanggal must-finish yang lebih lambat dari finish hasil hitungan membuat semua activity punya float positif, dan filter "float ≤ 0" tidak menunjukkan satu pun activity critical.
- **Beberapa calendar** — float dihitung berdasarkan calendar masing-masing activity, jadi activity di rantai driving yang sama bisa menunjukkan nilai float berbeda.
- **Beberapa milestone** — float sering diukur ke finish project, jadi rantai yang menentukan milestone antara seperti energization bisa terlihat punya float padahal critical untuk milestone itu.
- **Open end dan lag** — mendistorsi late date, sehingga float juga terdistorsi.

Recommended practice AACE tentang identifikasi critical path membahas masalah-masalah ini secara mendalam, dan panduan GAO lebih memilih longest path (driving path) kalau dua sudut pandang ini tidak sama. Pelajaran praktisnya: cek kedua tampilan sebelum melaporkan salah satunya.

## Near-Critical Path
Path dengan float positif yang kecil disebut near-critical. Slip kecil, atau langkah recovery yang diterapkan di critical path, bisa membuatnya jadi critical. Saya memantau satu band near-critical — batasnya ditentukan per project — bukan hanya activity dengan float nol.

## Critical ≠ Penting
"Critical" adalah sifat hasil hitungan: tidak ada float ke finish. Tidak ada hubungannya dengan biaya, tingkat risiko keselamatan atau seberapa terlihat pekerjaannya. Activity critical bisa saja approval dokumen yang kecil; instalasi besar yang berisiko tinggi bisa punya float. Mencampuradukkan keduanya membuat prioritas jadi salah.

## Kenapa Penting
Critical path menunjukkan di mana satu hari yang hilang berarti satu hari hilang dari finish — dan di mana upaya recovery benar-benar ada hasilnya. Upaya di luar critical path tidak menggeser forecast.

## Sudut Pandang Planner
Saya selalu menjalankan tampilan longest path berdampingan dengan tampilan float, lalu membandingkannya. Kalau berbeda, saya cari tahu kenapa sebelum melaporkan apa pun. Saya juga bertanya "critical terhadap apa?" Di data center, milestone yang penting bisa jadi energization atau start IST, jadi saya telusuri driving path ke milestone-milestone itu, bukan hanya ke finish akhir.

## Contoh Praktis
Di project fiktif ini, A-3030 berada di critical path electrical menuju energization, commissioning dan [[Integrated Systems Testing]]. Pengiriman standby generator ceritanya lain: slip-nya memakan float di path non-critical tanpa menggeser finish. Project yang sama, dua slip, konsekuensinya sangat berbeda. Lihat [[Electrical Equipment Installation - Area A]] dan [[Pantau Float, Bukan Hanya Tanggal]].

## Kesalahan yang Sering Terjadi
- Melaporkan "critical path" dari filter float tanpa mengecek constraint dan calendar.
- Menerima critical path yang mulai di tengah network atau melompat di antara activity yang tidak berhubungan — tanda logic yang rusak.
- Mengabaikan near-critical path.
- Menyebut activity "critical" karena dianggap penting.
- Hanya menganalisis milestone akhir dan melewatkan milestone antara, baik milestone kontrak maupun energization.

## Konsep Terkait
- [[Total Float]] — ukuran di balik definisi float terendah.
- [[Schedule Delay]] — delay di critical path menggeser finish.
- [[Schedule Recovery]] — upaya recovery harus menyasar critical path dan near-critical path.
- [[Acceleration]] — hanya ada hasilnya kalau diterapkan pada activity driving.
- [[Integrated Systems Testing]] — milestone data center yang umum menjadi ujung critical path.
- [[Pantau Float, Bukan Hanya Tanggal]] — membaca tren float, bukan hanya tanggal.

## Referensi
- [[REF-001 GAO Schedule Assessment Guide|REF-001]] — critical path yang valid sebagai best practice, dan mengutamakan longest path bila berbeda dengan tampilan float terendah.
