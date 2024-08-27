
- **Topik:** Optimization
- **Content:** Domain-Spesific Language
- **PIC:** Zaki Abdillah
- **Kelompok:** 1 | Prinsip Bahasa Pemrograman | Praktek
- **Tautan Referensi:** [Optimization - ChatGPT](https://chatgpt.com/share/b35f7c81-a6c8-4202-a55e-54673b353b29)

---

Berikut adalah contoh eksperimen mengenai optimisasi penggunaan energi pada sistem IoT dengan Arduino di Tinkercad:

### Judul Eksperimen:  
**Optimisasi Konsumsi Energi pada Sistem IoT dengan Sleep Mode pada Arduino**

### 1. Identifikasi Problem
Pada perangkat IoT yang beroperasi dengan sumber daya terbatas seperti baterai, konsumsi energi yang tinggi dapat mengurangi umur operasional perangkat. Oleh karena itu, diperlukan metode untuk mengoptimalkan konsumsi energi agar perangkat dapat beroperasi lebih lama tanpa sering membutuhkan penggantian baterai.

### 2. Deskripsi Problem
Arduino sebagai salah satu perangkat dalam sistem IoT dapat diatur untuk memasuki mode tidur (sleep mode) saat tidak sedang digunakan. Mode ini mengurangi konsumsi energi dengan mematikan beberapa fungsi perangkat keras yang tidak diperlukan. Eksperimen ini akan mengeksplorasi bagaimana penerapan sleep mode pada Arduino dapat mengurangi konsumsi energi dan memperpanjang masa operasional perangkat.

### 3. Metodologi Experiment
Eksperimen akan melibatkan dua skenario utama:
- **Skenario 1**: Arduino beroperasi secara terus-menerus tanpa sleep mode.
- **Skenario 2**: Arduino beroperasi dengan sleep mode yang diaktifkan setelah interval tertentu tanpa aktivitas.

Langkah-langkah eksperimen meliputi:
1. Menghubungkan sensor ke Arduino untuk mendeteksi aktivitas.
2. Mengatur Arduino untuk melakukan tugas sederhana (misalnya, mengedipkan LED) setiap kali sensor mendeteksi aktivitas.
3. Mengukur konsumsi daya pada kedua skenario.
4. Mencatat durasi operasional perangkat pada kedua skenario.

### 4. Pelaksanaan Experiment
1. **Rangkaian Elektronik**:
   - Arduino Uno.
   - Sensor PIR (Passive Infrared) untuk mendeteksi gerakan.
   - LED untuk indikasi aktivitas.
   - Resistor 220 ohm.

2. **Koding**:
   - Program Arduino untuk skenario 1 (tanpa sleep mode).
   - Program Arduino untuk skenario 2 (dengan sleep mode menggunakan library **LowPower.h**).

3. **Pelaksanaan**:
   - Bangun rangkaian di Tinkercad.
   - Jalankan skenario 1: Arduino terus aktif, LED berkedip saat sensor PIR mendeteksi gerakan.
   - Jalankan skenario 2: Arduino masuk ke mode tidur ketika tidak ada aktivitas dan bangun hanya ketika sensor PIR mendeteksi gerakan.
   - Pantau dan catat konsumsi daya serta durasi operasional untuk kedua skenario menggunakan fitur **monitor daya** di Tinkercad.

### 5. Analisis Hasil Experiment
Bandingkan hasil dari kedua skenario:
- **Konsumsi Daya**: Analisis seberapa besar energi yang dikonsumsi pada kedua skenario. Apakah sleep mode secara signifikan mengurangi konsumsi energi?
- **Durasi Operasional**: Evaluasi apakah penggunaan sleep mode memperpanjang masa operasional Arduino secara signifikan.
- **Efisiensi**: Hitung perbedaan persentase dalam konsumsi energi antara kedua skenario dan simpulkan efektivitas sleep mode dalam optimisasi energi.

Hasil eksperimen ini diharapkan menunjukkan bahwa penerapan sleep mode pada Arduino dapat secara signifikan mengurangi konsumsi energi dan memperpanjang masa pakai perangkat dalam sistem IoT.

---

© T1 - PBP - TIF423
