
# Laporan Praktikum Minggu [11]
Topik: Simulasi dan Deteksi Deadlock

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
1. Apa perbedaan antara deadlock prevention, avoidance, dan detection?
   **Jawaban**: Prevention: Mencegah salah satu kondisi deadlock terjadi, Avoidance: Menghindari deadlock dengan analisis kondisi aman, Detection: Mengizinkan deadlock terjadi lalu mendeteksinya.
   
3. Mengapa deteksi deadlock tetap diperlukan dalam sistem operasi?
   **Jawaban**: Karena pencegahan dan penghindaran deadlock dapat menurunkan efisiensi sistem.
   
3.Apa kelebihan dan kekurangan pendekatan deteksi deadlock?
   **Jawaban**: Kelebihan: Fleksibilitas tinggi, Utilisasi resource lebih baik, Tidak perlu info kebutuhan maksimum proses, Cocok untuk sistem dinamis. Kekurangan: Deadlock sudah terjadi sebelum ditangani, Overhead komputasi untuk deteksi, Risiko kehilangan data / rollback mahal.
 

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
