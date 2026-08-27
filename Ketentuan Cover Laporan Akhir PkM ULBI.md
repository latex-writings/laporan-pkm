# KETENTUAN COVER LAPORAN AKHIR PENGABDIAN KEPADA MASYARAKAT (PkM)

## 1. Fungsi Cover

Cover merupakan halaman pertama Laporan Akhir Pengabdian kepada Masyarakat (PkM) dan menjadi identitas utama dokumen.

Cover harus menampilkan secara jelas:

- jenis dokumen;
- jenis kegiatan;
- judul kegiatan;
- objek atau studi kasus;
- identitas tim pengabdi;
- identitas program studi;
- identitas universitas; dan
- tahun pelaksanaan/laporan.

Cover **tidak menampilkan nomor halaman**.

---

# 2. Ukuran Halaman Cover

Cover mengikuti ukuran dokumen utama:

- Kertas: **A4**
- Orientasi: **Portrait**
- Ukuran: **210 mm × 297 mm**

Margin cover mengikuti margin laporan:

| Posisi | Margin |
|---|---:|
| Kiri | 4 cm |
| Kanan | 3 cm |
| Atas | 4 cm |
| Bawah | 3 cm |

---

# 3. Font Cover

Font utama:

**Times New Roman**

Berdasarkan tampilan laporan acuan, hierarki ukuran yang direkomendasikan untuk template LaTeX adalah:

| Elemen | Ukuran | Format |
|---|---:|---|
| LAPORAN AKHIR | 14–16 pt | Bold, Uppercase |
| PENGABDIAN KEPADA MASYARAKAT (PKM) | 14–16 pt | Bold, Uppercase |
| Judul kegiatan | 14–16 pt | Bold, Uppercase |
| Studi Kasus | 12 pt | Regular/Bold sesuai kebutuhan |
| “Oleh:” | 12 pt | Bold |
| Nama tim | 12 pt | Regular/Bold |
| NIDN/NIK | 12 pt | Regular |
| Program Studi | 14 pt | Bold, Uppercase |
| Nama Universitas | 14 pt | Bold, Uppercase |
| Tahun | 14 pt | Bold |

Ukuran tersebut dijadikan standar template agar tampilan konsisten.

---

# 4. Perataan Cover

Mayoritas elemen cover menggunakan:

**Center alignment**

Elemen berikut ditempatkan di tengah halaman:

- `LAPORAN AKHIR`;
- `PENGABDIAN KEPADA MASYARAKAT (PKM)`;
- judul kegiatan;
- keterangan studi kasus;
- tulisan `Oleh:`;
- identitas tim;
- nama program studi;
- nama universitas;
- tahun laporan.

---

# 5. Susunan Cover

Urutan elemen cover harus mengikuti struktur berikut:

```text
LAPORAN AKHIR

PENGABDIAN KEPADA MASYARAKAT (PKM)


JUDUL KEGIATAN PENGABDIAN KEPADA MASYARAKAT
DITULIS DALAM HURUF KAPITAL DAN DAPAT
TERDIRI DARI BEBERAPA BARIS


(Studi Kasus: Nama Mitra / Lokasi / Objek Kegiatan)


[AREA IDENTITAS / LOGO APABILA DIPERSYARATKAN]


Oleh:

Nama Ketua Tim, Gelar                           NIDN
Nama Anggota 1, Gelar                           NIDN
Nama Anggota 2, Gelar                           NIDN


NAMA PROGRAM STUDI

UNIVERSITAS LOGISTIK DAN BISNIS INTERNASIONAL

TAHUN 2026
```

---

# 6. Bagian “LAPORAN AKHIR”

Teks:

```text
LAPORAN AKHIR
```

Ketentuan:

- ditulis menggunakan huruf kapital;
- bold;
- posisi center;
- ditempatkan pada bagian paling atas cover;
- tidak menggunakan tanda titik;
- tidak diberi nomor BAB atau nomor halaman.

---

# 7. Bagian Jenis Kegiatan

Di bawah `LAPORAN AKHIR` ditulis:

```text
PENGABDIAN KEPADA MASYARAKAT (PKM)
```

Ketentuan:

- uppercase;
- bold;
- center;
- menggunakan istilah **PkM/PkM** secara konsisten pada isi laporan;
- pada cover mengikuti bentuk kapital sebagaimana laporan acuan:

```text
PENGABDIAN KEPADA MASYARAKAT (PKM)
```

---

# 8. Judul Kegiatan

Judul kegiatan merupakan elemen paling dominan pada cover.

Ketentuan:

- menggunakan huruf kapital;
- bold;
- center;
- dapat terdiri dari beberapa baris;
- tidak menggunakan tanda titik di akhir;
- harus identik dengan judul pada halaman pengesahan;
- harus identik dengan judul pada dokumen administratif PkM;
- harus menggunakan ejaan dan kapitalisasi yang konsisten.

Contoh struktur:

```text
PENINGKATAN KOMPETENSI ...
MELALUI ...
BAGI ...
```

Apabila judul panjang, pemenggalan baris harus berdasarkan kelompok makna, bukan secara acak.

---

# 9. Subjudul / Studi Kasus

Setelah judul dapat ditambahkan keterangan:

```text
(Studi Kasus: ...)
```

Contoh format laporan acuan:

```text
(Studi Kasus: SMKN 2 Cimahi - Jurusan Rekayasa Perangkat Lunak)
```

Ketentuan:

- menggunakan tanda kurung;
- posisi center;
- ukuran lebih kecil daripada judul utama;
- menggunakan kapitalisasi normal;
- tidak harus seluruhnya uppercase;
- tidak menggunakan titik di bagian akhir.

Jika kegiatan tidak memerlukan studi kasus, bagian ini dapat disesuaikan dengan ketentuan administrasi PkM yang berlaku.

---

# 10. Logo Universitas

Apabila template resmi PkM tahun berjalan mensyaratkan logo ULBI, logo ditempatkan:

- di tengah;
- setelah judul/studi kasus;
- sebelum tulisan `Oleh:`;
- ukuran proporsional;
- tidak mengalami distorsi;
- menggunakan file dengan resolusi tinggi.

Contoh LaTeX:

```latex
\includegraphics[
    width=0.22\textwidth
]{assets/logo/logo-ulbi.png}
```

**Catatan:** penggunaan logo pada cover harus mengikuti dokumen/template resmi ULBI tahun berjalan. Jangan menambahkan atau menghilangkan logo apabila ketentuan resmi menyatakan lain.

---

# 11. Bagian “Oleh:”

Sebelum nama tim dicantumkan:

```text
Oleh:
```

Ketentuan:

- center;
- menggunakan huruf awal kapital;
- diikuti tanda titik dua;
- diletakkan setelah judul/logo;
- diberi jarak vertikal yang cukup dengan identitas tim.

---

# 12. Identitas Ketua Tim

Identitas ketua harus mencantumkan:

- nama lengkap;
- gelar akademik;
- NIDN/NIK/identitas yang dipersyaratkan.

Format:

```text
Nama Lengkap Ketua, Gelar                          NIDN
```

Nama dan gelar harus sesuai dengan data resmi institusi.

---

# 13. Identitas Anggota Tim

Setiap dosen anggota dicantumkan pada baris tersendiri.

Format:

```text
Nama Ketua, Gelar                                  NIDN
Nama Anggota 1, Gelar                              NIDN
Nama Anggota 2, Gelar                              NIDN
```

Ketentuan:

- urutan dimulai dari ketua;
- kemudian anggota;
- nama tidak disingkat kecuali gelar;
- NIDN/NIK menggunakan nomor resmi;
- format gelar harus konsisten;
- identitas harus sama dengan halaman pengesahan.

---

# 14. Mahasiswa pada Cover

Pada laporan acuan 2025, mahasiswa yang terlibat tidak dicantumkan pada cover utama, tetapi ditempatkan pada **Halaman Keterlibatan Mahasiswa**.

Dengan demikian, template dasar mengikuti ketentuan:

> **Cover memuat tim dosen/pengabdi utama, sedangkan mahasiswa dicantumkan pada Halaman Keterlibatan Mahasiswa.**

Jika terdapat ketentuan resmi tahun berjalan yang meminta mahasiswa dicantumkan pada cover, aturan resmi terbaru harus diprioritaskan.

---

# 15. Program Studi

Setelah identitas tim dituliskan nama program studi.

Format:

```text
SARJANA TERAPAN TEKNIK INFORMATIKA
```

atau sesuai program studi ketua pengusul.

Ketentuan:

- uppercase;
- bold;
- center;
- nama program studi ditulis lengkap;
- tidak menggunakan singkatan jika tidak diperlukan.

---

# 16. Nama Institusi

Nama institusi ditulis:

```text
UNIVERSITAS LOGISTIK DAN BISNIS INTERNASIONAL
```

Ketentuan:

- uppercase;
- bold;
- center;
- ditulis lengkap;
- ditempatkan setelah nama program studi.

---

# 17. Tahun

Bagian terakhir cover adalah tahun laporan.

Contoh:

```text
TAHUN 2026
```

Ketentuan:

- uppercase;
- bold;
- center;
- berada pada bagian bawah cover;
- menggunakan tahun pelaksanaan/laporan sesuai ketentuan program.

---

# 18. Nomor Halaman Cover

Cover:

**tidak menampilkan nomor halaman.**

Dalam LaTeX:

```latex
\thispagestyle{empty}
```

Setelah cover:

```latex
\clearpage
```

Penomoran Romawi dimulai pada bagian awal laporan berikutnya.

---

# 19. Konsistensi Judul

Judul kegiatan pada cover harus sama persis dengan judul pada:

- halaman pengesahan;
- surat mitra;
- dokumen kontrak;
- laporan kegiatan;
- poster;
- artikel ilmiah apabila relevan;
- modul apabila menggunakan judul kegiatan;
- dokumen luaran lainnya.

Perbedaan kata, tanda baca, atau urutan judul harus dihindari.

---

# 20. Konsistensi Nama dan Gelar

Nama tim harus menggunakan penulisan yang sama pada:

- cover;
- halaman pengesahan;
- halaman keterlibatan mahasiswa;
- CV;
- artikel;
- dokumen administrasi;
- surat mitra.

Perhatikan konsistensi:

- nama;
- titik pada gelar;
- tanda koma;
- spasi;
- NIDN;
- urutan anggota.

---

# 21. Jarak Vertikal Cover

Cover tidak boleh terlihat terlalu padat atau terlalu kosong.

Secara visual, pembagian halaman dapat menggunakan pola:

```text
BAGIAN ATAS
Laporan Akhir
Jenis Kegiatan

        ↓

BAGIAN TENGAH ATAS
Judul
Studi Kasus

        ↓

BAGIAN TENGAH
Logo / Area Identitas Institusi

        ↓

BAGIAN TENGAH BAWAH
Oleh:
Tim Pengabdi

        ↓

BAGIAN BAWAH
Program Studi
Universitas
Tahun
```

Gunakan `\vspace{}` secara terkontrol dan hindari penggunaan banyak baris kosong manual.

---

# 22. Larangan pada Cover

Cover tidak boleh:

- menampilkan nomor halaman;
- menggunakan header;
- menggunakan footer laporan;
- menampilkan nomor BAB;
- menggunakan daftar isi;
- memiliki caption;
- memiliki sitasi;
- menggunakan dekorasi yang tidak diperlukan;
- menggunakan warna atau font yang berbeda tanpa ketentuan resmi;
- menggunakan logo beresolusi rendah;
- mengubah rasio logo;
- menggunakan judul yang berbeda dari halaman pengesahan.

---

# 23. Footer pada Cover

Footer standar:

```text
Pengabdian Kepada Masyarakat Universitas Logistik dan Bisnis Internasional Tahun 2026
```

**tidak ditampilkan pada halaman cover.**

Footer baru digunakan mulai halaman berikutnya sesuai template laporan.

---

# 24. Template Konseptual LaTeX Cover

Contoh struktur implementasi:

```latex
\begin{titlepage}
    \thispagestyle{empty}

    \begin{center}

        {\fontsize{16}{19}\selectfont\bfseries
        LAPORAN AKHIR\par}

        \vspace{0.4cm}

        {\fontsize{16}{19}\selectfont\bfseries
        PENGABDIAN KEPADA MASYARAKAT (PKM)\par}

        \vspace{1.5cm}

        {\fontsize{15}{18}\selectfont\bfseries
        JUDUL KEGIATAN PENGABDIAN KEPADA MASYARAKAT\\
        DITULIS DALAM HURUF KAPITAL DAN DAPAT\\
        TERDIRI DARI BEBERAPA BARIS\par}

        \vspace{0.5cm}

        {\fontsize{12}{15}\selectfont
        (Studi Kasus: Nama Mitra)\par}

        \vspace{1.2cm}

        % Logo digunakan apabila dipersyaratkan
        \includegraphics[
            width=0.20\textwidth
        ]{assets/logo/logo-ulbi.png}

        \vspace{1.2cm}

        {\fontsize{12}{15}\selectfont\bfseries
        Oleh:\par}

        \vspace{0.4cm}

        {\fontsize{12}{15}\selectfont
        Nama Ketua, Gelar \qquad NIDN\\
        Nama Anggota 1, Gelar \qquad NIDN\\
        Nama Anggota 2, Gelar \qquad NIDN\par}

        \vfill

        {\fontsize{14}{17}\selectfont\bfseries
        NAMA PROGRAM STUDI\par}

        \vspace{0.3cm}

        {\fontsize{14}{17}\selectfont\bfseries
        UNIVERSITAS LOGISTIK DAN BISNIS INTERNASIONAL\par}

        \vspace{0.3cm}

        {\fontsize{14}{17}\selectfont\bfseries
        TAHUN 2026\par}

    \end{center}
\end{titlepage}
```

---

# 25. Struktur Cover Final

Template final cover menggunakan struktur:

```text
┌──────────────────────────────────────────────────┐

                    LAPORAN AKHIR

          PENGABDIAN KEPADA MASYARAKAT
                       (PKM)


            JUDUL KEGIATAN PENGABDIAN
                KEPADA MASYARAKAT
                 DITULIS DI SINI

               (Studi Kasus: Mitra)


                       [LOGO]


                        Oleh:

            Nama Ketua, Gelar       NIDN
            Nama Anggota, Gelar     NIDN
            Nama Anggota, Gelar     NIDN




                 PROGRAM STUDI

       UNIVERSITAS LOGISTIK DAN BISNIS
                 INTERNASIONAL

                    TAHUN 2026

└──────────────────────────────────────────────────┘
```

---

# 26. Checklist Cover

Sebelum laporan dikompilasi final, pastikan:

- [ ] Cover menggunakan ukuran A4.
- [ ] Orientasi portrait.
- [ ] Font menggunakan Times New Roman.
- [ ] Terdapat tulisan `LAPORAN AKHIR`.
- [ ] Terdapat tulisan `PENGABDIAN KEPADA MASYARAKAT (PKM)`.
- [ ] Judul kegiatan ditulis lengkap.
- [ ] Judul menggunakan huruf kapital.
- [ ] Judul sama dengan halaman pengesahan.
- [ ] Studi kasus/mitra dituliskan jika diperlukan.
- [ ] Logo ULBI digunakan jika dipersyaratkan.
- [ ] Logo menggunakan kualitas tinggi.
- [ ] Logo tidak mengalami distorsi.
- [ ] Terdapat tulisan `Oleh:`.
- [ ] Nama ketua dicantumkan.
- [ ] Gelar ketua benar.
- [ ] NIDN/NIK ketua benar.
- [ ] Nama seluruh anggota dicantumkan.
- [ ] Gelar anggota benar.
- [ ] NIDN/NIK anggota benar.
- [ ] Urutan tim sama dengan halaman pengesahan.
- [ ] Nama program studi ditulis lengkap.
- [ ] Nama universitas ditulis lengkap.
- [ ] Tahun laporan benar.
- [ ] Semua elemen utama menggunakan alignment center.
- [ ] Jarak antarbagian proporsional.
- [ ] Cover tidak menggunakan nomor halaman.
- [ ] Cover tidak menggunakan header.
- [ ] Cover tidak menggunakan footer laporan.
- [ ] Cover tidak memiliki sitasi.
- [ ] Cover tidak menggunakan dekorasi yang tidak diperlukan.

---

# 27. Posisi Cover dalam Struktur Laporan

Struktur awal laporan menjadi:

```text
COVER
│
│   • Tanpa nomor halaman
│   • Tanpa header
│   • Tanpa footer
│
├── HALAMAN PENGESAHAN ......................... i
│
├── HALAMAN KETERLIBATAN MAHASISWA ............ ii
│
├── RINGKASAN .................................. iii
│
├── PRAKATA .................................... iv
│
├── DAFTAR ISI ................................. v
│
└── DAFTAR LAMPIRAN ............................ ...
```

Setelah bagian awal selesai:

```text
BAB I PENDAHULUAN .............................. 1
```

dimulai menggunakan nomor halaman Arab.

---

## Ketentuan Utama

**Cover laporan PkM harus menjadi halaman identitas resmi yang sederhana, formal, konsisten dengan halaman pengesahan, dan mengikuti hierarki informasi laporan PkM ULBI. Cover tidak memiliki nomor halaman, header, maupun footer.**