---
layout: page
title: About Nginx
permalink: /about/nginx/
---

### Nginx - (baca: engine x)

adalah server [HTTP](http://id.wikipedia.org/wiki/HTTP) dan [Proxy](http://id.wikipedia.org/wiki/Proxy) dengan kode sumber terbuka yang bisa juga berfungsi sebagai proxy IMAP/POP3. Kode sumber nginx ditulis oleh seorang warga negara [Rusia](http://id.wikipedia.org/wiki/Rusia) yang bernama [Igor Sysoev](http://sysoev.ru/en/) pada tahun 2002 dan dirilis ke publik pada tahun 2004. Nginx terkenal karena stabil, memiliki tingkat performansi tinggi dan sedikit mengonsumsi sumber daya.
Untuk waktu yang lama, telah berjalan pada banyak berat dimuat situs Rusia termasuk [Yandex](http://www.yandex.ru/), [Mail.Ru](http://mail.ru/), [VK](http://vk.com/), dan [Rambler](http://www.rambler.ru/). Menurut Netcraft, nginx dilayani atau proksi [20.41% situs tersibuk di November 2014](http://news.netcraft.com/archives/2014/11/19/november-2014-web-server-survey.html).

Beberapa situs terkenal yang menggunakan Nginx adalah [Netflix](https://www.netflix.com/), [Wordpress](http://wordpress.org/), [Fastmail](https://www.fastmail.fm/), [Ohloh](https://code.ohloh.net/), [Sourceforge](http://sourceforge.net/), [Github](https://github.com), dan lain-lain.

Sumber dan dokumentasi yang didistribusikan di bawah [2-clause BSD-like license](/LICENSE.md).

Dukungan komersial tersedia dari [Nginx, Inc](http://nginx.com/?_ga=1.100477017.632127369.1411524321).

#### Fitur server HTTP dasar
   * Melayani statis dan indeks file, autoindexing , buka file descriptor Cache;
   * Accelerated proxy terbalik dengan caching , load balancing sederhana dan toleransi kesalahan;
   * Dukungan dipercepat dengan caching FastCGI , uwsgi , SCGI , dan memcached server, load balancing sederhana dan toleransi kesalahan;
   * Arsitektur modular. Filter termasuk gzipping , rentang byte, chunked tanggapan, XSLT , SSI , dan transformasi image filter. Beberapa inklusi SSI dalam satu halaman dapat diproses secara paralel jika mereka ditangani oleh server proxy atau FastCGI / uwsgi / SCGI;
   * SSL dan dukungan TLS SNI .

#### Fitur server HTTP lainnya
   * Nama-based dan berbasis IP server virtual;
   * Jaga-hidup dan pipelined koneksi dukungan;
   * Konfigurasi yang fleksibel;
   * Rekonfigurasi dan upgrade dieksekusi tanpa gangguan dari melayani klien;
   * Format akses log , buffered menulis log , rotasi log cepat , dan penebangan syslog;
   * 3xx-5xx kode kesalahan pengalihan;
   * Modul rewrite: URI berubah menggunakan ekspresi reguler;
   * Pelaksana fungsi yang berbeda tergantung pada alamat klien;
   * Pengendalian akses berdasarkan alamat IP client , dengan password (HTTP Basic otentikasi) dan oleh hasil subrequest;
   * Validasi HTTP referal;
   * The PUT, DELETE, MKCOL, COPY, dan MOVE metode;
   * FLV dan MP4 Streaming;
   * Tingkat respons membatasi;
   * Membatasi jumlah simultan koneksi atau permintaan yang datang dari satu alamat;
   * Tertanam Perl .

#### Mail fitur server proxy
   * Pengalihan pengguna untuk IMAP atau POP3 server menggunakan HTTP eksternal otentikasi Server;
   * Otentikasi pengguna menggunakan HTTP eksternal otentikasi server dan koneksi pengalihan ke internal SMTP server yang;
   * Metode otentikasi:
      - POP3 : PENGGUNA / LULUS, APOP, AUTH LOGIN / PLAIN / CRAM-MD5;
      - IMAP : LOGIN, AUTH LOGIN / PLAIN / CRAM-MD5;
      - SMTP : AUTH LOGIN / PLAIN / CRAM-MD5;
   * SSL dukungan;
   * STARTTLS dan STLS dukungan.

#### Arsitektur dan skalabilitas
   * Satu master dan beberapa proses pekerja; proses pekerja berjalan di bawah user biasa;
   * Dukungan untuk kqueue (FreeBSD 4.1+), epoll (Linux 2.6+), sinyal rt (Linux 2.2.19+), / dev / polling (Solaris 7 11/99 +), acara port (Solaris 10), pilih, dan jajak pendapat;
   * Dukungan dari berbagai fitur kqueue termasuk EV_CLEAR, EV_DISABLE (untuk menonaktifkan sementara peristiwa), NOTE_LOWAT, EV_EOF, jumlah data yang tersedia, kode kesalahan;
   * sendfile (FreeBSD 3.1 +, Linux 2.2 +, Mac OS X 10,5 +), sendfile64 (Linux 2.4.21+), dan sendfilev (Solaris 8 1/7 +) dukungan;
   * File AIO (FreeBSD 4.3+, Linux 2.6.22+);
   * DIRECTIO (FreeBSD 4.4+, Linux 2.4+, Solaris 2.6+, Mac OS X);
   * Terima-filter (FreeBSD 4.1+, NetBSD 5.0+) dan TCP_DEFER_ACCEPT (Linux 2.4+) dukungan;
   * 10.000 HTTP aktif tetap-hidup koneksi memakan waktu sekitar 2,5 juta memori;
   * Data menyalin operasi disimpan ke minimum.

#### Diuji OS dan platform
   * FreeBSD 3 - 10 / i386; FreeBSD 5 - 10 / amd64;
   * Linux 2,2-3 / i386; Linux 2,6-3 / amd64; Linux 3 / armv6l, armv7l, aarch64;
   * Solaris 9 / i386, sun4u; Solaris 10 / i386, amd64, sun4v;
   * AIX 7.1 / powerpc;
   * HP-UX 11.31 / ia64;
   * Mac OS X / ppc, i386;
   * Windows XP, Windows Server 2003. 