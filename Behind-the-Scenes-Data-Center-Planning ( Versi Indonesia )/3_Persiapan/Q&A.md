# Q&A — Jawaban yang Sudah Disiapkan

> Jawaban singkat dan akurat; jangan melebih-lebihkan. Kode REF-xxx merujuk ke note di vault `2_Demo/Planning-Knowledge-Demo-ID/06 Referensi`; sumber lain disebut langsung namanya.
> **Aturan emas:** ulangi pertanyaannya, jawab dalam dua–tiga kalimat, tawarkan diskusi lanjut setelah sesi.
> **Kerahasiaan:** jangan pernah menjawab dengan informasi proyek nyata — "justru itu sebabnya semua contoh hari ini fiktif."

---

## Tentang Pendekatannya

### 1. Kenapa Obsidian, bukan OneNote atau Notion?
Alasan utamanya, note di Obsidian itu file Markdown biasa di folder biasa di komputer saya. Link antar-note, lengkap dengan backlinks dan graph, sudah tersedia bawaan (REF-040, REF-041, REF-042). Jadi note-nya mudah dipindah dan bisa dibaca tool lain, termasuk AI. OneNote atau Notion juga bisa bekerja dengan baik — yang lebih penting itu kebiasaan menulis dan menghubungkan note, bukan tool-nya. Pakai saja yang didukung perusahaan Anda.

### 2. Kenapa tidak simpan PDF di folder saja?
Folder bagus untuk **arsip**, tapi lemah untuk **dipakai ulang**. Folder menjawab "file ini asalnya dari mana?". Note yang saling terhubung menjawab "apa yang saya tahu soal ini, dan ini terkait dengan apa saja?". PDF-nya tetap saya simpan — note berisi pemahaman saya dan menunjuk ke sumbernya.

### 3. Seberapa besar usaha untuk merawat vault?
Lebih ringan dari yang orang kira, asalkan note-nya tetap kecil. Cukup beberapa menit di minggu saat ada kejadian, ditambah merapikan sesekali. Kualitas link lebih penting daripada jumlah note.

### 4. Apa yang terjadi kalau vault jadi sangat besar?
Search, link, dan backlinks tetap jalan, karena tidak bergantung pada kedalaman folder. Risiko praktisnya adalah note ganda dan link yang lemah. Itu diatasi dengan Maps of Content dan bersih-bersih berkala. Untuk AI, vault yang lebih besar berarti tool-nya harus mencari, bukan membaca semuanya. Jadi nama note yang konsisten, ringkasan satu baris, dan bagian "Related Concepts" jadi makin penting.

### 5. Apakah ini bisa dipakai di profesi lain?
Bisa. Tidak ada yang khusus untuk planning di sini, kecuali isinya. Cost engineer, commissioning engineer, document controller, dan desainer juga mengumpulkan pengetahuan yang susah dicari lagi.

### 6. Bagaimana cara mulainya?
Pilih satu topik yang sering Anda pelajari ulang. Tulis satu note pendek per minggu dengan kata-kata sendiri. Hubungkan setiap note baru ke dua note lain. Setelah sebulan, coba tanya AI satu pertanyaan tentang note-note itu saja.

### 7. Apakah Obsidian gratis untuk dipakai kerja?
Sejak Februari 2025, lisensi komersial Obsidian sudah opsional, jadi gratis untuk dipakai kerja (REF-067). Tapi boleh atau tidaknya di-install di laptop kantor itu soal IT policy yang terpisah — cek dulu.

### 8. Apakah ini menggantikan P6 atau sistem document control?
Tidak. Schedule tetap di tool scheduling, dan dokumen resmi tetap di document control. Vault hanya berisi *pengetahuan pribadi* — konsep, lessons learned, cara kerja — bukan dokumen proyek.

---

## Tentang AI

### 9. Apakah AI dilatih pakai isi vault saya?
Tergantung plan dan settings-nya. Apa pun yang dibaca tool akan dikirim ke provider untuk membuat jawaban. Di plan konsumen Anthropic (Free, Pro, Max), Anda sendiri yang memilih di privacy settings apakah chat dan sesi coding boleh dipakai untuk training. Plan komersial (Team, Enterprise, API) secara default tidak dipakai untuk training (pengumuman Anthropic tentang pembaruan Consumer Terms 2025 dan halaman privasi Claude). Plan bisnis OpenAI secara default juga tidak dipakai untuk training, sedangkan plan pribadi bisa saja dipakai, kecuali Anda memilih opt-out (halaman kebijakan data OpenAI).

### 10. Apakah Claude bisa membaca semua note saya?
Hanya yang Anda beri akses. Di Code tab, Anda memilih satu folder, lalu Claude membaca dan mencari file di dalam folder itu (REF-060, REF-049). Saya hanya memilih demo vault — tidak pernah satu drive penuh. Claude juga tidak membaca semua file untuk setiap pertanyaan; dia mencari yang relevan. Karena itu nama note dan link yang bagus sangat membantu.

### 11. Apakah ini aman?
Seaman pilihan yang Anda buat: folder mana yang dibagikan, plan apa yang dipakai, dan permission mode apa yang dijalankan. Claude bebas membaca folder itu, tapi harus minta izin setiap kali akan membuat file, dan aturan vault hanya mengizinkannya membuat note baru di satu folder (`08 AI Output`) dengan status belum direview. Informasi rahasia tidak saya masukkan ke vault. Untuk pemakaian di kantor, ikuti kebijakan tool yang disetujui organisasi Anda.

### 12. Apakah ini bisa dipakai untuk informasi proyek yang rahasia?
Secara default tidak, dan tidak di akun pribadi. Hanya boleh dengan tool, plan, dan settings yang sudah disetujui organisasi untuk data tersebut — dan tetap terapkan prinsip need-to-know. Justru itu sebabnya proyek hari ini fiktif.

### 13. Kenapa Claude?
Di Claude Desktop, Code tab bisa langsung bekerja di folder lokal tanpa setup tambahan. Dia juga menunjukkan file mana saja yang dibuka. Lalu ada file instruksi proyek (`CLAUDE.md`) yang bisa saya pakai untuk menyuruhnya menyebut note sumbernya (REF-060; dokumentasi Claude Code tentang memory files). Kombinasi itu membuat demo-nya sederhana dan bisa ditelusuri. Asisten lain, seperti ChatGPT atau Codex, mungkin punya kemampuan yang mirip.

### 14. Apakah saya perlu MCP?
Untuk alur kerja ini, tidak. MCP (Model Context Protocol) adalah standar terbuka untuk menghubungkan aplikasi AI ke sumber data dan tool (modelcontextprotocol.io). MCP berguna kalau Anda ingin aplikasi AI menjangkau sistem yang tidak bisa disediakan oleh folder lokal. Di sini, satu folder berisi file Markdown sudah cukup — jadi saya buat sederhana saja.

### 15. Bagaimana mencegah jawaban AI yang salah?
Tidak bisa dicegah sepenuhnya — yang bisa dilakukan adalah mengelolanya. Saya minta AI menyebut nama note sumbernya. Saya suruh dia bilang "Not in vault" kalau jawabannya sudah di luar note saya. Note-nya saya jaga tetap jelas dan terstruktur. Dan untuk hal yang penting, saya cek sendiri dengan membuka note yang disebut. Untuk keputusan nyata, penilaian profesional dan proses review yang biasa tetap berlaku.

### 16. Bukankah ini pada dasarnya RAG?
Sangat mirip. Retrieval-augmented generation adalah ide riset: ambil dokumen yang relevan, lalu buat jawaban dari dokumen itu (REF-058). Di sini, asistennya mengambil informasi dengan mencari dan membaca file saya secara langsung, bukan lewat vector index yang dibangun terpisah. Prinsipnya sama: jawaban harus berdasar pada sumber yang Anda kendalikan sendiri.

### 17. Apakah AI bisa mengubah schedule?
Tidak di alur kerja ini. Vault berisi pengetahuan, bukan schedule yang sedang berjalan. Asisten bisa membaca file hasil export seperti CSV atau Excel, tapi perubahan schedule tetap dilakukan di tool scheduling, lewat change control yang biasa.

---

## Tentang Isi

### 18. Apakah Project Alpha berdasarkan proyek nyata?
Tidak. Project Alpha sepenuhnya fiktif — nama, aktivitas, tanggal, kuantitas, dan masalahnya dibuat untuk demo. Situasinya memang umum di planning konstruksi, makanya terasa familiar.

### 19. Apakah "empat dari lima siap" itu realistis?
Kasusnya fiktif, tapi polanya umum: sebagian besar prasyarat terlihat siap, lalu ada satu penghambat — akses, izin, jadwal inspeksi, atau interface — yang menghentikan pekerjaan. Itulah alasan kita melakukan lookahead dan constraint review (REF-009).

### 20. Apakah level commissioning (L1–L5) itu standar?
Itu konvensi yang banyak dipakai di industri, bukan satu standar universal, dan penamaannya berbeda-beda antar-organisasi (REF-025). Selalu pakai definisi yang ada di commissioning plan proyek Anda.

### 21. Anda menyebut DCMA check di vault — apakah itu berlaku untuk konstruksi?
DCMA check berasal dari panduan penilaian schedule milik lembaga pertahanan Amerika Serikat. Check itu berguna sebagai indikator penyaringan, bukan standar konstruksi. Hasil merah artinya "perlu dicek", bukan "gagal" (pamflet DCMA 2012 dan ulasan Mosaic Projects). Panduan penilaian schedule dari GAO adalah referensi best practice yang lebih luas (REF-001).

### 22. Berapa lama membuat semua ini?
Saran jawaban yang jujur: "Demo vault dan proyek fiktifnya saya buat khusus untuk sesi ini, dan saya pakai AI untuk membantu membuat draft-nya — lalu saya review dan perbaiki sendiri. Itu justru bagian dari poinnya: AI mempercepat draft pertama; penilaian kita yang membuatnya bisa dipakai."

### 23. Kok catatannya sudah banyak? Bagaimana cara saya membuat vault seperti ini?
(Sudah disampaikan di slide 23 — kalau ditanya lagi, ulangi tiga tahapnya.) "Vault demo ini disiapkan khusus untuk sesi ini. Di pekerjaan nyata, mulainya kecil:
1. **Hari ini** — install Obsidian, buat satu folder, tulis satu catatan dari pekerjaan hari ini: temuan site walk, hasil rapat, atau issue di schedule.
2. **Minggu pertama** — setiap kejadian penting jadi satu catatan pendek. Ketik `[[` untuk menghubungkannya ke activity atau konsep yang terkait. Kalau ada pelajaran yang berlaku umum, jadikan satu catatan lesson.
3. **Bulan pertama** — dua sampai tiga catatan per hari kerja sudah sekitar 50 catatan, kira-kira sebesar vault ini. Sisihkan 15 menit seminggu untuk merapikan dan menambah link.

Tidak perlu struktur sempurna di awal. Vault tidak dibuat dalam sehari — satu catatan, satu link, setiap hari."

### 24. Apakah cara ini sudah dipakai di proyek sungguhan atau jadi standar di perusahaan Anda?
"Belum — ini masih eksperimen pribadi saya, dan saya sendiri masih belajar. Ini bukan standar kerja atau rekomendasi resmi perusahaan mana pun. Yang saya bagikan adalah polanya: catat, hubungkan, pakai ulang, dan kalau pakai AI, selalu cek sumbernya. Kalau mau mencoba di kantor, pastikan dulu tools dan cara menyimpan datanya sesuai kebijakan IT dan kerahasiaan di tempat kerja masing-masing."
