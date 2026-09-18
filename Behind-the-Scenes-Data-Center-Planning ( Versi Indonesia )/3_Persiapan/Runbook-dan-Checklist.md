# Runbook dan Checklist — LinkedIn Live

> Semua contoh project dan data di sesi ini fiktif dan dibuat untuk demonstrasi.
> Kalimat yang diucapkan per slide ada di **speaker notes PPTX**. Setiap notes diawali `PEMBICARA: ...`, dan nama pembicara juga tampil kecil di pojok kanan bawah slide.

**Acara:** Behind the Scenes of Data Center Project — Mastering Control, Management, and Continuous Monitoring from Ground to Cloud
**Jadwal:** Jumat, 18 September 2026 · 20.00 WIB · LinkedIn Live (Project Management Prodigy)
**Pembicara:** Masron Hutabalian (bagian 1) & Abdul Kausar (bagian 2) · **Operator slide:** Abdul
**Deck:** `1_Presentasi/Behind-the-Scenes-of-Data-Center-Project.pptx` (31 slide)

Alur: **ground → ekosistem → interface → control → commissioning → monitoring → satu activity (serah terima) → informasi → knowledge → Obsidian → AI → kembali ke planner.**

## 1. Waktu — 1 Jam

| Jam | Menit | Slide | Pembicara | Pesan | Durasi |
|---|---|---|---|---|---|
| 20.00 | 0:00 | 1 | Masron & Abdul | Judul dan salam pembuka | 0:30 |
| 20.00 | 0:30 | 2–3 | Masron | Satu jam, tiga bagian + disclaimer data simulasi | 1:30 |
| 20.02 | 2:00 | 4–5 | Masron | Dari ground sampai cloud, perjalanannya panjang | 2:30 |
| 20.04 | 4:30 | 6–7 | Masron | Data center adalah ekosistem sistem | 3:00 |
| 20.07 | 7:30 | 8–9 | Masron | Kompleksitas ada di interface | 3:00 |
| 20.10 | 10:30 | 10 | Masron | Project control adalah sebuah loop | 3:00 |
| 20.13 | 13:30 | 11–12 | Masron | Lifecycle; READY = terbukti bekerja (L1–L5) | 3:00 |
| 20.16 | 16:30 | 13 | Masron | Monitoring tidak berhenti saat konstruksi selesai | 2:30 |
| 20.19 | 19:00 | 14–16 | Masron → **serah terima** | Satu activity, banyak realita | 2:30 |
| 20.21 | 21:30 | 17 | Abdul | 4 dari 5 ready bisa berarti belum ready | 2:30 |
| 20.24 | 24:00 | 18 | Abdul | Control butuh informasi | 1:30 |
| 20.25 | 25:30 | 19 | Abdul | Informasi tersebar di mana-mana | 2:00 |
| 20.27 | 27:30 | 20 | Abdul | Menyimpan informasi ≠ membangun pengetahuan + "…tapi di mana, ya?" | 2:30 |
| 20.30 | 30:00 | **21** | Abdul | **Apa itu Obsidian** + link download | 1:00 |
| 20.31 | 31:00 | 22 | Abdul | Catat · Rapikan · Hubungkan · Temukan kembali | 2:30 |
| 20.33 | 33:30 | **23** | Abdul | **Vault ini disiapkan untuk demo; di pekerjaan nyata tumbuh dari kebiasaan** | 1:15 |
| 20.34 | 34:45 | **24** | Abdul | **Demo langsung Obsidian** (tombol di slide) | 4:00 |
| 20.38 | 38:45 | 25 | Abdul | Bagaimana kalau AI bisa membaca yang sudah saya pelajari? AI mencari, menghubungkan, mengutip | 2:30 |
| 20.41 | 41:15 | **26–27** | Abdul | **Demo langsung Claude** (tombol di slide) | 4:00 |
| 20.45 | 45:15 | 28 | Abdul | Planner tetap di tengah — dari ground sampai cloud | 2:00 |
| 20.47 | 47:15 | 29 | Abdul | Pahami. Catat. Buat agar bisa dipakai lagi. | 0:30 |
| 20.47 | 47:45 | 30 | Abdul | Pertanyaan untuk dibawa pulang + "mulai besok dengan satu catatan" | 0:30 |
| 20.48 | 48:15 | 31 | Masron & Abdul | Tanya jawab | ±11:45 |

### Kalau waktu mepet (±5 menit dipotong)
| Slide | Aksi |
|---|---|
| 6–7 | Cukup build 2; sebutkan enam system dalam satu kalimat. |
| 11–12 | Cukup build 2 (L1–L5), lifecycle diucapkan singkat. |
| 20 | Cukup satu kalimat "…tapi di mana, ya?". |
| 23 | Jangan dilewati — cukup kalimat kuncinya (±40 detik). |
| 24 | Demo Obsidian 3 menit: lewati langkah 5 (graph). |
| 26–27 | Demo Claude 3 menit; verifikasi satu sitasi saja. |

### Tempo
- **Paling penting:** slide 8–9 (interface), 14–17 (satu activity dan 4 dari 5 ready), slide 23 (asal vault demo), dan kedua demo.
- **Pelan-pelan di:** slide 4–5, 10, 12, 17, 23, 26–27, 30.
- **Boleh cepat di:** slide 1, 13, 18, 25.

## 2. Operator Slide (Abdul)

- Mode PowerPoint: **Slide Show → Set Up Slide Show → Browsed by an individual (window)**, jendela dimaksimalkan, share **seluruh layar**.
- Selama bagian Masron, klik saat Masron memberi aba-aba ("next" / "slide berikutnya") atau ikuti speaker notes. Sepakati aba-abanya saat gladi.
- Build di satu slide (misalnya slide 4 → 5, 6 → 7) dianggap satu klik per langkah; notes menulis `build 1/2`, `build 2/2`.
- Serah terima ada di **slide 16**: Masron menutup dengan "saya serahkan ke Abdul", lalu Anda mulai di slide 17 dengan "Terima kasih, Masron".
- Di **slide 21**, tombol **Buka link download** membuka obsidian.md/download di browser. Tidak perlu diklik saat live — cukup tunjukkan alamatnya.

## 3. Urutan Latihan

| Latihan | Apa | Fokus | Berhasil kalau |
|---|---|---|---|
| 1 | Masron dan Abdul membaca bagian masing-masing, pakai timer | Alur dan serah terima | Bagian 1 ≈ 21 menit, bagian 2 ≈ 27 menit |
| 2 | Deck lengkap + kedua demo (klik tombol) | Aba-aba "next", pindah jendela | Total ≤ 49 menit, setiap demo ≤ 4:00 |
| 3 | **Latihan kalau gagal** | Pindah ke `2_Demo/Offline-Demo.pdf` di tengah demo | Pindah < 20 detik dengan kalimat yang sama |
| 4 | **Gladi dengan share layar** di platform yang dipakai | Keterbacaan di layar penonton, suara dua pembicara | Teks slide, Obsidian dan Claude terbaca; tidak ada suara bertabrakan |

### Koordinasi dengan Masron
- [ ] Masron sudah membaca dan menyesuaikan speaker notes slide 1–16 (isi bagian 1 disusun sebagai draft dari catatan vault).
- [ ] Sepakati aba-aba ganti slide dan kalimat serah terima di slide 16.
- [ ] Sepakati pembagian tanya jawab: data center, project control & monitoring → Masron; Obsidian, knowledge & AI → Abdul.
- [ ] Kirim PDF deck ke Masron/panitia sebagai cadangan kalau laptop atau koneksi operator bermasalah.

### Demo
- [ ] Setup, pengaturan share layar dan latihan tombol di `2_Demo/Panduan-Demo.md` bagian 1–2 sudah selesai.
- [ ] Lima langkah Obsidian berjalan tiga kali berturut-turut tanpa melihat catatan.
- [ ] Tes Claude lulus, dan prompt demo (termasuk menyimpan note) selesai ≤ 2 menit di jaringan yang akan dipakai.

### Istilah dan cara mengucapkan
| Istilah | Ucapkan | Arti singkat kalau ditanya |
|---|---|---|
| UPS | "U-P-S" | Uninterruptible power supply (listrik cadangan tanpa putus) |
| CRAH | *"krei"* | Computer room air handler (pendingin ruang server) |
| BMS / EPMS | "B-M-S" / "E-P-M-S" | Building management system / electrical power monitoring system |
| DCIM | "D-C-I-M" | Data center infrastructure management (pemantauan kapasitas & aset) |
| FAT | "F-A-T" | Factory acceptance test — tes equipment di pabrik |
| IST | "I-S-T" | Integrated systems testing (commissioning level 5) |
| Total float | — | Berapa lama activity boleh mundur tanpa menggeser tanggal finish |
| Obsidian | *ob-SI-di-en* | Aplikasi catatan gratis yang menyimpan catatan sebagai file Markdown di folder sendiri |
| Markdown | *MARK-daun* | Teks biasa dengan simbol format sederhana |
| RAG | "reg" | Retrieval-augmented generation — AI menjawab dari dokumen yang diambil |

### Log latihan
| Latihan | Tanggal | Bagian 1 | Bagian 2 | Demo 1 | Demo 2 | Yang diperbaiki |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |

## 4. Checklist Hari H (LinkedIn Live)

> Item bertanda 🔒 = kerahasiaan. Sesi ini publik — jangan dilewati.

### Sehari sebelumnya
- [ ] Claude Desktop, Obsidian dan aplikasi streaming sudah di-update (jangan update di hari H).
- [ ] Tes Claude lulus di laptop operator; gladi share layar bersama Masron sudah dilakukan.
- [ ] Charger, headset/mikrofon, dan koneksi internet cadangan (hotspot) siap.
- [ ] PDF deck sudah dikirim ke Masron/panitia.

### 60 menit sebelum (±19.00 WIB)
- [ ] Koneksi internet stabil; kalau bisa pakai kabel LAN.
- [ ] PPTX terbuka dalam mode **Browsed by an individual (window)**; font Georgia dan Segoe UI tampil benar.
- [ ] Obsidian membuka vault `Planning-Knowledge-Demo-ID` (versi Indonesia); zoom ± 125%; panel Backlinks terbuka.
- [ ] 🔒 Tidak ada vault proyek nyata di vault switcher atau daftar vault terakhir.
- [ ] Note `09 Inbox/Site Walk - Week 14` sudah dihapus, dan folder `08 AI Output` kosong.
- [ ] Claude: tab Code → Local → folder vault → model **Sonnet** → mode **Ask permissions**; sesi baru yang masih kosong. 🔒 Daftar sesi lama tidak memperlihatkan nama proyek nyata.
- [ ] `2_Demo/Offline-Demo.pdf` terbuka di jendela belakang.

### 15 menit sebelum
- [ ] Notifikasi mati (Windows Do Not Disturb; Teams, Outlook, WhatsApp Web dan chat ditutup).
- [ ] 🔒 Desktop, taskbar dan tab browser bersih — tidak ada nama file atau jendela yang menyebut proyek, klien atau lokasi.
- [ ] 🔒 Folder dan aplikasi kerja ditutup (email, P6, document control).
- [ ] Share **seluruh layar** sudah diuji; kamera dan mikrofon kedua pembicara dicek.
- [ ] Urutan Alt + Tab: PowerPoint → Obsidian → Claude.
- [ ] Air minum; HP mode senyap.

### Selama sesi
- [ ] Slide 3: disclaimer data simulasi disampaikan Masron.
- [ ] Slide 16 → 17: serah terima Masron → Abdul.
- [ ] Slide 23: sampaikan bahwa vault disiapkan untuk demo (sebelum penonton bertanya).
- [ ] Demo Obsidian (slide 24) macet > **20 detik** → Offline-Demo.pdf.
- [ ] Claude (slide 26) belum selesai setelah **2 menit** → halaman Claude di Offline-Demo.pdf.
- [ ] Waktu mepet? Pakai potongan di bagian 1.

### Tanya jawab
- [ ] Bacakan pertanyaan dari kolom komentar sebelum menjawab; sebut siapa yang menjawab.
- [ ] Jawaban yang sudah disiapkan (bagian Obsidian & AI): `3_Persiapan/Q&A.md`.
- [ ] 🔒 Pertanyaan tentang proyek nyata: "Kami sengaja tidak memakai data proyek nyata — itu sebabnya semua contoh tadi simulasi."

### Setelah selesai
- [ ] Hentikan share layar dulu, baru tutup aplikasi.
- [ ] 🔒 Tutup sesi Claude; hapus note Site Walk dan isi `08 AI Output` kalau ingin vault kembali seperti semula.
- [ ] Catat yang berhasil dan yang gagal untuk sesi berikutnya.
