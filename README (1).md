# Declarative Language
### Definisi
 Declarative language, di sisi lain, adalah paradigma pemrograman di mana fokus utama adalah pada apa yang ingin dicapai, bukan bagaimana cara mencapainya. Dalam bahasa ini, programmer mendefinisikan hasil akhir yang diinginkan, dan sistem menentukan cara terbaik untuk mencapainya.

### Karakteristik:
- **Ekspresi Hasil:** Alih-alih menentukan langkah-langkah eksplisit, programmer mendeskripsikan sifat-sifat atau kondisi akhir dari solusi.
- **Immutability:** Deklaratif cenderung mengurangi atau bahkan menghilangkan perubahan state, sehingga lebih mudah dipahami dan dikelola.
- **Contoh dalam DSL:** SQL adalah contoh klasik dari declarative language dalam DSL, di mana Anda cukup mendefinisikan data apa yang Anda inginkan, dan mesin basis data menentukan cara mengambilnya:
    ```
    SELECT name FROM users WHERE age > 30;
    ```
    Anda tidak perlu tahu bagaimana mesin akan mencari data tersebut; Anda hanya menyatakan hasil yang diinginkan.

### Keuntungan:
- **Sederhana dan Mudah Dibaca:** Karena tidak perlu menyatakan detail bagaimana hasil dicapai, kode declarative biasanya lebih sederhana dan lebih mudah dibaca.
- **Mengurangi Kesalahan:** Dengan mengurangi kebutuhan untuk mengelola state, kemungkinan terjadinya kesalahan menjadi lebih kecil.

### Kekurangan:
- **Kurang Kontrol:** Ketika kontrol penuh atau optimasi sangat dibutuhkan, declarative language bisa kurang memadai.
- **Performa Tersembunyi:** Karena pengembang tidak mengontrol cara sistem mencapai hasil, performa bisa tidak sesuai harapan dalam beberapa kasus.

--- 

Untuk memahami bagaimana "Declarative Language" dalam konteks "DSL (Domain Specific Language)" berkorelasi dengan bahasa pemrograman C/C++ yang digunakan pada Internet of Things (IoT) seperti Arduino, kita dapat melalui serangkaian langkah berikut:

### 1. Identifikasi Problem
Masalah yang perlu diidentifikasi adalah: "Bagaimana penerapan konsep Declarative Language dalam konteks DSL dapat membantu pengembangan aplikasi IoT yang menggunakan bahasa pemrograman C/C++ pada platform seperti Arduino?"

Dalam konteks ini, problem yang muncul adalah bagaimana konsep declarative, yang lebih umum diterapkan pada DSL, dapat diintegrasikan atau diadaptasi ke dalam bahasa imperatif seperti C/C++ yang digunakan di lingkungan IoT.

### 2. Deskripsi Problem
Declarative Language adalah paradigma pemrograman di mana programmer mendefinisikan apa yang harus dilakukan (tujuan akhir) daripada bagaimana melakukannya (proses). DSL adalah bahasa yang dirancang khusus untuk domain tertentu. Contoh dari DSL termasuk SQL untuk database, HTML untuk markup web, atau VHDL untuk desain hardware.

Sedangkan C/C++ merupakan bahasa pemrograman imperatif yang banyak digunakan untuk pengembangan perangkat lunak, terutama di bidang yang memerlukan kontrol hardware tingkat rendah seperti dalam IoT (misalnya, Arduino). Arduino menggunakan C/C++ untuk memprogram mikrokontroler yang mengendalikan perangkat keras.

Problemnya adalah bagaimana kita bisa mengadopsi pendekatan declarative dalam lingkungan yang secara tradisional menggunakan pendekatan imperatif, khususnya dalam pengembangan aplikasi IoT.

### 3. Metodologi Experiment
Untuk menguji korelasi ini, kita dapat melakukan beberapa langkah berikut:

**1. Pemahaman DSL di Arduino**: Teliti apakah ada DSL atau framework yang berbasis declarative yang sudah diterapkan dalam ekosistem Arduino.

**2. Implementasi Mini DSL**: Cobalah membuat mini DSL berbasis declarative yang dapat digunakan dalam proyek Arduino. DSL ini dapat difokuskan pada domain tertentu, misalnya, pengaturan sensor atau kontrol motor.

**3. Komparasi Kode**: Bandingkan bagaimana kode ditulis dalam DSL yang kamu buat dengan kode imperatif C/C++ tradisional di Arduino.

### 4. Pelaksanaan Experiment
**1. Penelitian DSL dalam Arduino**: Temukan contoh-contoh DSL yang mungkin sudah ada atau yang bisa diterapkan pada proyek Arduino, misalnya, domain yang spesifik seperti pengaturan pin atau komunikasi dengan sensor.

**2. Pengembangan DSL Sederhana**: Buat sebuah DSL sederhana menggunakan C++ yang memungkinkan pendekatan declarative untuk beberapa tugas spesifik dalam Arduino. Misalnya, DSL ini bisa digunakan untuk mendeklarasikan bagaimana sebuah sensor berinteraksi dengan mikrokontroler tanpa mendetailkan langkah-langkah imperatif.

**3. Pengujian**: Implementasikan dua contoh proyek Arduino yang serupa, satu menggunakan DSL dan yang lain menggunakan pendekatan C/C++ tradisional. 

### 5. Analisis Hasil Experiment
Bandingkan hasil eksperimen dari dua pendekatan tersebut:

**1. Kesederhanaan dan Readability**: Evaluasi apakah pendekatan declarative melalui DSL memudahkan pengembangan dan pemahaman kode dibandingkan dengan pendekatan imperatif tradisional.

**2. Efisiensi Waktu dan Kode**: Ukur apakah waktu pengembangan dan jumlah kode yang diperlukan lebih sedikit dalam DSL atau C/C++ tradisional.

**3. Kemampuan Ekspresi**: Tentukan apakah DSL dapat mencakup semua kasus yang dapat ditangani oleh C/C++ tradisional dalam konteks Arduino.

**4. Performa**: Evaluasi apakah ada pengaruh performa yang signifikan ketika menggunakan DSL dibandingkan dengan C/C++ tradisional.

Hasil dari eksperimen ini akan memberikan pemahaman yang lebih dalam mengenai bagaimana paradigma declarative dan DSL bisa diintegrasikan atau disesuaikan dalam pengembangan IoT menggunakan C/C++ pada platform seperti Arduino.

---

## Rangkaian Sederhana Menggunakan Declarative Language
**Proyek:** Mengontrol LED dengan Blok Perintah Tinkercad (Declarative Approach)

**Bahan:**
- 1 x Arduino Uno
- 1 x LED
- 1 x Resistor 220Ω
- Kabel Jumper

### Langkah-langkah:
**1. Menyusun Rangkaian:**

Rangkai LED dan resistor sama seperti pada proyek sebelumnya.

**2. Menggunakan Blok Perintah:**

- Buka bagian Code di Tinkercad dan pilih Blocks untuk menulis kode dalam bentuk blok perintah.
- Buat rangkaian blok berikut:
    - Tambahkan blok "set pin" dan atur pin 13 sebagai output.
    - Tambahkan blok "repeat forever" (ulangi selamanya).
    - Di dalam blok "repeat forever", tambahkan blok "set pin 13 high", "wait 1 second", "set pin 13 low", dan "wait 1 second".
- Jalankan simulasi.

**Penjelasan:** Dalam kasus ini, Anda menggunakan pendekatan declarative language yang lebih intuitif di mana Anda mendeklarasikan tindakan apa yang ingin dilakukan, tanpa perlu menulis kode langkah-demi-langkah secara eksplisit seperti dalam kode imperative.