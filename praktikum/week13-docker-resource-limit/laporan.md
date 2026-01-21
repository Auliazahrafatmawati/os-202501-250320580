
# Laporan Praktikum Minggu [13]
Topik: Docker – Resource Limit (CPU & Memori)

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
1. Mengapa container perlu dibatasi CPU dan memori?
   **Jawaban**: Container perlu dibatasi CPU dan memori agar satu container tidak menggunakan sumber daya secara berlebihan dan mengganggu container lain atau sistem host. Pembatasan ini membantu menjaga stabilitas sistem, memastikan keadilan penggunaan resource, serta memudahkan perencanaan kapasitas dan performa aplikasi.
2. Apa perbedaan VM dan container dalam konteks isolasi resource?
   **Jawaban**: Virtual Machine (VM) melakukan isolasi resource dengan menjalankan sistem operasi lengkap (guest OS) di atas hypervisor, sehingga isolasinya lebih kuat namun membutuhkan resource lebih besar.
Container melakukan isolasi pada level sistem operasi (kernel yang sama), sehingga lebih ringan dan cepat, tetapi tingkat isolasinya lebih rendah dibanding VM.
3. Apa dampak limit memori terhadap aplikasi yang boros memori?
   **Jawaban**: Jika aplikasi yang boros memori diberi limit memori, aplikasi tersebut dapat mengalami penurunan performa, error, atau dihentikan secara paksa (misalnya terkena OOM Killer). Hal ini memaksa aplikasi untuk lebih efisien dalam penggunaan memori, tetapi jika limit terlalu kecil, aplikasi bisa sering crash.

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
