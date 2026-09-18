---
type: concept
domain: project-controls
status: evergreen
tags:
  - forecasting
  - project-controls
  - scheduling
references:
  - REF-001
updated: 2026-09-14
---

# Forecasting

> **Intinya:** Forecast finish adalah perkiraan terbaik saat ini tentang kapan pekerjaan benar-benar selesai, disusun dari progress nyata, remaining duration yang jujur, logic, dan risiko yang diketahui — dibandingkan dengan baseline, tapi tidak pernah disamakan dengan baseline.

Bagian dari [[Beranda Pengetahuan Planning]]

## Definisi

- **Baseline finish** — tanggal acuan yang sudah disetujui. Tanggal ini tidak bergeser mengikuti progress; lihat [[Baseline]].
- **Forecast finish** — tanggal yang sekarang dihitung schedule dari data date, berdasarkan progress actual, remaining duration, dan logic.
- **Variance** — selisih keduanya. Variance menunjukkan seberapa jauh kenyataan bergeser dari rencana; [[Total Float]] menunjukkan berapa banyak ruang yang tersisa sebelum milestone penting terdampak.

## Kenapa Penting

Keputusan — langkah recovery, resequencing, notice komersial — bergantung pada forecast. Forecast yang terus sama dengan baseline sampai detik terakhir menghilangkan waktu untuk bertindak. Forecast yang berubah-ubah tiap minggu juga cepat merusak kepercayaan.

## Sudut Pandang Planner

**Dua cara membuat forecast, dipakai bersamaan:**

| Pendekatan | Caranya | Kelebihan | Kekurangan |
|---|---|---|---|
| Berbasis tren | Proyeksi dari performa: produktivitas, task selesai vs rencana (BEI), efisiensi critical path (CPLI) | Cepat; membongkar asumsi yang tidak realistis | Mengasumsikan masa lalu memprediksi masa depan |
| Bottom-up | Menilai ulang remaining duration per activity bersama orang yang mengerjakannya, lalu hitung ulang | Detail; menangkap perubahan yang sudah diketahui | Rawan terlalu optimis dan tawar-menawar |

Kalau forecast bottom-up jauh lebih bagus daripada tren, saya tanya: apa yang akan berubah sehingga hasilnya bisa begitu?

**Remaining duration, secara jujur.** Remaining duration adalah waktu yang dibutuhkan untuk sisa pekerjaan, dengan resource dan constraint yang benar-benar ada — bukan durasi awal dikurangi waktu yang sudah lewat. Karena alasan inilah kebanyakan tool CPM memisahkan remaining duration dari percent complete. Saya cek apakah constraint yang masih terbuka sudah tercermin: activity tidak bisa mulai besok kalau permit-nya baru keluar beberapa minggu lagi.

**Forecast commissioning.** Forecast commissioning digerakkan oleh readiness, bukan hanya oleh tanggal selesai predecessor. Saya memperhitungkan approval script, ketersediaan vendor dan witness, laju penutupan issue, dan allowance retest yang realistis. Menurut pengalaman saya, di sinilah forecast paling sering terlalu optimis.

**Menyampaikan ketidakpastian.**

- Berikan tanggal beserta asumsi utamanya dan apa yang bisa mengubahnya.
- Tunjukkan path yang near-critical, bukan hanya yang critical.
- Pakai rentang kalau buktinya mendukung rentang; schedule risk analysis — salah satu best practice GAO — memberi cara terstruktur untuk membuatnya.
- Pisahkan forecast (yang saya perkirakan) dari target (yang sedang kami kejar).

## Contoh Praktis

Di [[Gambaran Umum Project Alpha|Project Alpha]], forecast delivery generator bergantung pada tanggal dari supplier yang bergeser setelah ada QA hold. Pendekatan berbasis tren bertanya apakah tanggal-tanggal supplier belakangan ini terbukti tepat; pendekatan bottom-up bertanya bukti progress manufaktur apa yang ada. Sampai bukti itu datang — action yang tercatat di [[Constraint Register]] — saya akan menganggap tanggal supplier sebagai asumsi yang perlu disebutkan, bukan fakta untuk dasar forecast.

## Kesalahan yang Sering Terjadi

- Forecast dibuat sama dengan baseline sampai ada yang membuktikan sebaliknya.
- Remaining duration berkurang mengikuti waktu yang lewat, terlepas dari pekerjaan yang benar-benar selesai.
- Mengabaikan path yang near-critical.
- Satu tanggal tunggal tanpa asumsi apa pun.
- "Recovery" forecast di atas kertas dengan memadatkan durasi commissioning.

## Konsep Terkait

- [[Baseline]] — acuan tetap untuk mengukur forecast.
- [[Total Float]] — berapa ruang yang tersisa, dan di mana ruang itu terpakai.
- [[Schedule Delay]] — pergeseran forecast perlu diidentifikasi penyebabnya.
- [[Schedule Recovery]] — respons saat forecast mengancam milestone penting.
- [[Pantau Float, Bukan Hanya Tanggal]] — lesson learned tentang membaca forecast lewat tren float.

## Referensi

- [[REF-001 GAO Schedule Assessment Guide|REF-001]] — update status dengan progress actual, menyesuaikan forecast sisa pekerjaan, dan schedule risk analysis.
