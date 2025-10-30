
# Laporan Praktikum Minggu [1]
Topik: Arsitektur Sistem Operasi dan Kernel

---

## Identitas
- **Nama**  : Aulia Zahra Fatmawati  
- **NIM**   : 250320580  
- **Kelas** : 1DSRA

---

## Tujuan
Tuliskan tujuan praktikum minggu ini.  
> Mahasiswa mampu menjelaskan fungsi utama sistem operasi dan peran kernel serta system call.
> Mahasiswa mampu memahami konsep dasar arsitektur sistem operasi.
> Mahasiswa mampu mempelajari struktur dan desain sistem operasi.
> Mahasiswa mengimplementasikan konsep teoritis ke dalam praktek.
> Mengasah keterampilan pemrograman sistem.
---

## Dasar Teori
Tuliskan ringkasan teori (3–5 poin) yang mendasari percobaan.
1. Sistem operasi adalah perangkat lunak yang bertindak sebagai perantara antara pengguna dan perangkat keras komputer. Sistem operasi mengelola perangkat keras dan perangkat lunak komputer, serta menyediakan layanan bagi program aplikasi.
2. Arsitektur Sistem Operasi
Monolithic Kernel: Semua layanan OS berjalan di dalam satu kernel space. Contoh: Linux.
Microkernel: Layanan OS dipisah ke dalam modul-modul kecil. Hanya fitur dasar yang ada di kernel. Contoh: Minix.
Modular: Gabungan monolithic dan microkernel; modul bisa dimuat/dibongkar. Contoh: Linux modern.
Layered: Dibagi dalam lapisan-lapisan hierarki.
Virtual Machine Architecture: Menyediakan emulasi lengkap mesin fisik.
3. Kernel adalah komponen inti dari sistem operasi yang bertugas langsung mengelola sumber daya perangkat keras (seperti CPU, memori, dan perangkat I/O) serta mengatur interaksi antara perangkat keras dengan perangkat lunak (program aplikasi).

---

## Langkah Praktikum
1. Langkah-langkah yang dilakukan.  
2. Perintah yang dijalankan.  
3. File dan kode yang dibuat.  
4. Commit message yang digunakan.

---

## Kode / Perintah
Tuliskan potongan kode atau perintah utama:
```bash
uname -a
lsmod | head
dmesg | head
```

---

## Hasil Eksekusi
Sertakan screenshot hasil percobaan atau diagram:
![Screenshot hasil](screenshots/example.png)

---

## Analisis
- Jelaskan makna hasil percobaan.
 Memperdalam pemahaman teori arsitektur sistem operasi dengan praktik nyata, melihat langsung bagaimana berbagai komponen sistem operasi berinteraksi dan bekerja,mengamati perilaku sistem operasi saat mengelola sumber daya komputer,mengidentifikasi kelebihan dan keterbatasan suatu pendekatan arsitektur OS.
- Hubungkan hasil dengan teori (fungsi kernel, system call, arsitektur OS).  
- Apa perbedaan hasil di lingkungan OS berbeda (Linux vs Windows)?  

---

## Kesimpulan
Tuliskan 2–3 poin kesimpulan dari praktikum ini.

---
## Tugas
Kernel monolitik adalah jenis arsitektur sistem operasi di mana seluruh sistem operasi, termasuk fungsi-fungsi inti seperti manajemen memori, manajemen proses, driver perangkat, dan sistem berkas, terintegrasi ke dalam satu blok kode besar yang berjalan dalam satu ruang alamat. Desain ini dapat mempercepat sistem karena semua komponen dapat berinteraksi secara langsung, tetapi juga dapat membuat sistem lebih kompleks dan lebih sulit dipelihara, karena bug di satu bagian kernel berpotensi memengaruhi seluruh sistem.
Mikrokernel adalah pendekatan minimalis untuk merancang sistem operasi. Dalam arsitektur mikrokernel, hanya fungsi-fungsi terpenting yang disertakan dalam kernel, seperti komunikasi dasar antara perangkat keras dan perangkat lunak, serta manajemen proses yang sederhana. Layanan lain seperti driver perangkat, sistem berkas, dan protokol jaringan dijalankan di ruang pengguna sebagai proses terpisah.
monolithic kernel menyatukan semua layanan (manajemen memori, proses, driver) dalam satu ruang kernel besar, menjadikannya cepat tetapi rentan terhadap kegagalan; microkernel hanya menyertakan fungsionalitas dasar di dalam kernel, memindahkan layanan lain ke ruang pengguna untuk meningkatkan keamanan dan stabilitas; sedangkan layered architecture membagi OS menjadi beberapa lapisan (layer), di mana setiap lapisan memiliki tugas spesifik dan berinteraksi dengan lapisan di atas dan di bawahnya untuk menjalankan fungsi. 
Monolitik Kernel
Konsep: Seluruh fungsi sistem operasi (manajemen memori, manajemen proses, driver perangkat, dan lain lain.) berjalan dalam satu program besar di ruang kernel. 
Kelebihan:
Kinerja tinggi karena semua komponen berada dalam ruang alamat yang sama dan tidak memerlukan komunikasi antar-proses yang rumit. 
Kekurangan:
Ukuran besar: Sulit untuk diperluas dan dipelihara. 
Keamanan rendah: Satu kegagalan dalam satu komponen dapat menyebabkan seluruh sistem crash (misalnya, Blue Screen of Death di Windows). 
Contoh: Linux, Unix, dan Windows. 
2. Mikrokernel
Konsep: Hanya fungsi-fungsi paling dasar yang ditempatkan di dalam kernel (misalnya, penanganan memori dan thread dasar), sementara layanan lain (seperti manajemen file dan driver) dipindahkan ke ruang pengguna sebagai server terpisah. 
Kelebihan:
Keamanan dan stabilitas tinggi: Jika satu server gagal, sistem inti tidak terpengaruh, membuat sistem lebih andal. 
Modularitas tinggi: Mudah untuk menambah atau menghapus layanan tanpa mengkompilasi ulang seluruh kernel. 
Kekurangan:
Kinerja lebih lambat: Komunikasi antar server di ruang pengguna dan antara ruang pengguna serta kernel membutuhkan lebih banyak overhead. 
3. Arsitektur Berlapis (Layered Architecture)
Konsep: Sistem operasi dibagi menjadi beberapa lapisan yang diatur secara hierarkis, di mana setiap lapisan hanya dapat berkomunikasi dengan lapisan di bawah dan di atasnya.
Kelebihan:
Modularitas: Pemisahan tugas yang jelas.
Toleransi kesalahan yang lebih baik: Kesalahan di satu lapisan tidak akan merusak lapisan lain secara langsung.
Lebih mudah dirancang dan diuji: Setiap lapisan dapat dikembangkan dan diuji secara terpisah.
Kekurangan:
Kompleks: Bisa lebih kompleks daripada model monolitik.
Overhead kinerja: Komunikasi antar lapisan dapat menciptakan overhead yang lebih besar dibandingkan dengan monolitik.
monolithic kernel mengintegrasikan semua layanan OS dalam satu ruang kernel untuk kinerja tinggi, tetapi rentan terhadap kegagalan (contoh: Linux, Windows). Microkernel meminimalkan layanan dalam kernel agar lebih stabil dan aman, tetapi kinerjanya lebih lambat karena komunikasi antarproses lebih kompleks (contoh: Minix, QNX). Layered architecture membagi OS menjadi lapisan-lapisan vertikal yang terpisah, dengan setiap lapisan yang memiliki tugas spesifik, membuatnya lebih modular dan toleran terhadap kesalahan dibandingkan sistem monolitik.
## Quiz
1. Sebutkan tiga fungsi utama sistem operasi.
   **Jawaban:** Tiga fungsi utama sistem operasi adalah Manajemen Sumber Daya, Manajemen Proses dan File, serta Penyediaan Antarmuka Pengguna.
2. Jelaskan perbedaan antara kernel mode dan user mode.
   **Jawaban:** Dalam mode kernel, CPU memiliki akses tak terbatas ke sumber daya sistem dan dapat menjalankan instruksi istimewa. Sementara itu, dalam mode pengguna, akses dibatasi dan operasi tertentu dilarang untuk memastikan stabilitas dan keamanan sistem. 
3. Sebutkan contoh OS dengan arsitektur monolithic dan microkernel.
   **Jawaban:** Contoh sistem operasi dengan arsitektur monolitik adalah Linux dan varian Unix seperti FreeBSD, sementara contoh sistem operasi dengan arsitektur mikrokernel adalah QNX, L4Linux, dan Symbian. 

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
