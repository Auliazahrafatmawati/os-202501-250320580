
# Laporan Praktikum Minggu [2]
Topik: System Call Structures

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
## Tugas
System call penting untuk keamanan OS karena menjadi gateway yang terstruktur antara aplikasi dan kernel, mencegah akses langsung yang tidak sah ke sumber daya sensitif seperti memori dan perangkat keras, serta menegakkan kontrol akses yang memvalidasi izin sebelum operasi dieksekusi. Melalui system call, sistem operasi mengontrol dan mengisolasi setiap program, memastikan satu program tidak dapat mengganggu program lain atau merusak sistem. Sistem operasi (OS) memastikan transisi yang aman antara mode pengguna (user mode) dan mode kernel (kernel mode) melalui kombinasi dukungan perangkat keras (hardware) dan mekanisme perangkat lunak (software). Mekanisme utamanya adalah operasi mode ganda (dual-mode operation) dan penggunaan panggilan sistem (system calls).
Cara OS memastikan keamanan transisi tersebut:
1. Operasi Mode Ganda (Dual-Mode Operation)
Ini adalah fondasi keamanan transisi, di mana CPU beroperasi dalam salah satu dari dua mode:
Mode Pengguna (User Mode): Ini adalah mode terbatas di mana sebagian besar aplikasi berjalan. Dalam mode ini, akses ke sumber daya perangkat keras dan instruksi CPU tertentu dibatasi. Kesalahan atau crash dalam mode pengguna tidak akan membahayakan stabilitas seluruh sistem.
Mode Kernel (Kernel Mode/Privileged Mode): Ini adalah mode istimewa di mana kernel OS berjalan. Kernel memiliki akses penuh ke semua sumber daya perangkat keras (memori, CPU, perangkat I/O) dan dapat menjalankan semua instruksi CPU. 
Perangkat keras (CPU) memiliki register khusus yang menentukan mode operasi saat ini.
2. Panggilan Sistem (System Calls)
Transisi dari mode pengguna ke mode kernel hanya dapat terjadi melalui mekanisme yang terkontrol dan terdefinisi, yang disebut panggilan sistem. Ini berfungsi sebagai "gerbang" yang aman: 
Inisiasi: Program di mode pengguna yang membutuhkan layanan kernel (misalnya, mengakses file, manajemen memori) tidak dapat melakukannya secara langsung. Ia harus membuat permintaan panggilan sistem.
Interupsi Perangkat Lunak: Panggilan sistem memicu interupsi perangkat lunak (software interrupt) yang secara otomatis mengubah mode CPU dari mode pengguna ke mode kernel. Ini adalah satu-satunya cara yang sah untuk beralih ke mode kernel.
Penanganan Kernel: Kode kernel kemudian mengambil kendali, memvalidasi permintaan dari program pengguna, dan menjalankan operasi yang diminta. Kernel memeriksa parameter yang diteruskan untuk memastikan keamanannya.
Pengembalian: Setelah operasi selesai, kernel mengembalikan kontrol ke program pengguna dan mengubah mode CPU kembali ke mode pengguna. 
3. Isolasi Memori
Setiap proses berjalan di ruang alamat memorinya sendiri (user space), yang terisolasi dari ruang memori kernel (kernel space). Unit Manajemen Memori (MMU) perangkat keras menerapkan isolasi ini, mencegah program pengguna mengakses atau memodifikasi memori kernel secara langsung. 
4. Pengerasan Kernel (Kernel Hardening)
Selain mekanisme dasar, OS modern juga menerapkan teknik tambahan:
Address Space Layout Randomization (ASLR): Mengacak lokasi memori kernel untuk menyulitkan serangan yang mengandalkan pengetahuan tentang tata letak memori tertentu.
Mandatory Access Control (MAC): Kebijakan kontrol akses granular yang membatasi hak istimewa bahkan dalam mode kernel untuk mencegah eskalasi hak istimewa yang tidak sah, seperti SELinux pada Linux.
Hardware Stack Protection: Beberapa perangkat keras menyediakan perlindungan tumpukan untuk menegakkan integritas alur kontrol kernel dan mencegah eksploitasi buffer overflow. 
Melalui mekanisme berlapis ini, OS memastikan bahwa meskipun program pengguna mengalami kerusakan, kernel tetap terlindungi dan stabilitas seluruh sistem terjaga.
Contoh system call yang sering digunakan di Linux adalah open, read, write, close (untuk manajemen file), fork, exec, exit (untuk manajemen proses), dan kill (untuk mengirim sinyal ke proses). Panggilan sistem ini menyediakan antarmuka antara program dan kernel sistem operasi, memungkinkan program untuk meminta layanan seperti interaksi file, pembuatan proses baru, atau mengakhiri eksekusi. 

## Kesimpulan
Tuliskan 2–3 poin kesimpulan dari praktikum ini.

---

## Quiz
1. Apa fungsi utama system call dalam sistem operasi?
   **Jawaban:** Fungsi utama system call adalah sebagai jembatan antara aplikasi pengguna dan kernel sistem operasi untuk mengakses sumber daya perangkat keras dan layanan sistem lainnya.
2. Sebutkan 4 kategori system call yang umum digunakan.
   **Jawaban:**  Empat kategori system call yang umum digunakan adalah manajemen proses, manajemen berkas, manajemen perangkat I/O, dan komunikasi.
3. Mengapa system call tidak bisa dipanggil langsung oleh user program. 
   **Jawaban:**  System call tidak dapat dipanggil langsung oleh program pengguna karena beberapa alasan mendasar terkait keamanan, stabilitas, dan manajemen sumber daya sistem operasi.

---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
