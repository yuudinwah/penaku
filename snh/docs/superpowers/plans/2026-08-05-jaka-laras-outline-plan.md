# Jaka dan Laras Outline Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Membuat 39 berkas kerangka yang memetakan cerita Jaka dan Laras dalam versi utama, POV Jaka, dan POV Laras sebelum prosa lengkap ditulis.

**Architecture:** `id/` menjadi canon naratif dan menetapkan semua kejadian objektif. `id-male/` dan `id-female/` mengikuti kejadian yang sama, tetapi mengganti batas informasi, fokus indrawi, penafsiran, dan konflik batin. Setiap berkas memakai skema kerangka yang sama agar ketiga versi dapat diaudit secara mekanis dan dibaca berdampingan.

**Tech Stack:** Markdown, Git, `rg`, `find`, `diff`, dan pemeriksaan manual lintas POV.

## Global Constraints

- Gunakan orang ketiga dekat dalam semua versi.
- Gunakan bahasa Indonesia natural, sederhana, dan tidak terasa seperti terjemahan.
- Cerita berlatar dusun fiktif di Jawa Tengah pada awal abad ke-20 tanpa menyebut tahun.
- Jaka menggarap sawah sewaan dan tegalan kecil; Laras adalah jelmaan kuntul kerbau.
- Jaka dan Laras telah menikah selama tiga tahun sebelum Jaka sakit.
- Penyakit tanpa nama berlangsung sembilan sampai sebelas bulan, dari kemarau pertama hingga awal kemarau kedua.
- Fakta objektif, urutan musim, dialog penting, luka, barang, dan peristiwa harus sama di ketiga versi.
- Nasib akhir Laras ambigu; cinta Jaka dan Laras tidak ambigu.
- Tahap ini menghasilkan kerangka rinci, bukan prosa lengkap.
- Setiap berkas wajib memuat tepat satu heading judul dan bagian `Tujuan bab`, `Urutan adegan`, `Konflik batin`, `Batas informasi`, `Motif`, dan `Kait ke bab berikutnya`. `epilogue.md` mengganti bagian terakhir dengan `Kesan akhir`.

## File Map

Setiap direktori berikut menghasilkan tiga belas berkas dengan nama identik:

```text
prologue.md
chapter-1.md
chapter-2.md
chapter-3.md
chapter-4.md
chapter-5.md
chapter-6.md
chapter-7.md
chapter-8.md
chapter-9.md
chapter-10.md
chapter-11.md
epilogue.md
```

- `id/`: canon naratif; misteri Laras dijaga sampai Bab 11.
- `id-male/`: seluruh kesadaran mengikuti Jaka; identitas Laras tidak diketahui sampai Bab 11.
- `id-female/`: seluruh kesadaran mengikuti Laras; identitasnya diketahui sejak awal.

---

### Task 1: Kerangka versi utama pada `id/`

**Files:**
- Create: `id/prologue.md`
- Create: `id/chapter-1.md`
- Create: `id/chapter-2.md`
- Create: `id/chapter-3.md`
- Create: `id/chapter-4.md`
- Create: `id/chapter-5.md`
- Create: `id/chapter-6.md`
- Create: `id/chapter-7.md`
- Create: `id/chapter-8.md`
- Create: `id/chapter-9.md`
- Create: `id/chapter-10.md`
- Create: `id/chapter-11.md`
- Create: `id/epilogue.md`

**Interfaces:**
- Consumes: keputusan canon dalam `docs/superpowers/specs/2026-08-05-jaka-laras-story-design.md`.
- Produces: urutan objektif adegan, cuaca, musim, benda, luka, dialog jangkar, dan transisi waktu yang wajib diikuti dua versi POV.

- [ ] **Step 1: Tulis Prolog sampai Bab 3**

Gunakan judul dan isi wajib berikut:

- Prolog, `Pertanyaan pada Malam Badai`: potongan Bab 11; Laras mengajukan pertanyaan terakhir; cahaya lampu padam sebelum jawaban lengkap dan nasibnya terlihat.
- Bab 1, `Rumah yang Terlalu Sepi`: rutinitas Jaka, satu piring, rumah bocor, sawah sewaan, tegalan, warga yang berkeluarga, dan keyakinan Jaka bahwa ia tidak pantas dipilih.
- Bab 2, `Burung di Tengah Badai`: perjalanan pulang, kuntul terjerat, pikiran lapar untuk memasaknya, rasa malu, pembebasan, serta burung yang menghilang ke balik hujan.
- Bab 3, `Perempuan di Ambang Rumah`: badai berlanjut keesokan hari, Jaka tidak ke ladang, Laras berteduh di emper rumah, tawaran masuk, makanan hangat, dan alasan Laras tidak memiliki tujuan.

- [ ] **Step 2: Tulis Bab 4 sampai Bab 6**

- Bab 4, `Satu Hari Lagi`: pembagian ruang dan pekerjaan, kesalahan porsi makanan, perbaikan tempat tidur, suara langkah, serta Laras terus menunda pergi.
- Bab 5, `Orang yang Memilih Tinggal`: gunjingan warga, Jaka meminta Laras mencari hidup lebih layak, Laras memilihnya secara sadar, pengakuan sederhana, dan pernikahan kecil.
- Bab 6, `Musim yang Baik`: tiga tahun pernikahan melalui rangkaian adegan konkret; hasil ladang buruk yang dimasak Laras, perselisihan kecil, rencana memperbaiki rumah, pertanyaan ringan mengenai perubahan rupa atau suara, serta pertanda Laras tidak sepenuhnya manusia tanpa mengungkap identitasnya.

- [ ] **Step 3: Tulis Bab 7 sampai Bab 9**

- Bab 7, `Ketika Jaka Tidak Bisa Bangun`: kemarau panjang, tanaman rusak, Jaka memaksakan diri, tumbang karena panas, pemeriksaan tabib, dan kegagalan tubuhnya pulih.
- Bab 8, `Bulan-Bulan yang Hilang`: musim peralihan, demam berulang, sawah terbengkalai, persediaan menipis, biaya tabib, musim hujan, dan kemunculan kain pertama tanpa membuka sumbernya.
- Bab 9, `Tangan yang Berubah`: penjualan kain berulang, obat yang membantu sementara, tubuh Laras makin kurus, luka pada tangan, pertanyaan apakah Jaka tetap mencintai tangannya, dan kecurigaan Jaka.

- [ ] **Step 4: Tulis Bab 10, Bab 11, dan Epilog**

- Bab 10, `Pergilah Jika Itu Membuatmu Bahagia`: Jaka sengaja menyakiti Laras, Laras pergi sampai tepi hutan, rumah kembali sunyi, Laras memilih pulang, dan rekonsiliasi yang belum menyelesaikan rahasia.
- Bab 11, `Bulu Terakhir`: awal kemarau kedua, pohon mengering dan roboh, janji batin Laras, ruang tenun, Jaka menyaksikan sebagian perubahan, hujan badai pertama, pertanyaan prolog, serta jawaban Jaka.
- Epilog, `Setelah Badai`: kain terakhir, jendela terbuka, bulu putih, jejak yang larut, nasib Laras tanpa kepastian, dan kedua pertolongan yang saling mencerminkan.

- [ ] **Step 5: Verifikasi struktur versi utama**

Run:

```bash
find id -maxdepth 1 -type f -name '*.md' | sort
rg -L '^## Tujuan bab$' id/prologue.md id/chapter-*.md
rg -L '^## Urutan adegan$' id/prologue.md id/chapter-*.md
rg -L '^## Konflik batin$' id/prologue.md id/chapter-*.md
rg -L '^## Batas informasi$' id/prologue.md id/chapter-*.md
rg -L '^## Motif$' id/prologue.md id/chapter-*.md
rg -L '^## Kait ke bab berikutnya$' id/prologue.md id/chapter-*.md
rg -n 'kuntul kerbau|tiga tahun|kemarau kedua|bukan lagi manusia' id
```

Expected:

- `find` menampilkan tepat 13 berkas.
- Enam perintah `rg -L` tidak menghasilkan keluaran.
- Pencarian canon menemukan kuntul pada Bab 2, tiga tahun pada Bab 6, kemarau kedua pada Bab 11, dan pertanyaan identitas pada Prolog/Bab 11.

- [ ] **Step 6: Commit versi utama**

```bash
git add id
git commit -m "docs: outline main Jaka and Laras story"
```

### Task 2: Kerangka POV Jaka pada `id-male/`

**Files:**
- Create: `id-male/prologue.md`
- Create: `id-male/chapter-1.md`
- Create: `id-male/chapter-2.md`
- Create: `id-male/chapter-3.md`
- Create: `id-male/chapter-4.md`
- Create: `id-male/chapter-5.md`
- Create: `id-male/chapter-6.md`
- Create: `id-male/chapter-7.md`
- Create: `id-male/chapter-8.md`
- Create: `id-male/chapter-9.md`
- Create: `id-male/chapter-10.md`
- Create: `id-male/chapter-11.md`
- Create: `id-male/epilogue.md`

**Interfaces:**
- Consumes: seluruh fakta objektif dari `id/`; hanya hal yang Jaka lihat, dengar, ingat, rasakan, atau simpulkan boleh masuk kesadarannya.
- Produces: perjalanan batin Jaka dari rasa tidak pantas, syukur, takut kehilangan, keruntuhan harga diri, rasa bersalah, hingga penerimaan identitas Laras.

- [ ] **Step 1: Tulis kerangka Prolog sampai Bab 5 dengan fokus Jaka**

Pertahankan adegan objektif versi utama. Tambahkan secara eksplisit:

- Prolog: ketakutan Jaka bahwa jawaban jujurnya sudah terlambat.
- Bab 1: kebiasaan merendahkan diri sebelum orang lain menolaknya.
- Bab 2: lapar, pertimbangan memasak burung, dan keputusan bahwa kemiskinan tidak boleh menjadikannya kejam.
- Bab 3: kecurigaan bahwa Laras adalah penipu atau mimpi; rasa mustahil perempuan seperti itu mencarinya.
- Bab 4: kecemasan setiap kali Laras menyebut kepulangan.
- Bab 5: ketidakmampuan percaya bahwa Laras memilih dirinya tanpa paksaan.

- [ ] **Step 2: Tulis kerangka Bab 6 sampai Epilog dengan fokus Jaka**

Tambahkan secara eksplisit:

- Bab 6: kebahagiaan yang terasa terlalu baik untuk bertahan.
- Bab 7: keyakinan bahwa nilai suami terletak pada kerja dan nafkah.
- Bab 8: rasa malu mendengar Laras bekerja sementara ia terbaring.
- Bab 9: keinginan bertanya tentang luka berlawanan dengan ketakutan mengetahui harganya.
- Bab 10: kebohongan untuk mengusir Laras dan harapan egois agar Laras tidak menurut.
- Bab 11: pengetahuan bahwa burung yang diselamatkannya adalah Laras, rasa syukur yang berubah menjadi rasa bersalah, lalu pilihan mencintai Laras dalam rupa apa pun.
- Epilog: kehilangan dan syukur hidup berdampingan; Jaka tidak menganggap pertolongan Laras sebagai utang.

- [ ] **Step 3: Audit batas pengetahuan Jaka**

Run:

```bash
rg -n 'aku adalah kuntul|bulu tubuhnya sendiri|berubah menjadi manusia|datang untuk membalas budi' id-male/prologue.md id-male/chapter-{1..10}.md
find id-male -maxdepth 1 -type f -name '*.md' | wc -l
```

Expected:

- Pencarian fakta rahasia tidak menghasilkan keluaran sebelum Bab 11.
- Jumlah berkas adalah `13`.

- [ ] **Step 4: Commit POV Jaka**

```bash
git add id-male
git commit -m "docs: outline Jaka point of view"
```

### Task 3: Kerangka POV Laras pada `id-female/`

**Files:**
- Create: `id-female/prologue.md`
- Create: `id-female/chapter-1.md`
- Create: `id-female/chapter-2.md`
- Create: `id-female/chapter-3.md`
- Create: `id-female/chapter-4.md`
- Create: `id-female/chapter-5.md`
- Create: `id-female/chapter-6.md`
- Create: `id-female/chapter-7.md`
- Create: `id-female/chapter-8.md`
- Create: `id-female/chapter-9.md`
- Create: `id-female/chapter-10.md`
- Create: `id-female/chapter-11.md`
- Create: `id-female/epilogue.md`

**Interfaces:**
- Consumes: seluruh fakta objektif dari `id/`; identitas Laras diketahui, tetapi pikiran Jaka hanya boleh ia tafsirkan melalui ucapan dan tindakan.
- Produces: perjalanan Laras dari ketakutan terhadap manusia, utang budi, penemuan rumah, cinta, godaan untuk pergi, hingga pengorbanan yang disadari.

- [ ] **Step 1: Tulis kerangka Prolog sampai Bab 5 dengan fokus Laras**

Pertahankan adegan objektif versi utama. Tambahkan secara eksplisit:

- Prolog: kesadaran bahwa ia mungkin kehilangan wujud, rumah, dan Jaka.
- Bab 1: kehidupan sebagai kuntul, kebebasan yang sepi, dan pengamatan terhadap manusia.
- Bab 2: ketakutan ketika terjerat, pembacaan atas keraguan Jaka, dan keterkejutan saat dilepas tanpa syarat.
- Bab 3: niat awal hanya berterima kasih; badai dipakai sebagai alasan tinggal.
- Bab 4: usaha mencari alasan untuk menunda kepergian satu hari lagi.
- Bab 5: kesadaran bahwa pilihannya tidak lagi didorong utang budi.

- [ ] **Step 2: Tulis kerangka Bab 6 sampai Epilog dengan fokus Laras**

Tambahkan secara eksplisit:

- Bab 6: rasa takut kehilangan rumah jika identitasnya diketahui.
- Bab 7: kemungkinan kehilangan manusia pertama yang memberinya tempat pulang.
- Bab 8: penemuan cara menenun bagian tubuhnya dan keputusan mengambil hanya sedikit.
- Bab 9: siklus `satu kali lagi`, sakit fisik, kebohongan, serta pertanyaan mengenai tangannya.
- Bab 10: kemarahan kepada Jaka, kesempatan kembali menjadi bebas, perjalanan ke tepi hutan, dan pilihan pulang.
- Bab 11: pohon roboh, janji tidak membiarkan Jaka tumbang, pengorbanan terakhir yang diakui sebagai cinta, dan ketakutan ditolak dalam wujud asli.
- Epilog: kesadaran dibuat samar tanpa memastikan apakah Laras hidup, mati, pergi, atau berubah.

- [ ] **Step 3: Audit batas pengetahuan Laras**

Run:

```bash
rg -n 'Jaka berpikir|dalam pikiran Jaka|Jaka diam-diam berharap|Jaka takut bahwa' id-female
find id-female -maxdepth 1 -type f -name '*.md' | wc -l
```

Expected:

- Pencarian pembacaan pikiran Jaka tidak menghasilkan keluaran; perasaannya hanya ditafsirkan Laras.
- Jumlah berkas adalah `13`.

- [ ] **Step 4: Commit POV Laras**

```bash
git add id-female
git commit -m "docs: outline Laras point of view"
```

### Task 4: Audit canon lintas versi

**Files:**
- Modify only if audit finds a contradiction: `id/*.md`
- Modify only if audit finds a contradiction: `id-male/*.md`
- Modify only if audit finds a contradiction: `id-female/*.md`

**Interfaces:**
- Consumes: 39 kerangka dari Tasks 1–3.
- Produces: tiga versi yang mempunyai canon objektif identik dan perjalanan batin berbeda.

- [ ] **Step 1: Verifikasi jumlah dan nama berkas**

Run:

```bash
for dir in id id-male id-female; do find "$dir" -maxdepth 1 -type f -name '*.md' -exec basename {} \; | sort; done
```

Expected: setiap blok direktori menampilkan daftar 13 nama yang sama: prolog, sebelas bab, dan epilog.

- [ ] **Step 2: Bandingkan heading judul per bab**

Run:

```bash
for file in prologue.md chapter-{1..11}.md epilogue.md; do sed -n '1p' "id/$file"; sed -n '1p' "id-male/$file"; sed -n '1p' "id-female/$file"; done
```

Expected: masing-masing kelompok tiga baris mempunyai judul bab yang sama.

- [ ] **Step 3: Audit delapan jangkar canon secara manual**

Periksa ketiga versi untuk memastikan fakta berikut terjadi pada bab yang sama:

1. Kuntul dibebaskan pada Bab 2.
2. Laras masuk ke rumah pada Bab 3.
3. Pernikahan terjadi pada Bab 5.
4. Lompatan tiga tahun dinyatakan pada Bab 6.
5. Jaka tumbang pada Bab 7.
6. Kain pertama muncul pada Bab 8 dan luka tangan dibahas pada Bab 9.
7. Laras pergi ke tepi hutan lalu kembali pada Bab 10.
8. Kemarau kedua, perubahan, pertanyaan terakhir, dan hujan badai terjadi pada Bab 11.

- [ ] **Step 4: Audit skema seluruh kerangka**

Run:

```bash
rg -L '^## Tujuan bab$' id*/prologue.md id*/chapter-*.md
rg -L '^## Urutan adegan$' id*/prologue.md id*/chapter-*.md
rg -L '^## Konflik batin$' id*/prologue.md id*/chapter-*.md
rg -L '^## Batas informasi$' id*/prologue.md id*/chapter-*.md
rg -L '^## Motif$' id*/prologue.md id*/chapter-*.md
rg -L '^## Kait ke bab berikutnya$' id*/prologue.md id*/chapter-*.md
rg -L '^## Kesan akhir$' id*/epilogue.md
```

Expected: semua perintah tidak menghasilkan keluaran.

- [ ] **Step 5: Perbaiki hanya kontradiksi yang ditemukan dan ulangi Steps 1–4**

Gunakan versi `id/` sebagai sumber kebenaran untuk fakta objektif. Pertahankan perbedaan interpretasi yang memang berasal dari POV. Expected: semua pemeriksaan lulus tanpa menghapus konflik batin khas setiap versi.

- [ ] **Step 6: Commit audit akhir bila ada perbaikan**

```bash
git add id id-male id-female
git commit -m "docs: align Jaka and Laras story outlines"
```

Jika audit tidak memerlukan perubahan, jangan membuat commit kosong.
