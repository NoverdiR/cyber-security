# Reverse Engineering

*Reverse engineering* (RE) adalah proses atau metode dimana kita mencoba memahami secara deduktif bagaimana sebuah program bekerja.


# Table Of Contents

- [Reverse Engineering dalam CTF](#reverse-engineering-dalam-ctf)
- [Static Analysis](#static-analysis)
- [Yang Harus Dipahami](#yang-harus-dipahami)
- [Yang Harus Dipersiapkan](#yang-harus-dipersiapkan)
- [Tools Yang Dapat Digunakan](#tools-yang-dapat-digunakan)
- [Jenis File](#jenis-file)
    - [File C](#file-c)
    - [File ELF](#file-elf)
- [Control Flow](#control-flow)
- [Stripped vs Not-Stripped](#stripped-vs-not-stripped)
- [Langkah Umum](#langkah-umum)


## Reverse Engineering dalam CTF

Secara umum, dalam soal RE disediakan file program yang bisa dieksekusi. Tugas kita adalah memahami bagaimana dia bekerja, dan mencoba mencari "flag" berdasarkan cara kerja program tersebut.


## Static Analysis

Dalam static analysis, kita bisa menganalisis file secara langsung tanpa mengecek state dari proses ketika dijalankan.


## Yang Harus Dipahami

- Pemahaman Bahasa C
- Pemahaman Bahasa Python
- Pemahaman Dasar dari Assembly
- Penggunaan Terminal


## Yang Harus Dipersiapkan

- OS GNU/Linux
- Ghidra/IDA Pro
- Uncompyle6


## Tools Yang Dapat Digunakan

Tools ini umumnya sudah terpasang di sistem operasi GNU/Linux.

- *file*    : mengetahui jenis file
- *xxd*     : melihat hexdump dari file
- *strings* : melihat teks yang ada dalam file
- *readelf* : menampilkan informasi dari file ELF


## Jenis File

### File C

File C adalah file yang berisi *source code* dalam bahasa C.

### File ELF

ELF adalah jenis file yang umumnya berupa file executable atau library.


## Control Flow

Control flow adalah urutan pengerjaan instruksi dalam program.


## Stripped vs Not-Stripped

Ketika file di-*compile*, *compiler* akan memasukkan informasi *debugging*, diantaranya baris kode, nama variabel dan alamat memori pasangannya pada *runtime*.

- File *not-stripped* akan menyimpan informasi *debugging* tersebut.
- File *stripped* akan menghapus informasi tersebut.

Informasi mengenai *stripped*/*not-stripped* dapat dilihat menggunakan *file*.


## Langkah Umum

1. Download file dari soal
2. Pahami bagaimana file bekerja
3. Temukan flag. :D