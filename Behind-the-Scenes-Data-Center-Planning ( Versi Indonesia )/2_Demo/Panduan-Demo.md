# Panduan Demo — Obsidian + Claude (LinkedIn Live)

> Semua contoh project dan data di sesi ini fiktif dan dibuat untuk demonstrasi.
> Prinsip: yang penting demo berjalan lancar, bukan rumit. Setiap langkah punya cadangan di `Offline-Demo.pdf`. Jangan troubleshooting di depan penonton lebih dari 20 detik.

Isi folder ini:
- `Planning-Knowledge-Demo-ID/` — vault Obsidian. Satu-satunya tempat data Project Alpha, catatan pengetahuan, dan referensi.
- `Demo-Launcher.html` — tombol yang sama seperti di slide, ditambah tombol **Salin prompt** untuk prompt Claude.
- `Offline-Demo.pdf` — screenshot setiap langkah dan jawaban Claude yang sudah direkam, untuk cadangan.

---

## 1. Setup (sekali saja)

### Obsidian
1. Install Obsidian, lalu pilih **Open folder as vault** → folder `2_Demo/Planning-Knowledge-Demo-ID`.
   Buka **hanya folder itu**, jangan seluruh folder paket. Tombol di slide mencari vault bernama `Planning-Knowledge-Demo-ID`.
2. Tutup semua vault lain, terutama vault kerja.
3. Panel kanan: buka tab **Backlinks**. Perbesar tampilan sekitar 125% (Ctrl + =) — di livestream, teks kecil sulit terbaca.

### Claude Desktop
1. Install Claude Desktop, lalu login dengan paket **Pro, Max, Team atau Enterprise** (tab Code butuh paket berbayar).
2. Tab **Code** → environment **Local** → **Select folder** → `Planning-Knowledge-Demo-ID`.
3. Model: **Sonnet** (±1 menit untuk prompt demo). Permission mode: **Ask permissions**. Claude bebas membaca, tapi **minta izin** setiap kali akan membuat file.
4. File `CLAUDE.md` di vault memuat `AGENTS.md`. Isinya meminta Claude menjawab dalam Bahasa Indonesia, mengutip note sebagai `[[Nama Note]]`, dan menjawab "Tidak ada di vault" kalau informasinya tidak ada.
5. Kalau diminta **menyimpan**, `AGENTS.md` mewajibkan Claude mengikuti template di `07 Template/` persis (termasuk aturan di dalamnya), membaca hanya note sumber yang disebut template, menyimpan **satu file** di `08 AI Output/` dengan `reviewed: false`, dan tidak mengubah file lain.
6. Prompt demo memakai `Template Review Critical Path`. Jawabannya **deterministik**: sudah diuji 2 kali dan hasilnya identik. Hasil yang benar selalu 5 activity: **A-3030, A-3040, A-4010, A-4020, A-5050**, urut berdasarkan tanggal dibutuhkan, disimpan sebagai `08 AI Output/Review Critical Path - 2030-04-08.md`.

### Tes Claude (harus lulus sebelum hari H)
Tempel prompt ini di sesi baru:

```text
Hanya berdasarkan note di vault ini, apa yang sudah saya tulis tentang schedule recovery? Sebutkan pendekatan recovery utama dari note saya, dan setelah setiap poin kutip note sumbernya sebagai [[Nama Note]].
```

Lulus kalau:
- jawabannya dalam Bahasa Indonesia;
- isinya daftar pendekatan recovery dari note **Schedule Recovery**, dan setiap poin mengutip `[[Schedule Recovery]]`;
- terlihat Claude membuka file itu.

Kalau jawabannya umum tanpa sitasi, berarti Claude tidak membaca vault. Cek lagi folder yang dipilih.

Tes negatif: *"Apa yang ditulis di vault saya tentang desain pondasi tower crane? Jawab hanya dari vault."* Jawaban yang benar: topik itu tidak ada di vault.

### Pengaturan untuk share layar (LinkedIn Live)
1. Share **seluruh layar**, bukan satu jendela. Kalau hanya jendela PowerPoint yang di-share, penonton tidak melihat Obsidian dan Claude saat Anda Alt + Tab.
2. PowerPoint → **Slide Show → Set Up Slide Show → Browsed by an individual (window)**, lalu maksimalkan jendelanya. Dengan mode ini Alt + Tab ke Obsidian dan kembali ke slide berjalan mulus di satu layar.
3. Presenter View butuh layar kedua. Kalau hanya ada satu layar, cetak atau buka speaker notes (`File → Export → Handouts`, atau PDF notes) di perangkat lain.
4. Resolusi layar 1920 × 1080; tutup semua jendela lain.

---

## 2. Latihan Tombol

1. Mulai slideshow. Di slide **24**, klik setiap tombol **Buka** satu kali.
2. Di slide **26**, klik **Buka Claude** dan **Salin prompt**. Di slide **27**, klik **Buka note yang dikutip**.
3. Kalau PowerPoint, browser atau Windows bertanya apakah boleh membuka Obsidian atau Claude, pilih **Yes / Always allow**. Dengan begitu pertanyaan itu tidak muncul di siaran.
4. Jalankan prompt demo satu kali (klik **Allow** saat diminta) dan catat waktunya (target ±1 menit, maksimal 2 menit). Buka `08 AI Output/Review Critical Path - 2030-04-08.md` dan pastikan tabelnya berisi 5 activity di atas.
5. Latih sekali dengan share layar yang sebenarnya (misalnya bersama Masron atau panitia) dan cek apakah teks Obsidian dan Claude terbaca di layar penonton.
6. Setelah selesai, **hapus note `09 Inbox/Site Walk - Week 14`** dan **semua note di `08 AI Output/`**, supaya saat live keduanya terlihat baru. Kalau tidak dihapus pun aman, karena Claude akan menimpa file yang sama.

---

## 3. Posisi Awal — Cek Jam 19.45

Susun semua jendela seperti ini **sebelum live**, supaya saat demo Anda hanya klik dan bicara.

**Obsidian**
- [ ] Vault yang terbuka adalah versi Indonesia: panel kiri berisi **00 Beranda … 06 Referensi, 09 Inbox**, tanpa folder 07/08.
- [ ] Note `09 Inbox/Site Walk - Week 14` **sudah dihapus**: klik kanan note itu, lalu pilih **Delete**.
- [ ] Folder `08 AI Output` **kosong** (hasil latihan sudah dihapus). Folder `07 Template` berisi **Template Review Critical Path**.
- [ ] Buka note **Beranda Pengetahuan Planning** sebagai tampilan awal.
- [ ] Panel kiri menampilkan **daftar file** (ikon folder di kiri atas aktif).
- [ ] Panel kanan terbuka dengan tab **Backlinks** (Ctrl + P → ketik `backlinks` → **Backlinks: Open backlinks**).
- [ ] Zoom sekitar 125% (Ctrl + =).
- [ ] Jangan buka daftar vault di pojok kiri bawah selama share layar, karena daftar itu memperlihatkan vault Anda yang lain.

**Claude Desktop**
- [ ] Sudah login.
- [ ] Di tab **Code**, **sesi baru sudah dibuat**: environment **Local**, folder `Planning-Knowledge-Demo-ID` (versi Indonesia), model **Sonnet**, mode **Ask permissions**. Kotak input masih kosong.
- [ ] Sidebar daftar sesi ditutup, supaya nama sesi lain tidak terlihat.

**Browser dan cadangan**
- [ ] `Demo-Launcher.html` sudah terbuka di satu tab browser.
- [ ] `Offline-Demo.pdf` sudah terbuka, lalu di-minimize.

**PowerPoint**
- [ ] Slide Show dalam mode **Browsed by an individual (window)**, jendela dimaksimalkan.
- [ ] Coba **Alt + Tab** sekali: PowerPoint → Obsidian → kembali ke PowerPoint.

> Aturan Alt + Tab: satu kali **Alt + Tab** selalu kembali ke jendela **sebelumnya**. Untuk memilih jendela lain, tahan **Alt** lalu tekan **Tab** beberapa kali, atau klik ikonnya di taskbar.

---

## 4. Demo 1 — Satu Minggu Planner di Obsidian (slide 24, ± 4 menit)

Slide 23 sebelumnya sudah menjelaskan bahwa vault ini disiapkan untuk demo dan bahwa di pekerjaan nyata vault tumbuh dari satu catatan per hari.

### Langkah 1 — Catat (± 1 menit)

| # | Yang Anda lakukan | Yang muncul di layar | Yang diucapkan |
|---|---|---|---|
| 1 | Di slide 24, klik **Buka** di baris **1 · Catat** | Obsidian maju ke depan. Note **Site Walk - Week 14** terbuka dan muncul di folder `09 Inbox` di panel kiri | "Pagi ini saya site walk…" |
| 2 | Arahkan kursor ke kalimat **Temuan di site** | — | "Rigging route ke Area A tertutup scaffold, permit-nya juga masih pending. Daripada hilang di chat atau cuma di kepala, saya catat." |
| 3 | Arahkan kursor ke link **Electrical Equipment Installation - Area A** | — | "Catatan ini terhubung ke activity-nya, A-3030." |
| 4 | Tekan **Ctrl + E** | Note berubah ke **mode edit**: simbol Markdown terlihat | "Supaya cepat, catatan ini saya siapkan lewat tombol. Tapi saya tunjukkan cara membuat hubungannya, karena ini intinya." |
| 5 | Klik di **akhir baris paling bawah** (setelah kata *Constraints*), lalu tekan **Enter** | Muncul poin baru `- ` | — |
| 6 | Ketik `Bahas di rapat minggu ini → ` lalu ketik **`[[`** | Obsidian otomatis menambah `]]` dan menampilkan **daftar semua note** | "Cukup ketik dua kurung siku." |
| 7 | Ketik **`Weekly`** | Daftar menyaring ke **Weekly Planning - Week 14** | — |
| 8 | Tekan **Enter** | Menjadi `[[Weekly Planning - Week 14]]` | — |
| 9 | Tekan **Ctrl + E** | Kembali ke **mode baca**. Tulisan tadi menjadi **link berwarna** | "Selesai, dua catatan ini sekarang terhubung. Link ke A-3030 di atas juga dibuat dengan cara yang sama. Tidak perlu copy-paste atau mencari folder." |
| 10 | **Alt + Tab** | Kembali ke slide 24 | — |

Kalau salah ketik, klik **Buka** di baris 1 lagi. Note-nya akan ditimpa dan kembali bersih.

### Langkah 2 — Hubungkan (± 50 detik)

| # | Yang Anda lakukan | Yang muncul di layar | Yang diucapkan |
|---|---|---|---|
| 1 | Klik **Buka** di baris **2 · Hubungkan** | Note **Electrical Equipment Installation - Area A** (A-3030) terbuka | "Sekarang saya lihat dari sisi activity-nya." |
| 2 | Scroll ke bagian **Apa yang Membuatnya Bisa Dimulai — Readiness Check** | Tabel prerequisite dengan kesimpulan **NOT READY** | — |
| 3 | Arahkan kursor ke baris **Access ❌ NOT READY** | — | "Di schedule activity ini kelihatan normal, tapi dari readiness check: empat dari lima ready, satu belum, yaitu akses. Persis temuan site walk tadi." |
| 4 | Arahkan kursor ke **panel kanan (Backlinks)**, bagian **Linked mentions** | Daftar note yang menyebut A-3030, termasuk **Site Walk - Week 14** | "Saya tidak menghubungkannya dari sini. Karena catatan site walk tadi menyebut activity ini, Obsidian otomatis menampilkannya di sini, bersama notulen rapat, weekly planning dan decision log." |
| 5 | **Alt + Tab** | Kembali ke slide 24 | — |

Kalau panel kanan tidak terlihat: tekan **Ctrl + P**, ketik `backlinks`, lalu Enter.

### Langkah 3 — Pakai Ulang (± 40 detik)

| # | Yang Anda lakukan | Yang muncul di layar | Yang diucapkan |
|---|---|---|---|
| 1 | Klik **Buka** di baris **3 · Pakai ulang** | Note **Cek Readiness Sebelum Mulai** terbuka | "Dari activity tadi saya sampai ke lesson yang pernah saya tulis." |
| 2 | Arahkan kursor ke kotak **Intinya** di atas | — | "Ini bukan data project. Ini pelajaran yang saya tulis dengan bahasa saya sendiri." |
| 3 | Scroll sedikit, lalu arahkan kursor ke kalimat tebal **"Kalau empat dari lima prerequisite sudah ready, activity itu belum ready."** | — | "Pelajaran ini bisa saya pakai di project mana pun. Di project berikutnya saya tidak mulai dari nol." |
| 4 | **Alt + Tab** | Kembali ke slide 24 | — |

### Langkah 4 — Temukan (± 40 detik)

| # | Yang Anda lakukan | Yang muncul di layar | Yang diucapkan |
|---|---|---|---|
| 1 | Klik **Buka** di baris **4 · Temukan** | Panel kiri berubah menjadi **Search** dengan kata `rigging` dan daftar hasil | "Enam bulan lagi saya lupa catatannya di mana. Cukup cari satu kata." |
| 2 | Arahkan kursor ke hasil: **Notulen Rapat…**, **Electrical Equipment Installation…**, **Cek Readiness…**, **Site Walk - Week 14** | — | "Notulen rapat, activity, lesson dan catatan site walk hari ini muncul bersama. Konteksnya kembali dalam satu layar." |
| 3 | Klik ikon **folder** (File explorer) di kiri atas | Panel kiri kembali ke daftar file | — |
| 4 | **Alt + Tab** | Kembali ke slide 24 | — |

### Langkah 5 — Lihat (opsional, ± 30 detik; lewati kalau waktu mepet)

| # | Yang Anda lakukan | Yang muncul di layar | Yang diucapkan |
|---|---|---|---|
| 1 | **Alt + Tab** ke Obsidian, lalu tekan **Ctrl + G** | Tab **Graph view** terbuka. Tunggu 2 detik sampai titik-titiknya diam | "Kalau catatannya makin banyak dan saling terhubung, bentuknya kurang lebih seperti ini." |
| 2 | — | — | "Tapi graph bukan tujuannya. Tujuannya menemukan konteks lagi." |
| 3 | Tekan **Ctrl + W** | Tab graph tertutup | — |
| 4 | **Alt + Tab**, lalu tekan **→** | Pindah ke slide 25 | "Nah, sekarang bagaimana kalau AI bisa membaca catatan-catatan ini?" |

---

## 5. Demo 2 — Obsidian + Claude (slide 26–27, ± 4 menit)

### Di slide 26

| # | Yang Anda lakukan | Yang muncul di layar | Yang diucapkan |
|---|---|---|---|
| 1 | Klik **Buka Claude** | Claude Desktop maju ke depan dengan sesi yang sudah disiapkan: tab **Code**, folder `Planning-Knowledge-Demo-ID`, model **Sonnet**, mode **Ask permissions** | "Ini Claude. Saya beri akses hanya ke satu folder, yaitu vault tadi." |
| 2 | Kalau yang terbuka tab Chat: klik tab **Code**, lalu pilih sesi yang sudah disiapkan | — | — |
| 3 | **Alt + Tab** ke PowerPoint, lalu klik **Salin prompt** | Browser terbuka di **Demo Launcher**, bagian *2 · Obsidian + Claude* | "Bagian AI ini masih eksperimen, jadi saya tidak minta pendapat AI. Saya minta sesuatu yang bisa dicek: dari data project, activity mana di critical path yang masih punya constraint open. Hasilnya disimpan sebagai note, memakai template." |
| 4 | Di browser, klik tombol **Salin prompt** | Muncul tulisan **Tersalin ✓** | — |
| 5 | Klik ikon **Claude** di taskbar. Satu kali Alt + Tab dari browser akan kembali ke PowerPoint, bukan ke Claude | Claude di depan | — |
| 6 | Klik kotak input, tekan **Ctrl + V**, lalu **Enter** | Prompt terkirim. **Biasanya ±1 menit, batas 2 menit** | — |
| 7 | Arahkan kursor ke baris aktivitas Claude: **Read … Template Review Critical Path.md**, **Constraint Register.md**, **Decision Log.md** | Claude hanya membaca beberapa note | "Perhatikan: dia membaca template-nya dulu, lalu hanya note yang dibutuhkan: constraint register, decision log, schedule." |
| 8 | Muncul permintaan izin untuk **membuat file** di `08 AI Output/` → klik **Allow** (izinkan sekali) | Claude menulis note | "Sebelum menyimpan, dia minta izin. Saya yang memutuskan." |
| 9 | Claude selesai | Di chat hanya ada nama file dan satu kalimat ringkasan: *5 constraint open di critical path; paling mendesak C-003 pada A-3030* | "Isinya tidak di chat. Isinya sudah jadi catatan di vault." |
| 10 | Klik ikon **Obsidian** di taskbar. Di panel kiri buka folder **08 AI Output**, lalu klik **Review Critical Path - 2030-04-08** | Note hasil terbuka dalam format template | — |
| 11 | Arahkan kursor ke **tabel**, baris 1: **A-3030 · C-003 · Access · D-001, D-002** | Tabel 5 activity: A-3030, A-3040, A-4010, A-4020, A-5050 | "Lima activity di critical path, urut dari yang paling mendesak. Nomor satu A-3030, activity yang sama dengan yang kita bahas dari tadi. Setiap baris menyebut activity ID, constraint ID dan decision ID." |
| 12 | Arahkan kursor ke **reviewed: false** dan kotak **Draft AI — belum direview** | — | "Statusnya masih draft sampai saya sendiri yang mereview." |
| 13 | Scroll ke **Pertanyaan Review per Activity**, lalu **klik link [[Constraint Register]]** di bawah A-3030 | Constraint Register terbuka | "Setiap baris bisa dicek balik ke sumbernya." |
| 14 | Klik ikon **PowerPoint** di taskbar, lalu tekan **→** | Slide 27 | — |

Kalau Claude **belum selesai setelah 2 menit**, atau muncul error, katakan: "Ini hasil yang sama dari latihan." Lalu pindah ke **slide 27**, yang menampilkan baris A-3030 dari hasil uji coba, atau buka halaman terakhir `Offline-Demo.pdf` yang berisi hasil lengkapnya.

### Di slide 27

| # | Yang Anda lakukan | Yang muncul di layar | Yang diucapkan |
|---|---|---|---|
| 1 | Arahkan kursor ke kotak kiri: **A-3030 · C-003 Access · dibutuhkan 2030-04-08 · decision D-001, D-002** | Satu baris dari note hasil Claude | "Ambil satu baris: A-3030, constraint C-003." |
| 2 | Klik **Buka note yang dikutip** | Obsidian maju. **Constraint Register** terbuka | "Ini register-nya." |
| 3 | Scroll ke tabel **Register**, lalu arahkan kursor ke baris **C-003** | C-003 · A-3030 · Access · Open · Main Contractor Site Manager · 2030-04-08 | "C-003 memang open, owner Site Manager, dibutuhkan 8 April. Kalau AI salah, saya langsung tahu." |
| 4 | **Alt + Tab**, lalu tekan **→** | Slide 28 | "Dan karena pertanyaannya berbasis data, jawabannya konsisten. Saya jalankan dua kali, hasilnya sama persis." |

Kalau langkah 13 di slide 26 sudah memverifikasi sumbernya dan waktu mepet, slide 27 cukup ditunjukkan sebentar tanpa klik.

Cara lain untuk verifikasi live: di Obsidian tekan **Ctrl + O**, ketik nama note yang dikutip Claude, lalu Enter.

---

## 6. Kalau Ada yang Gagal

| Masalah | Tindakan | Yang dikatakan |
|---|---|---|
| Tombol di slide tidak membuka apa-apa | Pakai tombol yang sama di `Demo-Launcher.html` | — |
| Muncul "Vault not found" | Obsidian → Open folder as vault → `Planning-Knowledge-Demo-ID`, lalu klik lagi | — |
| Obsidian tidak mau terbuka | `Offline-Demo.pdf`, halaman Obsidian | "Ini jalur yang tadinya mau saya klik." |
| Internet lambat atau Claude tidak tersedia | Demo Obsidian tetap live; bagian Claude dari `Offline-Demo.pdf` | "Jaringannya sedang kurang bersahabat, jadi ini pertanyaan yang sama dari latihan." |
| Claude lambat (lebih dari 2 menit) | Pindah ke `Offline-Demo.pdf`; verifikasi sitasi tetap live di Obsidian | "Ini jawaban dari latihan — kita cek satu sitasinya langsung." |
| Penonton tidak melihat Obsidian/Claude | Ganti share ke **seluruh layar** | "Sebentar, saya ganti tampilan layarnya." |
| Stream atau laptop bermasalah | Masron melanjutkan dengan PDF deck (kirim `1_Presentasi/Behind-the-Scenes-of-Data-Center-Project.pdf` ke Masron sebelum acara) | — |
| Waktu mepet | Lewati langkah 5; verifikasi cukup satu sitasi | — |

---

## 7. Keamanan dan Beres-Beres

- Isi file yang dibaca Claude dikirim ke Anthropic sebagai bagian dari percakapan. Di paket konsumen (Free, Pro, Max), Anda bisa memilih di Settings → Privacy apakah percakapan boleh dipakai untuk training. Paket komersial tidak dipakai untuk training secara default.
- Sesi ini publik: pilih hanya folder vault demo, dan pastikan daftar sesi Claude, vault switcher Obsidian dan taskbar tidak memperlihatkan nama proyek nyata.
- Setelah sesi: tutup sesi Claude di tab Code. Hapus note `09 Inbox/Site Walk - Week 14` dan isi `08 AI Output/` kalau ingin vault kembali seperti semula.
