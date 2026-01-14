
# Laporan Praktikum Minggu [4]
Topik: Manajemen Proses dan User di Linux

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
1. Apa fungsi dari proses init atau systemd dalam sistem Linux?  
   **Jawaban:** Dalam sistem Linux, init atau systemd berfungsi sebagai proses pertama (PID 1) yang dijalankan oleh kernel setelah booting. Proses ini bertanggung jawab menginisialisasi dan mengelola seluruh proses serta layanan sistem.  
2. Apa perbedaan antara kill dan killall? 
   **Jawaban:** Perbedaan antara kill dan killall di Linux terletak pada cara menargetkan proses yang akan dihentikan. kill: menghentikan proses berdasarkan PID (Process ID). killall menghentikan proses berdasarkan nama proses.  
3. Mengapa user root memiliki hak istimewa di sistem Linux? 
   **Jawaban:** User root memiliki hak istimewa di sistem Linux karena root adalah superuser, yaitu akun dengan kendali penuh atas sistem. Konsep ini dirancang secara sengaja untuk memungkinkan administrasi dan pengelolaan sistem secara menyeluruh. 

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
