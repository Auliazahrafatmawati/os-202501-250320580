
# Laporan Praktikum Minggu [12]
Topik: Virtualisasi Menggunakan Virtual Machine

---

## Identitas
- **Nama**  : Aulia Zahra Fatmawati 
- **NIM**   : 250320580 
- **Kelas** : 1DSRA

---

## Tujuan
Tuliskan tujuan praktikum minggu ini.  
Contoh:  
> Mahasiswa mampu menjelaskan fungsi utama sistem operasi dan peran kernel serta system call.

---

## Dasar Teori
Tuliskan ringkasan teori (3–5 poin) yang mendasari percobaan.

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
- Hubungkan hasil dengan teori (fungsi kernel, system call, arsitektur OS).  
- Apa perbedaan hasil di lingkungan OS berbeda (Linux vs Windows)?  

---

## Kesimpulan
Tuliskan 2–3 poin kesimpulan dari praktikum ini.

---

## Quiz
1. Apa perbedaan antara host OS dan guest OS?
   **Jawaban**: Host OS adalah sistem operasi utama yang terpasang langsung pada perangkat keras (hardware) dan mengelola sumber daya fisik seperti CPU, memori, dan storage.
Guest OS adalah sistem operasi yang berjalan di dalam mesin virtual (virtual machine) di atas host OS, menggunakan sumber daya yang dialokasikan secara virtual, bukan langsung dari hardware.
2. Apa peran hypervisor dalam virtualisasi?
   **Jawaban**: Hypervisor berperan sebagai lapisan pengelola yang memungkinkan beberapa mesin virtual berjalan pada satu perangkat keras fisik. Hypervisor bertugas membagi, mengatur, dan mengisolasi sumber daya hardware (CPU, RAM, disk) agar setiap guest OS dapat berjalan secara independen dan stabil.
3. Mengapa virtualisasi meningkatkan keamanan sistem?
   **Jawaban**: Virtualisasi meningkatkan keamanan karena setiap sistem berjalan dalam lingkungan yang terisolasi. Jika satu guest OS terkena serangan atau mengalami kegagalan, dampaknya tidak langsung memengaruhi host OS atau mesin virtual lainnya. Selain itu, virtualisasi memudahkan pengujian, pemulihan (snapshot), dan pembatasan akses sehingga risiko kerusakan sistem dapat dikurangi.

   
---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
