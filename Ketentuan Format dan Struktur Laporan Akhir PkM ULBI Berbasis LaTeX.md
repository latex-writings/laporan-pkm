# KETENTUAN FORMAT DAN STRUKTUR LAPORAN AKHIR PENGABDIAN KEPADA MASYARAKAT (PkM)

## Acuan Penyusunan Template LaTeX Laporan Akhir PkM 2026

---

## 1. Pendahuluan

Dokumen ini merupakan pedoman penyusunan **Laporan Akhir Pengabdian kepada Masyarakat (PkM)** menggunakan LaTeX dengan mengacu pada format Laporan Akhir PkM Universitas Logistik dan Bisnis Internasional (ULBI) Tahun 2025.

Pedoman ini digunakan sebagai dasar untuk:

- membangun template LaTeX laporan akhir PkM;
- menjaga konsistensi format seluruh dokumen;
- menyusun struktur BAB dan subbab;
- mengatur halaman awal dan penomoran;
- mengatur tabel, gambar, dan lampiran;
- mengatur sitasi dan daftar pustaka;
- menghindari inkonsistensi format yang ditemukan pada laporan sebelumnya; dan
- mempermudah pengembangan laporan PkM tahun 2026.

---

# 2. FORMAT DASAR DOKUMEN

## 2.1 Ukuran Kertas

Ketentuan kertas:

- Ukuran: **A4**
- Orientasi: **Portrait**
- Ukuran A4: **210 mm × 297 mm**

Konfigurasi LaTeX:

```latex
\documentclass[12pt,a4paper]{report}
```

---

## 2.2 Margin

Format margin yang digunakan sebagai acuan adalah:

| Posisi | Margin |
|---|---:|
| Kiri | 4 cm |
| Kanan | 3 cm |
| Atas | 4 cm |
| Bawah | 3 cm |

Konfigurasi LaTeX:

```latex
\usepackage[
    left=4cm,
    right=3cm,
    top=4cm,
    bottom=3cm
]{geometry}
```

Margin harus digunakan secara konsisten pada seluruh bagian utama laporan.

Lampiran tertentu yang berupa dokumen hasil pindai dapat menyesuaikan ukuran dokumen asli.

---

# 3. FONT DAN TIPOGRAFI

## 3.1 Font Utama

Font utama yang digunakan adalah:

**Times New Roman**

Ukuran font isi utama:

**12 pt**

Jika menggunakan XeLaTeX atau LuaLaTeX:

```latex
\usepackage{fontspec}
\setmainfont{Times New Roman}
```

---

## 3.2 Format Teks Isi

Ketentuan isi paragraf:

- Font: Times New Roman
- Ukuran: 12 pt
- Perataan: rata kiri-kanan atau *justified*
- Spasi: 1,5
- Indentasi awal paragraf: sekitar 0,75 cm
- Tidak menggunakan jarak kosong berlebihan antarparagraf

Contoh konfigurasi:

```latex
\usepackage{setspace}
\onehalfspacing

\setlength{\parindent}{0.75cm}
\setlength{\parskip}{0pt}
```

---

# 4. FORMAT JUDUL BAB

Judul BAB menggunakan format:

- Times New Roman
- 16 pt
- Bold
- Huruf kapital
- Posisi tengah
- BAB dan nama BAB ditulis pada dua baris
- Setiap BAB dimulai pada halaman baru

Contoh:

```text
BAB I
PENDAHULUAN
```

Struktur BAB yang digunakan:

```text
BAB I
PENDAHULUAN

BAB II
TINJAUAN PUSTAKA

BAB III
METODE PELAKSANAAN

BAB IV
HASIL DAN LUARAN YANG DICAPAI

BAB V
KESIMPULAN DAN REKOMENDASI
```

---

# 5. FORMAT SUBBAB

Subbab menggunakan sistem penomoran desimal.

Contoh:

```text
1.1 Analisis Situasi Permasalahan
1.2 Permasalahan Mitra
1.3 Tujuan Pengabdian
```

Format yang direkomendasikan:

| Tingkat | Format |
|---|---|
| BAB | 16 pt, Bold, Uppercase, Center |
| Subbab | 14 pt, Bold |
| Sub-subbab | 12 pt, Bold |
| Isi | 12 pt, Regular |

Format ini digunakan secara konsisten pada seluruh BAB.

---

# 6. SPASI DAN PARAGRAF

Ketentuan paragraf:

- spasi antarbaris 1,5;
- paragraf rata kiri-kanan;
- indentasi awal paragraf ±0,75 cm;
- tidak perlu menambahkan satu baris kosong antarparagraf;
- istilah asing menggunakan huruf miring apabila sesuai dengan kaidah penulisan ilmiah.

Contoh:

```latex
\textit{machine learning}
```

```latex
\textit{deep learning}
```

```latex
\textit{computer vision}
```

```latex
\textit{pre-test}
```

```latex
\textit{post-test}
```

Nama metode atau algoritma seperti berikut tidak wajib dimiringkan:

- ResNet9
- YOLO
- Grad-CAM
- DeepKNN
- CNN

---

# 7. SISTEM PENOMORAN HALAMAN

Laporan menggunakan dua jenis penomoran halaman.

## 7.1 Bagian Awal

Bagian awal menggunakan angka Romawi kecil:

```text
i
ii
iii
iv
v
vi
vii
```

Susunan yang digunakan:

| Bagian | Nomor |
|---|---|
| Cover | Tidak ditampilkan |
| Halaman Pengesahan | i |
| Halaman Keterlibatan Mahasiswa | ii |
| Ringkasan | iii |
| Prakata | iv |
| Daftar Isi | v dan seterusnya |
| Daftar Lampiran | Romawi |

Konfigurasi:

```latex
\pagenumbering{roman}
```

---

## 7.2 Bagian Utama

BAB I dimulai menggunakan angka Arab dan dimulai kembali dari halaman 1.

```latex
\clearpage
\pagenumbering{arabic}
\setcounter{page}{1}
```

---

# 8. POSISI NOMOR HALAMAN DAN FOOTER

Nomor halaman ditempatkan pada:

**kanan bawah halaman.**

Footer laporan menggunakan teks:

```text
Pengabdian Kepada Masyarakat Universitas Logistik dan Bisnis Internasional Tahun 2026
```

Format footer:

- Times New Roman;
- sekitar 9 pt;
- italic;
- berada pada sisi kiri bawah;
- nomor halaman berada pada sisi kanan bawah.

Contoh menggunakan `fancyhdr`:

```latex
\usepackage{fancyhdr}

\pagestyle{fancy}
\fancyhf{}

\fancyfoot[L]{
    \footnotesize\itshape
    Pengabdian Kepada Masyarakat Universitas Logistik dan Bisnis Internasional Tahun 2026
}

\fancyfoot[R]{\thepage}

\renewcommand{\headrulewidth}{0pt}
```

---

# 9. STRUKTUR COVER

Cover laporan memiliki susunan:

```text
LAPORAN AKHIR

PENGABDIAN KEPADA MASYARAKAT (PKM)


JUDUL KEGIATAN PENGABDIAN KEPADA MASYARAKAT


(Studi Kasus: Nama Mitra)


LOGO UNIVERSITAS


Oleh:

Nama Ketua
Nama Anggota
Nama Anggota


PROGRAM STUDI

UNIVERSITAS LOGISTIK DAN BISNIS INTERNASIONAL

TAHUN 2026
```

Ketentuan:

- posisi teks mayoritas center;
- judul utama menggunakan huruf kapital;
- judul menggunakan bold;
- nama anggota tim disertai identitas yang diperlukan seperti NIDN;
- nama program studi dituliskan secara lengkap;
- nama universitas menggunakan huruf kapital;
- tahun laporan ditempatkan di bagian bawah.

Cover tidak menampilkan nomor halaman.

---

# 10. HALAMAN PENGESAHAN

Setelah cover terdapat:

# HALAMAN PENGESAHAN

Halaman pengesahan memuat informasi seperti:

- logo ULBI;
- judul kegiatan;
- ketua tim;
- NIDN/NIK;
- anggota tim;
- program studi;
- nilai pendanaan;
- pihak yang mengetahui;
- ketua kegiatan;
- tanda tangan;
- QR Code apabila tersedia;
- tanggal pengesahan.

Apabila LPPM menyediakan lembar pengesahan resmi dalam bentuk PDF, disarankan untuk memasukkan halaman PDF tersebut secara langsung.

Contoh:

```latex
\usepackage{pdfpages}

\includepdf[
    pages=-,
    pagecommand={}
]{assets/pengesahan.pdf}
```

---

# 11. HALAMAN KETERLIBATAN MAHASISWA

Bagian berikutnya adalah:

# HALAMAN KETERLIBATAN MAHASISWA

Tabel menggunakan struktur:

| No | Nama Mahasiswa | NPM | Bentuk Keterlibatan | Tanda Tangan |
|---:|---|---|---|---|

Setiap mahasiswa harus dijelaskan bentuk keterlibatannya dalam kegiatan.

Contoh bentuk keterlibatan:

- membantu persiapan kegiatan;
- menjadi fasilitator;
- memberikan pendampingan praktikum;
- membantu dokumentasi;
- membantu pengolahan data evaluasi;
- membantu penyampaian materi;
- membantu siswa selama kegiatan berlangsung.

Pada bagian bawah halaman dicantumkan:

```text
Bandung, [Tanggal]

Ketua Tim Pengabdi


[Nama Ketua]
[Identitas]
```

---

# 12. RINGKASAN

Bagian setelah keterlibatan mahasiswa adalah:

# RINGKASAN

Istilah yang digunakan adalah **Ringkasan**, bukan Abstrak.

Ringkasan sebaiknya mencakup:

1. kondisi atau permasalahan mitra;
2. kebutuhan mitra;
3. solusi yang diberikan;
4. bentuk kegiatan PkM;
5. metode pelaksanaan;
6. metode evaluasi;
7. hasil utama kegiatan;
8. dampak kegiatan;
9. luaran yang dihasilkan.

Pada bagian akhir ditambahkan:

```text
Kata Kunci:
```

Disarankan menggunakan sekitar 4–6 kata kunci yang merepresentasikan kegiatan.

---

# 13. PRAKATA

Bagian berikutnya:

# PRAKATA

Prakata sekurang-kurangnya mencakup:

1. ucapan syukur;
2. penyebutan kegiatan PkM;
3. tujuan penyusunan laporan;
4. ucapan terima kasih kepada pihak yang membantu;
5. harapan terhadap kebermanfaatan kegiatan;
6. tempat dan waktu penyusunan laporan;
7. identitas tim pengabdi.

Pihak yang dapat disebutkan antara lain:

- Rektor ULBI;
- LPPM ULBI;
- pimpinan sekolah mitra;
- guru pendamping;
- peserta kegiatan;
- mahasiswa pendamping;
- pihak lain yang terlibat.

Pada bagian akhir:

```text
Bandung, [Bulan] 2026

Tim Pengabdi
```

---

# 14. DAFTAR ISI

Daftar isi dibuat otomatis menggunakan LaTeX.

```latex
\tableofcontents
```

Daftar isi mencakup:

- halaman awal;
- BAB;
- subbab;
- daftar pustaka;
- lampiran.

---

# 15. DAFTAR LAMPIRAN

Setelah daftar isi terdapat:

# DAFTAR LAMPIRAN

Lampiran yang digunakan berdasarkan laporan acuan adalah:

1. CV Ketua, Anggota, dan Mahasiswa yang terlibat;
2. Penggunaan Anggaran;
3. Gambaran Iptek yang telah dilaksanakan pada mitra;
4. Gambaran Lokasi Mitra dengan ULBI;
5. Surat Pernyataan Kesediaan Bekerja Sama dengan Mitra;
6. Dokumentasi Kegiatan;
7. Absensi Kegiatan;
8. Modul Pelatihan;
9. Bukti penerimaan artikel/LoA atau URL artikel yang telah dipublikasikan.

---

# 16. STRUKTUR UTAMA LAPORAN

Struktur utama laporan terdiri atas lima BAB.

```text
BAB I PENDAHULUAN

1.1 Analisis Situasi Permasalahan
1.2 Permasalahan Mitra
1.3 Tujuan Pengabdian
1.4 Manfaat Pengabdian
1.5 Luaran Pengabdian


BAB II TINJAUAN PUSTAKA

2.1 Pengertian/Teori Terkait Topik
2.2 Tinjauan Pustaka Sesuai Topik Permasalahan


BAB III METODE PELAKSANAAN

3.1 Tempat dan Waktu
3.2 Khalayak Sasaran
3.3 Metode Pengabdian
3.4 Indikator Keberhasilan
3.5 Metode Evaluasi


BAB IV HASIL DAN LUARAN YANG DICAPAI

4.1 Hasil Kegiatan
4.2 Analisis Keilmuan
4.3 Pengukuran Dampak Kegiatan
4.4 Luaran yang Dicapai


BAB V KESIMPULAN DAN REKOMENDASI

5.1 Kesimpulan
5.2 Rekomendasi
```

---

# 17. BAB I — PENDAHULUAN

## 17.1 Bagian Pengantar BAB

Setelah judul BAB I dapat diberikan paragraf pembuka yang menjelaskan isi keseluruhan BAB.

Contoh cakupan:

- latar belakang kegiatan;
- kondisi mitra;
- masalah yang ditemukan;
- tujuan;
- manfaat;
- luaran.

---

# 18. 1.1 ANALISIS SITUASI PERMASALAHAN

Bagian ini menjelaskan kondisi aktual mitra sebelum kegiatan PkM dilaksanakan.

Isi yang disarankan:

1. kondisi umum bidang yang menjadi fokus kegiatan;
2. perkembangan teknologi atau kebutuhan kompetensi;
3. karakteristik mitra;
4. hasil observasi awal;
5. kemampuan atau kondisi awal peserta;
6. kebutuhan yang belum terpenuhi;
7. tantangan yang dihadapi;
8. fakta atau literatur pendukung;
9. relevansi solusi yang akan diberikan;
10. alasan kegiatan PkM perlu dilaksanakan.

Penulisan sebaiknya tidak memberi kesan bahwa mitra memiliki kondisi yang buruk.

Framing yang dianjurkan adalah:

> Mitra telah memiliki kemampuan dasar yang baik, namun masih membutuhkan penguatan pada aspek tertentu agar lebih relevan dengan perkembangan teknologi dan kebutuhan saat ini.

---

# 19. 1.2 PERMASALAHAN MITRA

Permasalahan mitra disusun secara terstruktur dan bernomor.

Format:

```text
1. Permasalahan pertama
   Penjelasan.

2. Permasalahan kedua
   Penjelasan.

3. Permasalahan ketiga
   Penjelasan.
```

Permasalahan harus berasal dari:

- observasi;
- wawancara;
- diskusi;
- evaluasi kondisi awal;
- kebutuhan nyata mitra.

Permasalahan yang ditulis harus memiliki hubungan langsung dengan solusi yang diberikan melalui kegiatan PkM.

---

# 20. 1.3 TUJUAN PENGABDIAN

Bagian tujuan terdiri atas:

## Tujuan Umum

Menjelaskan tujuan utama kegiatan dalam satu paragraf.

## Tujuan Khusus

Disusun secara numerik.

Contoh:

```text
1. Meningkatkan ...
2. Memberikan ...
3. Memfasilitasi ...
4. Menghasilkan ...
5. Mengevaluasi ...
6. Memperkuat ...
```

Tujuan harus dapat dikaitkan dengan indikator keberhasilan dan hasil kegiatan.

---

# 21. 1.4 MANFAAT PENGABDIAN

Manfaat dikelompokkan berdasarkan pihak penerima manfaat.

Struktur yang direkomendasikan:

## 1. Bagi Siswa

a. ...  
b. ...  
c. ...

## 2. Bagi Guru

a. ...  
b. ...  
c. ...

## 3. Bagi Sekolah Mitra

a. ...  
b. ...  
c. ...

## 4. Bagi Mahasiswa Pendamping

a. ...  
b. ...  
c. ...

## 5. Bagi Perguruan Tinggi

a. ...  
b. ...  
c. ...

Dengan demikian manfaat tidak hanya berorientasi pada peserta, tetapi mencakup seluruh pemangku kepentingan kegiatan.

---

# 22. 1.5 LUARAN PENGABDIAN

Bagian ini menjelaskan luaran yang direncanakan atau dihasilkan.

Contoh kategori luaran:

1. modul pembelajaran;
2. peningkatan kompetensi peserta;
3. produk atau aplikasi;
4. dokumentasi kegiatan;
5. poster kegiatan;
6. artikel ilmiah;
7. buku;
8. HKI apabila tersedia;
9. publikasi media;
10. luaran tambahan lainnya.

Status luaran harus dituliskan dengan jelas.

Contoh:

```text
Artikel ilmiah — Submitted
Artikel ilmiah — Under Review
Artikel ilmiah — Accepted
Artikel ilmiah — Published
```

---

# 23. BAB II — TINJAUAN PUSTAKA

Struktur:

```text
BAB II
TINJAUAN PUSTAKA

2.1 Pengertian/Teori Terkait Topik
2.2 Tinjauan Pustaka Sesuai Topik Permasalahan
```

---

# 24. 2.1 PENGERTIAN/TEORI TERKAIT TOPIK

Bagian ini menjelaskan konsep dan teori yang digunakan dalam kegiatan PkM.

Untuk kegiatan berbasis teknologi, pembahasan dapat mencakup:

- definisi bidang utama;
- teknologi yang digunakan;
- metode pembelajaran;
- konsep sistem;
- konsep metode atau algoritma;
- keterkaitan teknologi dengan proses pembelajaran.

Tinjauan teori tidak perlu sepanjang tinjauan pustaka pada skripsi atau disertasi.

Fokus pada teori yang diperlukan untuk menjelaskan kegiatan PkM.

---

# 25. 2.2 TINJAUAN PUSTAKA SESUAI TOPIK PERMASALAHAN

Bagian ini membahas hasil penelitian atau kegiatan sebelumnya yang relevan dengan permasalahan mitra.

Fungsi utamanya adalah:

1. menunjukkan bahwa masalah yang diangkat relevan;
2. mendukung pemilihan solusi;
3. menunjukkan manfaat metode yang digunakan;
4. memberikan dasar akademik terhadap kegiatan PkM.

Literatur harus memiliki hubungan langsung dengan topik kegiatan.

---

# 26. BAB III — METODE PELAKSANAAN

Struktur:

```text
BAB III
METODE PELAKSANAAN

3.1 Tempat dan Waktu
3.2 Khalayak Sasaran
3.3 Metode Pengabdian
3.4 Indikator Keberhasilan
3.5 Metode Evaluasi
```

---

# 27. 3.1 TEMPAT DAN WAKTU

Bagian ini sekurang-kurangnya memuat:

- nama mitra;
- alamat mitra;
- kota/kabupaten;
- tanggal kegiatan;
- periode kegiatan;
- jumlah pertemuan;
- durasi setiap pertemuan;
- lokasi ruangan/laboratorium apabila relevan.

Informasi jumlah pertemuan harus konsisten dengan bagian hasil kegiatan.

---

# 28. 3.2 KHALAYAK SASARAN

Bagian ini menjelaskan karakteristik peserta kegiatan.

Harus memuat:

- kelompok sasaran;
- kelas/tingkat;
- program studi/jurusan;
- jumlah peserta;
- keterlibatan guru;
- keterlibatan pihak mitra lainnya apabila ada.

Jumlah peserta harus dituliskan secara spesifik.

---

# 29. 3.3 METODE PENGABDIAN

Metode pengabdian menjelaskan pendekatan dan tahapan kegiatan.

Tahapan dapat disusun sebagai berikut:

```text
1. Persiapan
2. Koordinasi dengan mitra
3. Penyusunan materi/modul
4. Evaluasi kondisi awal
5. Pelaksanaan pelatihan/workshop
6. Praktikum
7. Pendampingan peserta
8. Evaluasi
9. Dokumentasi
10. Penyusunan luaran
```

Tahapan harus disesuaikan dengan pelaksanaan kegiatan sebenarnya.

---

# 30. 3.4 INDIKATOR KEBERHASILAN

Indikator keberhasilan harus:

- terukur;
- spesifik;
- berhubungan dengan tujuan;
- memungkinkan untuk dievaluasi.

Contoh:

```text
1. Peserta mengikuti minimal 75% kegiatan.
2. Peserta mampu menyelesaikan kegiatan praktikum.
3. Terjadi peningkatan hasil post-test dibandingkan pre-test.
4. Modul pembelajaran berhasil disusun.
5. Produk kegiatan berhasil dibuat.
6. Luaran publikasi berhasil disiapkan.
```

Jika memungkinkan, gunakan indikator kuantitatif.

---

# 31. 3.5 METODE EVALUASI

Evaluasi dapat menggunakan beberapa metode.

## 1. Pre-Test

Digunakan untuk mengukur kemampuan awal peserta.

## 2. Post-Test

Digunakan untuk mengukur kemampuan peserta setelah kegiatan.

## 3. Observasi

Digunakan untuk melihat:

- keterlibatan peserta;
- kemampuan praktis;
- aktivitas selama kegiatan.

## 4. Kuesioner

Digunakan untuk mengukur:

- kepuasan peserta;
- kualitas materi;
- kualitas fasilitator;
- manfaat kegiatan.

## 5. Evaluasi Praktikum atau Proyek

Digunakan untuk mengukur kemampuan peserta dalam menerapkan materi.

## 6. Dokumentasi

Berupa:

- foto;
- video;
- absensi;
- catatan kegiatan;
- dokumen pendukung lainnya.

---

# 32. BAB IV — HASIL DAN LUARAN YANG DICAPAI

Struktur:

```text
BAB IV
HASIL DAN LUARAN YANG DICAPAI

4.1 Hasil Kegiatan
4.2 Analisis Keilmuan
4.3 Pengukuran Dampak Kegiatan
4.4 Luaran yang Dicapai
```

---

# 33. 4.1 HASIL KEGIATAN

Bagian ini menjelaskan pelaksanaan kegiatan yang benar-benar terjadi.

Pembahasan disusun berdasarkan urutan kegiatan.

Contoh:

```text
1. Persiapan kegiatan
2. Pembukaan
3. Pelaksanaan pre-test
4. Penyampaian materi
5. Praktikum
6. Pendampingan
7. Evaluasi
8. Post-test
9. Penutupan
```

Bagian ini dapat dilengkapi dengan:

- tabel kegiatan;
- dokumentasi;
- foto;
- diagram;
- data jumlah peserta.

---

# 34. 4.2 ANALISIS KEILMUAN

Bagian ini menghubungkan pelaksanaan kegiatan dengan bidang ilmu yang diterapkan.

Analisis harus menjelaskan:

1. konsep keilmuan yang digunakan;
2. bagaimana konsep tersebut diterapkan;
3. alasan pemilihan metode/teknologi;
4. relevansinya terhadap kebutuhan mitra;
5. bagaimana peserta memperoleh pengalaman atau kompetensi baru.

Bagian ini tidak hanya mendeskripsikan kegiatan, tetapi menjelaskan substansi akademik yang diterapkan.

---

# 35. 4.3 PENGUKURAN DAMPAK KEGIATAN

Bagian ini membandingkan kondisi:

```text
SEBELUM KEGIATAN
        ↓
PELAKSANAAN INTERVENSI
        ↓
SESUDAH KEGIATAN
```

Data yang dapat digunakan antara lain:

- skor pre-test;
- skor post-test;
- nilai rata-rata;
- median;
- peningkatan nilai;
- persentase peningkatan;
- distribusi nilai;
- hasil kuesioner;
- tingkat kepuasan;
- observasi keterampilan;
- keberhasilan praktikum.

Apabila tersedia data yang memadai, hasil dapat divisualisasikan menggunakan:

- tabel;
- diagram batang;
- diagram garis;
- boxplot;
- grafik perbandingan;
- visualisasi indikator.

Bagian ini harus menjadi bukti bahwa kegiatan PkM memberikan dampak nyata kepada mitra.

---

# 36. 4.4 LUARAN YANG DICAPAI

Bagian ini menjelaskan status nyata seluruh luaran kegiatan.

Contoh:

| Luaran | Target | Capaian | Status |
|---|---|---|---|
| Modul | 1 modul | 1 modul | Tercapai |
| Pelatihan | Dilaksanakan | Dilaksanakan | Tercapai |
| Artikel | Submitted | Submitted | Tercapai |
| Poster | 1 poster | 1 poster | Tercapai |
| Dokumentasi | Tersedia | Tersedia | Tercapai |

Luaran yang belum selesai harus diberikan status sebenarnya.

---

# 37. BAB V — KESIMPULAN DAN REKOMENDASI

Struktur:

```text
BAB V
KESIMPULAN DAN REKOMENDASI

5.1 Kesimpulan
5.2 Rekomendasi
```

---

# 38. 5.1 KESIMPULAN

Kesimpulan disusun dalam bentuk poin bernomor.

Kesimpulan harus menjawab:

1. apakah kegiatan berhasil dilaksanakan;
2. apakah tujuan kegiatan tercapai;
3. apakah terdapat peningkatan kompetensi;
4. bagaimana hasil evaluasi kegiatan;
5. apa luaran utama yang berhasil diperoleh;
6. apa dampak kegiatan terhadap mitra.

Kesimpulan tidak digunakan untuk memasukkan data atau pembahasan baru.

---

# 39. 5.2 REKOMENDASI

Rekomendasi dapat dibagi berdasarkan penerima rekomendasi.

Contoh:

## 1. Untuk Siswa

Rekomendasi pengembangan kompetensi lebih lanjut.

## 2. Untuk Guru

Rekomendasi integrasi materi ke pembelajaran.

## 3. Untuk Sekolah Mitra

Rekomendasi terkait keberlanjutan program.

## 4. Untuk Perguruan Tinggi

Rekomendasi pengembangan program PkM.

## 5. Untuk Kegiatan Selanjutnya

Rekomendasi pengembangan kegiatan PkM lanjutan.

---

# 40. DAFTAR PUSTAKA

Sistem sitasi yang digunakan adalah sistem numerik.

Contoh sitasi dalam teks:

```text
... berdasarkan penelitian sebelumnya [1].

... sebagaimana dijelaskan dalam [2], [3].
```

Daftar pustaka:

```text
[1] Nama Penulis, Judul, ...
[2] Nama Penulis, Judul, ...
```

Format LaTeX yang direkomendasikan:

```latex
\usepackage[
    backend=biber,
    style=ieee,
    sorting=none
]{biblatex}

\addbibresource{references.bib}
```

Pencetakan daftar pustaka:

```latex
\printbibliography[
    heading=bibintoc,
    title={DAFTAR PUSTAKA}
]
```

---

# 41. KETENTUAN GAMBAR

Gambar dapat berupa:

- dokumentasi kegiatan;
- diagram;
- workflow;
- grafik;
- visualisasi hasil;
- peta lokasi;
- tangkapan layar aplikasi.

Ketentuan:

- posisi gambar dibuat proporsional;
- gambar harus memiliki kualitas yang cukup baik;
- caption berada di bawah gambar;
- setiap gambar diberi nomor;
- gambar harus dirujuk pada narasi;
- gambar eksternal harus mencantumkan sumber.

Contoh:

```latex
\begin{figure}[H]
    \centering
    \includegraphics[width=0.8\textwidth]{figures/gambar1.png}
    \caption{Pelaksanaan kegiatan PkM.}
    \label{fig:kegiatan}
\end{figure}
```

---

# 42. DOKUMENTASI MULTI-GAMBAR

Dokumentasi dapat disusun dua kolom.

Contoh:

```text
Gambar 1             Gambar 2

Gambar 3             Gambar 4

Gambar 5             Gambar 6
```

LaTeX dapat menggunakan:

```latex
\usepackage{subcaption}
```

atau struktur `minipage`.

---

# 43. SUMBER GAMBAR

Gambar dari sumber eksternal harus memiliki sumber.

Contoh:

```text
Sumber: Google Maps
```

atau:

```text
Sumber: Dokumentasi Google Maps, 2026
```

Foto hasil dokumentasi kegiatan sendiri tidak harus memiliki sumber eksternal.

---

# 44. LAMPIRAN

Bagian lampiran menggunakan judul:

# LAMPIRAN-LAMPIRAN

---

# 45. LAMPIRAN 1 — CV KETUA, ANGGOTA, DAN MAHASISWA

CV mengikuti format akademik/DIKTI.

Dapat berisi:

- identitas diri;
- pendidikan;
- pengalaman mengajar;
- penelitian;
- pengabdian kepada masyarakat;
- publikasi;
- buku;
- HKI;
- keanggotaan;
- penghargaan;
- pengalaman organisasi;
- pelatihan;
- sertifikasi;
- tanda tangan.

Untuk mahasiswa dapat berisi:

- identitas diri;
- program studi;
- NIM;
- kegiatan kemahasiswaan;
- penghargaan;
- pernyataan kebenaran data;
- tanda tangan.

---

# 46. LAMPIRAN 2 — PENGGUNAAN ANGGARAN

Penggunaan anggaran disajikan dalam bentuk tabel.

Kategori dapat meliputi:

1. honorarium/gaji dan upah;
2. bahan habis pakai;
3. perjalanan;
4. kegiatan lainnya.

Tabel harus menunjukkan:

- jenis pengeluaran;
- justifikasi;
- kuantitas;
- harga satuan;
- jumlah;
- subtotal;
- total dana.

---

# 47. LAMPIRAN 3 — GAMBARAN IPTEK

Bagian ini menjelaskan ilmu pengetahuan dan teknologi yang telah ditransfer kepada mitra.

Struktur dapat berupa:

```text
1. Teknologi/konsep pertama
   Penjelasan.

2. Teknologi/konsep kedua
   Penjelasan.

3. Metode pembelajaran
   Penjelasan.

4. Modul
   Penjelasan.

5. Produk atau hasil akhir
   Penjelasan.
```

---

# 48. LAMPIRAN 4 — GAMBARAN LOKASI MITRA

Bagian ini menjelaskan lokasi mitra terhadap ULBI.

Berdasarkan laporan acuan terdapat ketentuan:

> Jarak lokasi mitra dengan Universitas Logistik dan Bisnis Internasional tidak lebih dari 200 km.

Bagian ini sebaiknya memuat:

- alamat mitra;
- jarak dari ULBI;
- estimasi waktu perjalanan;
- peta Google Maps;
- rute perjalanan;
- foto lokasi mitra.

Gambar eksternal mencantumkan sumber.

---

# 49. LAMPIRAN 5 — SURAT KESEDIAAN MITRA

Lampiran memuat:

**Surat Pernyataan Kesediaan Bekerja Sama dengan Mitra PkM.**

Dokumen menggunakan materai sesuai ketentuan yang berlaku.

Disarankan memasukkan surat yang telah ditandatangani dan dipindai.

Contoh:

```latex
\includepdf[
    pages=-,
    pagecommand={}
]{assets/surat-kesediaan-mitra.pdf}
```

---

# 50. LAMPIRAN 6 — DOKUMENTASI KEGIATAN

Dokumentasi mencakup foto-foto penting selama kegiatan.

Contoh:

1. pembukaan kegiatan;
2. penyampaian materi;
3. pelaksanaan praktikum;
4. pendampingan peserta;
5. evaluasi;
6. presentasi;
7. penutupan;
8. foto bersama.

Setiap foto diberikan caption yang menjelaskan kegiatan.

---

# 51. LAMPIRAN 7 — ABSENSI KEGIATAN

Absensi dimasukkan sebagai dokumen hasil pindai.

Absensi harus memperlihatkan:

- nama peserta;
- tanggal;
- tanda tangan;
- identitas kegiatan.

Jika terdiri dari beberapa halaman, seluruh halaman dapat dimasukkan menggunakan `pdfpages`.

---

# 52. LAMPIRAN 8 — MODUL PELATIHAN

Tidak harus memasukkan seluruh isi modul ke dalam laporan utama.

Lampiran dapat berisi:

- deskripsi modul;
- cover depan;
- cover belakang;
- daftar isi;
- cuplikan halaman penting.

Jika diperlukan, modul lengkap dapat dilampirkan sebagai dokumen terpisah.

---

# 53. LAMPIRAN 9 — BUKTI PUBLIKASI

Lampiran terakhir memuat bukti luaran artikel ilmiah.

Dapat berupa:

- Letter of Acceptance;
- bukti submitted;
- halaman jurnal;
- DOI;
- URL artikel;
- screenshot halaman publikasi.

Status publikasi harus sesuai keadaan sebenarnya.

---

# 54. STRUKTUR MASTER LAPORAN

Struktur keseluruhan laporan:

```text
COVER
│
├── HALAMAN PENGESAHAN
├── HALAMAN KETERLIBATAN MAHASISWA
├── RINGKASAN
├── PRAKATA
├── DAFTAR ISI
└── DAFTAR LAMPIRAN

BAB I PENDAHULUAN
├── 1.1 Analisis Situasi Permasalahan
├── 1.2 Permasalahan Mitra
├── 1.3 Tujuan Pengabdian
├── 1.4 Manfaat Pengabdian
└── 1.5 Luaran Pengabdian

BAB II TINJAUAN PUSTAKA
├── 2.1 Pengertian/Teori Terkait Topik
└── 2.2 Tinjauan Pustaka Sesuai Topik Permasalahan

BAB III METODE PELAKSANAAN
├── 3.1 Tempat dan Waktu
├── 3.2 Khalayak Sasaran
├── 3.3 Metode Pengabdian
├── 3.4 Indikator Keberhasilan
└── 3.5 Metode Evaluasi

BAB IV HASIL DAN LUARAN YANG DICAPAI
├── 4.1 Hasil Kegiatan
├── 4.2 Analisis Keilmuan
├── 4.3 Pengukuran Dampak Kegiatan
└── 4.4 Luaran yang Dicapai

BAB V KESIMPULAN DAN REKOMENDASI
├── 5.1 Kesimpulan
└── 5.2 Rekomendasi

DAFTAR PUSTAKA

LAMPIRAN-LAMPIRAN
├── Lampiran 1 CV Tim dan Mahasiswa
├── Lampiran 2 Penggunaan Anggaran
├── Lampiran 3 Gambaran Iptek
├── Lampiran 4 Lokasi Mitra
├── Lampiran 5 Surat Kesediaan Mitra
├── Lampiran 6 Dokumentasi
├── Lampiran 7 Absensi
├── Lampiran 8 Modul Pelatihan
└── Lampiran 9 Bukti Publikasi/LoA
```

---

# 55. STRUKTUR DIREKTORI LATEX

Untuk menjaga laporan tetap modular, direkomendasikan menggunakan struktur:

```text
PKM_2026_LaTeX/
│
├── main.tex
├── references.bib
│
├── config/
│   └── ulbi-pkm.sty
│
├── frontmatter/
│   ├── cover.tex
│   ├── pengesahan.tex
│   ├── keterlibatan-mahasiswa.tex
│   ├── ringkasan.tex
│   └── prakata.tex
│
├── chapters/
│   ├── bab1.tex
│   ├── bab2.tex
│   ├── bab3.tex
│   ├── bab4.tex
│   └── bab5.tex
│
├── appendices/
│   ├── lampiran1-cv.tex
│   ├── lampiran2-anggaran.tex
│   ├── lampiran3-iptek.tex
│   ├── lampiran4-lokasi.tex
│   ├── lampiran5-surat-mitra.tex
│   ├── lampiran6-dokumentasi.tex
│   ├── lampiran7-absensi.tex
│   ├── lampiran8-modul.tex
│   └── lampiran9-publikasi.tex
│
└── assets/
    ├── logo/
    ├── figures/
    ├── documentation/
    ├── maps/
    └── scans/
```

---

# 56. FUNGSI FILE LATEX

## `main.tex`

Mengendalikan seluruh isi laporan.

## `ulbi-pkm.sty`

Menyimpan seluruh konfigurasi:

- margin;
- font;
- header;
- footer;
- format BAB;
- format subbab;
- caption;
- tabel;
- daftar pustaka;
- penomoran.

## `references.bib`

Menyimpan seluruh daftar pustaka.

## `frontmatter/`

Menyimpan bagian awal laporan.

## `chapters/`

Menyimpan BAB I sampai BAB V.

## `appendices/`

Menyimpan masing-masing lampiran.

## `assets/`

Menyimpan seluruh:

- logo;
- gambar;
- dokumentasi;
- peta;
- scan;
- PDF pendukung.

---

# 57. KOREKSI TERHADAP LAPORAN ACUAN

Beberapa inkonsistensi pada laporan tahun sebelumnya tidak perlu direplikasi dalam template baru.

## 57.1 Kesalahan Nama Subbab 1.5

Pada daftar isi laporan acuan terdapat:

```text
1.4 Manfaat Pengabdian
1.5 Manfaat Pengabdian
```

Namun isi 1.5 sebenarnya membahas luaran.

Template baru harus menggunakan:

```text
1.5 Luaran Pengabdian
```

---

## 57.2 Inkonsistensi Jumlah Pertemuan

Pada bagian Metode Pelaksanaan laporan acuan disebutkan kegiatan berlangsung dalam dua pertemuan.

Pada bagian Hasil Kegiatan disebutkan empat pertemuan.

Template laporan baru harus memastikan:

- tanggal;
- jumlah hari;
- jumlah pertemuan;
- durasi;

dituliskan secara konsisten pada seluruh bagian laporan.

---

## 57.3 Inkonsistensi Heading

Ukuran subjudul pada laporan lama tidak sepenuhnya seragam.

Template LaTeX harus menetapkan satu format global sehingga seluruh subbab menggunakan format yang konsisten.

---

## 57.4 Konsistensi Istilah Asing

Istilah asing harus ditulis secara konsisten.

Contoh:

```text
machine learning
deep learning
computer vision
pre-test
post-test
Project-Based Learning
```

Gunakan format italic sesuai kaidah penulisan ilmiah.

---

# 58. SPESIFIKASI FINAL TEMPLATE LATEX

Ringkasan spesifikasi:

| Komponen | Ketentuan |
|---|---|
| Ukuran kertas | A4 |
| Orientasi | Portrait |
| Margin kiri | 4 cm |
| Margin kanan | 3 cm |
| Margin atas | 4 cm |
| Margin bawah | 3 cm |
| Font | Times New Roman |
| Font isi | 12 pt |
| Spasi | 1,5 |
| Alignment | Justified |
| Indent paragraf | ±0,75 cm |
| Judul BAB | 16 pt Bold Uppercase Center |
| Subbab | 14 pt Bold |
| Sub-subbab | 12 pt Bold |
| Cover | Tanpa nomor halaman |
| Front Matter | Romawi kecil |
| BAB I dan seterusnya | Angka Arab |
| Posisi nomor halaman | Kanan bawah |
| Footer | 9 pt Italic |
| Sistem sitasi | Numerik |
| Gaya daftar pustaka | IEEE/Numeric |
| Caption gambar | Di bawah gambar |
| Istilah asing | Italic |
| BAB baru | Dimulai pada halaman baru |
| Struktur utama | 5 BAB |
| Bagian akhir | Daftar Pustaka + Lampiran |

---

# 59. PRINSIP PENYUSUNAN LAPORAN

Laporan akhir PkM harus memenuhi prinsip:

## Konsisten

Format, istilah, angka, tanggal, dan jumlah peserta harus sama pada seluruh bagian.

## Terukur

Keberhasilan kegiatan harus didukung indikator yang dapat dievaluasi.

## Berbasis Bukti

Setiap capaian didukung oleh:

- data;
- hasil evaluasi;
- dokumentasi;
- produk;
- dokumen luaran.

## Berorientasi Dampak

Laporan tidak hanya menjelaskan kegiatan yang dilakukan, tetapi menunjukkan perubahan yang terjadi setelah kegiatan.

## Berorientasi Mitra

Permasalahan, solusi, metode, dan hasil harus selalu dikaitkan dengan kebutuhan mitra.

## Akademik

Argumentasi harus didukung teori dan literatur yang relevan.

## Sistematis

Hubungan antarbagian harus mengikuti alur:

```text
Permasalahan
      ↓
Tujuan
      ↓
Solusi
      ↓
Metode
      ↓
Indikator Keberhasilan
      ↓
Pelaksanaan
      ↓
Evaluasi
      ↓
Hasil
      ↓
Dampak
      ↓
Luaran
      ↓
Kesimpulan
      ↓
Rekomendasi
```

---

# 60. KESIMPULAN PEDOMAN

Template LaTeX Laporan Akhir PkM 2026 harus mempertahankan struktur utama laporan PkM ULBI tahun sebelumnya, yaitu:

- bagian awal laporan;
- lima BAB utama;
- daftar pustaka;
- sembilan kelompok lampiran.

Penggunaan LaTeX diarahkan tidak hanya untuk mereplikasi tampilan laporan terdahulu, tetapi juga memperbaiki konsistensi format melalui pengaturan otomatis terhadap:

- margin;
- font;
- heading;
- penomoran;
- caption;
- tabel;
- gambar;
- sitasi;
- daftar pustaka;
- footer;
- nomor halaman; dan
- lampiran.

Dengan struktur modular, setiap BAB dan lampiran dapat dikembangkan secara terpisah tanpa mengganggu keseluruhan format dokumen.

---

## Checklist Template

Sebelum laporan dianggap selesai, lakukan pemeriksaan berikut:

- [ ] Ukuran kertas menggunakan A4.
- [ ] Margin mengikuti ketentuan.
- [ ] Seluruh isi menggunakan Times New Roman.
- [ ] Isi utama menggunakan ukuran 12 pt.
- [ ] Spasi menggunakan 1,5.
- [ ] Paragraf rata kiri-kanan.
- [ ] Format seluruh BAB konsisten.
- [ ] Format seluruh subbab konsisten.
- [ ] Cover tidak menampilkan nomor halaman.
- [ ] Bagian awal menggunakan angka Romawi.
- [ ] BAB I dimulai dari halaman 1.
- [ ] Nomor halaman berada di kanan bawah.
- [ ] Footer menggunakan identitas PkM ULBI Tahun 2026.
- [ ] Halaman pengesahan telah dimasukkan.
- [ ] Halaman keterlibatan mahasiswa telah tersedia.
- [ ] Ringkasan telah dilengkapi kata kunci.
- [ ] Prakata telah tersedia.
- [ ] Daftar isi dibuat otomatis.
- [ ] Daftar lampiran telah tersedia.
- [ ] BAB I terdiri dari Subbab 1.1–1.5.
- [ ] BAB II terdiri dari Subbab 2.1–2.2.
- [ ] BAB III terdiri dari Subbab 3.1–3.5.
- [ ] BAB IV terdiri dari Subbab 4.1–4.4.
- [ ] BAB V terdiri dari Subbab 5.1–5.2.
- [ ] Permasalahan mitra telah didukung hasil observasi.
- [ ] Tujuan berhubungan dengan permasalahan.
- [ ] Indikator keberhasilan bersifat terukur.
- [ ] Metode evaluasi telah dijelaskan.
- [ ] Data pre-test dan post-test dianalisis jika tersedia.
- [ ] Dampak kegiatan dijelaskan secara kuantitatif dan/atau kualitatif.
- [ ] Seluruh luaran diberikan status capaian.
- [ ] Kesimpulan menjawab tujuan kegiatan.
- [ ] Rekomendasi disusun berdasarkan hasil kegiatan.
- [ ] Sistem sitasi numerik digunakan secara konsisten.
- [ ] Seluruh referensi yang disitasi terdapat di daftar pustaka.
- [ ] Seluruh gambar memiliki caption.
- [ ] Gambar eksternal mencantumkan sumber.
- [ ] Dokumentasi kegiatan tersedia.
- [ ] Absensi tersedia.
- [ ] Penggunaan anggaran tersedia.
- [ ] Gambaran Iptek tersedia.
- [ ] Peta dan lokasi mitra tersedia.
- [ ] Surat kesediaan mitra tersedia.
- [ ] Modul pelatihan tersedia.
- [ ] Bukti publikasi/LoA tersedia apabila menjadi luaran.
- [ ] Tanggal, jumlah peserta, jumlah pertemuan, dan durasi kegiatan konsisten pada seluruh laporan.

---

**Dokumen Acuan:**  
Laporan Akhir Pengabdian kepada Masyarakat (PkM) Universitas Logistik dan Bisnis Internasional Tahun 2025.

**Tujuan Dokumen:**  
Spesifikasi format dan struktur untuk pengembangan template **LaTeX Laporan Akhir PkM ULBI Tahun 2026**.