# PORTOFOLIO INDIVIDU

## Identitas

- **Nama:** Muhammad Agung Budi Laksono
- **NIM:** 2510512181
- **Program Studi:** S1 Sistem Informasi
- **Mata Kuliah:** Sistem Operasi
- **Kelompok:** 5A
- **Proyek:** Pengembangan Sistem Otomasi Backup dan Pemulihan Data pada Linux Menggunakan Shell Script

## Deskripsi Proyek

Proyek ini merupakan pengembangan sistem otomasi backup dan pemulihan data pada sistem operasi Linux menggunakan Shell Script. Sistem dirancang untuk membantu proses pencadangan data, menjaga keamanan arsip, memeriksa integritas file, serta mendukung pemulihan data ketika diperlukan.

Pengembangan dilakukan pada lingkungan Ubuntu Server menggunakan mesin virtual VirtualBox. Pengelolaan kode dan dokumentasi proyek dilakukan melalui Git dan GitHub secara berkelompok.

## Kontribusi dan Tanggung Jawab

Dalam proyek ini, saya bertanggung jawab sebagai Anggota 2 dengan tugas utama pembuatan arsip backup, pengaturan hak akses arsip, dan pengujian akses terhadap file backup.

Kontribusi yang saya kerjakan meliputi:

1. Mengembangkan script `scripts/backup.sh` untuk membuat arsip dari direktori sumber menggunakan utilitas GNU Tar dan Gzip.
2. Menerapkan penamaan arsip berdasarkan timestamp dan process ID agar hasil backup dapat dibedakan.
3. Memeriksa keberadaan dan validitas arsip setelah proses pembuatan menggunakan perintah `tar`.
4. Menerapkan pembatasan hak akses arsip menggunakan `umask 077` dan `chmod 600`.
5. Melaksanakan pengujian pembuatan arsip serta pengujian akses menggunakan akun pengguna yang berbeda.
6. Mendokumentasikan hasil implementasi dan pengujian sebagai evidence proyek.

## Implementasi Teknis

Beberapa perintah dan konsep Linux yang digunakan dalam pekerjaan ini antara lain:

- `tar -czf`: membuat arsip terkompresi dengan format `.tar.gz`.
- `tar -tzf`: memeriksa dan menampilkan isi arsip.
- `chmod 600`: membatasi hak akses file agar hanya pemilik yang dapat membaca dan menulis.
- `umask 077`: membatasi permission awal file yang dibuat oleh proses.
- `stat`: memeriksa permission serta pemilik arsip.
- `mktemp`: menguji kemampuan tulis pada direktori tujuan.
- Exit status: mengetahui apakah proses backup berhasil atau mengalami kegagalan.

## Hasil Pengujian

Pengujian dilakukan melalui empat skenario utama berikut:

| ID | Skenario | Hasil |
|---|---|---|
| T04 | Pembuatan arsip backup pada direktori yang dapat ditulis | Berhasil, exit status 0 |
| T05 | Pembuatan backup pada direktori yang tidak dapat ditulis | Ditolak, exit status 6 |
| T17 | Pemilik arsip membaca isi arsip | Berhasil, exit status 0 |
| T18 | Pengguna lain mencoba membaca arsip | Ditolak dengan Permission denied, exit status 2 |

Pengujian tersebut menunjukkan bahwa script dapat membuat arsip backup, mendeteksi kondisi tujuan yang tidak dapat ditulis, serta menerapkan pembatasan akses terhadap arsip berdasarkan permission Linux.

## File dan Dokumentasi Kontribusi

File yang berkaitan dengan pekerjaan saya pada repository kelompok:

- `scripts/backup.sh`
- `docs/analisis-anggota2.md`
- `tests/anggota2-uji-arsip.md`
- `evidence/07-ubuntu-server-demo/02-backup/`
- `evidence/07-ubuntu-server-demo/05-access-control/`

## Pengetahuan dan Pengalaman yang Diperoleh

Melalui proyek ini, saya memperoleh pengalaman dalam menggunakan Linux Server, menjalankan perintah Bash, membuat arsip backup, mengelola permission file, serta melakukan pengujian pada kondisi positif dan negatif.

Saya juga mempelajari penerapan konsep sistem operasi, khususnya sistem berkas, proses input/output, mekanisme hak akses, serta penanganan kesalahan menggunakan exit status.

Selain kemampuan teknis, proyek ini memberikan pengalaman bekerja secara kolaboratif menggunakan Git dan GitHub untuk mengelola kode program, dokumentasi, dan bukti pengerjaan.

## Penutup

Kontribusi pada proyek ini memberikan pemahaman mengenai penerapan otomasi backup dan pengelolaan keamanan file pada lingkungan Linux. Hasil pengerjaan menjadi salah satu bentuk dokumentasi pengalaman dan kemampuan yang diperoleh selama mengikuti praktikum dan proyek mata kuliah Sistem Operasi.
