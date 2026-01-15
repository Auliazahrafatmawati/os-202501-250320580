
# Laporan Praktikum Minggu [10]
Topik: Manajemen Memori - Page Replacement (FIFO & LRU)

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
```from collections import deque

def fifo_page_replacement(reference_string, frames):
    memory = deque()
    page_faults = 0

    print("=== FIFO Page Replacement ===")
    for page in reference_string:
        if page not in memory:
            page_faults += 1
            if len(memory) == frames:
                memory.popleft()
            memory.append(page)
            status = "FAULT"
        else:
            status = "HIT"
        print(f"Page: {page} | Memory: {list(memory)} | {status}")

    print(f"Total Page Fault (FIFO): {page_faults}\n")
    return page_faults


def lru_page_replacement(reference_string, frames):
    memory = []
    page_faults = 0

    print("=== LRU Page Replacement ===")
    for page in reference_string:
        if page not in memory:
            page_faults += 1
            if len(memory) == frames:
                memory.pop(0)
            memory.append(page)
            status = "FAULT"
        else:
            memory.remove(page)
            memory.append(page)
            status = "HIT"
        print(f"Page: {page} | Memory: {memory} | {status}")

    print(f"Total Page Fault (LRU): {page_faults}\n")
    return page_faults


if __name__ == "__main__":
    reference_string = [7, 0, 1, 2, 0, 3, 0, 4, 2, 3, 0, 3, 2]
    frames = 3

    fifo_faults = fifo_page_replacement(reference_string, frames)
    lru_faults = lru_page_replacement(reference_string, frames)

    print("=== Perbandingan ===")
    print(f"FIFO Page Faults: {fifo_faults}")
    print(f"LRU Page Faults : {lru_faults}")
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
1. Apa perbedaan utama FIFO dan LRU?
   **Jawaban**:
2. Mengapa FIFO dapat menghasilkan Belady’s Anomaly?
   **Jawaban**:
3. Mengapa LRU umumnya menghasilkan performa lebih baik dibanding FIFO?
   **Jawaban**:


---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
