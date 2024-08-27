
- **Topik:** Type System dalam IoT
- **Content:** Pengolahan Program Bahasa Pemrograman
- **PIC:** Satria Permata Sejati
- **Kelompok:** 1 | Type | Praktek
- **Tautan Referensi:** [Type System - ChatGPT](https://chatgpt.com/share/d3a7f66d-554e-4944-aee0-b00be8b90a14)

---

### 1. Identifikasi Problem
Bagaimana peran "type system" dalam pengembangan perangkat Internet of Things (IoT) dan apa saja aspek yang perlu dikritisi dalam penerapannya?

### 2. Deskripsi Problem
Dalam pengembangan IoT, penggunaan berbagai jenis sensor, aktuator, dan perangkat komunikasi yang berbeda sering kali melibatkan berbagai tipe data. Type system adalah mekanisme yang digunakan oleh bahasa pemrograman untuk mengklasifikasikan dan mengatur tipe data ini. Masalah yang muncul adalah bagaimana type system dapat digunakan untuk menjamin keandalan, keamanan, dan efisiensi dalam pengembangan aplikasi IoT, serta apa saja keterbatasan yang ada dalam penerapan type system ini.

Hal yang harus dikritisi meliputi:

Keamanan: Apakah type system yang digunakan mampu mencegah kesalahan tipe yang dapat menyebabkan kegagalan sistem?
Efisiensi: Seberapa baik type system ini mendukung optimasi performa pada perangkat dengan sumber daya terbatas?
Keterbacaan dan Pemeliharaan: Apakah penggunaan type system mempermudah atau malah memperumit pengembangan dan pemeliharaan kode?
Interoperabilitas: Bagaimana type system menangani interoperabilitas antara perangkat yang mungkin menggunakan bahasa pemrograman yang berbeda?

### 3. Metodologi Eksperimen
Eksperimen ini akan menggunakan simulasi IoT sederhana dengan Arduino di Tinkercad. Kita akan membuat sebuah sistem monitoring suhu dan kelembapan dengan menggunakan sensor DHT11. Dalam eksperimen ini, kita akan mencoba mengidentifikasi dan menangani potensi kesalahan tipe data dalam proses pengambilan data dan pengiriman informasi melalui komunikasi serial.

Langkah-langkah metodologi:

Desain Sistem: Merancang sistem monitoring suhu dan kelembapan menggunakan Arduino dan sensor DHT11.
Implementasi Kode: Menulis kode yang menggunakan type system C++ untuk membaca data dari sensor, memprosesnya, dan mengirimkannya melalui komunikasi serial.
Pengujian: Menguji kode untuk melihat bagaimana type system menangani tipe data dan kemungkinan kesalahan yang muncul.
Analisis: Menganalisis hasil pengujian untuk menentukan keandalan dan efisiensi type system dalam konteks ini.

### 4. Pelaksanaan Eksperimen
Desain Sistem:

Buatlah rangkaian dengan Arduino UNO, sensor DHT11, dan beberapa LED sebagai indikator.
Sensor DHT11 akan terhubung ke pin digital Arduino untuk membaca suhu dan kelembapan.
Implementasi Kode:

cpp
Copy code
#include "DHT.h"

#define DHTPIN 2     // Pin yang digunakan untuk sensor
#define DHTTYPE DHT11   // Jenis sensor

DHT dht(DHTPIN, DHTTYPE);

void setup() {
  Serial.begin(9600);
  dht.begin();
}

void loop() {
  float h = dht.readHumidity();    // Membaca kelembapan
  float t = dht.readTemperature(); // Membaca suhu

  // Mengirim data melalui serial
  Serial.print("Kelembapan: ");
  Serial.print(h);
  Serial.print(" %\t");
  Serial.print("Suhu: ");
  Serial.print(t);
  Serial.println(" *C");

  // Menunda pembacaan berikutnya
  delay(2000);
}

### Pengujian:

Jalankan simulasi dan lihat bagaimana data dari sensor ditangani dan ditampilkan.
Cobalah untuk memaksa kesalahan tipe data, misalnya dengan menggunakan tipe data yang salah atau mencoba melakukan operasi yang tidak sesuai.
Analisis:

Analisis apakah kesalahan tipe data ditangani dengan baik oleh type system C++.
Evaluasi bagaimana penggunaan type system dapat mencegah bug atau crash pada aplikasi IoT.
Identifikasi apakah type system membantu dalam menjaga keandalan dan efisiensi sistem, terutama pada perangkat dengan sumber daya terbatas.
5. Analisis Hasil Eksperimen
Setelah eksperimen dilakukan, berikut adalah beberapa poin penting yang dapat diambil:

Keandalan: Type system dalam C++ terbukti mampu mencegah beberapa kesalahan tipe yang umum, seperti pengiriman tipe data yang tidak sesuai melalui komunikasi serial.
Efisiensi: Meskipun type system dapat membantu dalam pengoptimalan, efisiensi masih tergantung pada desain keseluruhan dan bagaimana kode ditulis.
Keterbacaan: Dengan type system yang kuat, kode menjadi lebih mudah dipahami dan dimodifikasi karena setiap tipe data memiliki makna yang jelas.
Interoperabilitas: Dalam konteks IoT, interoperabilitas antar perangkat yang menggunakan bahasa yang berbeda bisa menjadi tantangan, terutama jika type system tidak seragam.
Melalui eksperimen ini, Anda dapat lebih memahami bagaimana type system berperan dalam pengembangan aplikasi IoT, serta bagaimana hal tersebut dapat mempengaruhi keandalan dan efisiensi sistem secara keseluruhan.

---

© T1 - PBP - TIF423
