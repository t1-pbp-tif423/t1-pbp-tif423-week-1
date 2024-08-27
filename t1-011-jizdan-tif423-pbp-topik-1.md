- Topik: Syntax & Semantics
- PIC: Jizdan Mulkan Nailan
- Kelompok: 1 | Prinsip Bahasa Pemrograman | Praktek
---


## 1. Identifikasi Problem
Masalah: Bagaimana perbedaan sintaks dan semantik memengaruhi perilaku perangkat IoT. Terutama, eksperimen ini bertujuan untuk mengeksplorasi bagaimana penulisan kode yang berbeda (sintaks) dapat menghasilkan hasil yang berbeda (semantik) dalam konteks pengendalian perangkat keras, seperti LED atau sensor, menggunakan platform simulasi Tinkercad.

Pertanyaan Utama:
1. Bagaimana perubahan dalam sintaks (penulisan kode) mempengaruhi semantik (tindakan yang dilakukan perangkat)?
2. Bagaimana memastikan bahwa perintah yang diberikan dalam kode diterjemahkan dengan benar oleh perangkat IoT?

## 2. Deskripsi Problem
Deskripsi: Perangkat IoT (Internet of Things) memerlukan instruksi yang tepat untuk melakukan tugas-tugas tertentu. Dalam konteks ini, memahami perbedaan antara sintaks dan semantik sangat penting. Sintaks mengacu pada aturan penulisan kode, sedangkan semantik berkaitan dengan arti atau perilaku yang dihasilkan oleh kode tersebut.

Eksperimen ini akan menggunakan platform Tinkercad untuk membuat rangkaian elektronik sederhana dan menulis kode yang mengontrol perangkat IoT (seperti LED) untuk menguji hubungan antara sintaks dan semantik.

## 3. Metodologi Experiment
Metodologi eksperimen ini melibatkan langkah-langkah berikut:

1. Pemilihan Platform dan Alat: Menggunakan Tinkercad sebagai platform simulasi untuk membangun rangkaian elektronik dan menulis kode Arduino.

2. Desain Rangkaian: Merancang rangkaian elektronik sederhana yang melibatkan Arduino Uno, LED, resistor, dan breadboard.

3. Penulisan Kode (Sintaks): Mengembangkan beberapa versi kode Arduino untuk mengontrol LED, yang masing-masing memiliki sintaks berbeda namun ditujukan untuk menghasilkan semantik yang sama atau berbeda.

4. Pengujian dan Simulasi: Menjalankan simulasi di Tinkercad untuk mengamati perilaku LED berdasarkan kode yang ditulis.

5. Analisis Hasil: Mengevaluasi bagaimana perbedaan sintaks mempengaruhi hasil semantik dan perilaku perangkat IoT.

## 4. Pelaksanaan Experiment
--- Penyusunan Rangkaian: ---

Buat proyek baru di Tinkercad dan tambahkan komponen berikut ke workspace: 
1. Arduino Uno
2. LED
3. Resistor (220 ohm)
4. Breadboard
   
Hubungkan LED dan resistor ke breadboard. Sambungkan salah satu kaki resistor ke pin digital Arduino (misalnya, pin 13), dan kaki lainnya ke GND Arduino.

--- Penulisan Kode (Sintaks): ---

Berikut adalah kode untuk menghidupkan dan mematikan lampu LED dalam interval 1 detik:

```cpp
int ledPin = 13;

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  digitalWrite(ledPin, HIGH);
  delay(1000);
  digitalWrite(ledPin, LOW);
  delay(1000);
}
```

--- Modifikasi Kode untuk Pengujian Semantik: ---

Misalnya, kita akan mengubah frekuensi kedipan LED:

```cpp
void loop() {
  digitalWrite(ledPin, HIGH);
  delay(500);  // LED menyala selama 0.5 detik
  digitalWrite(ledPin, LOW);
  delay(1500); // LED mati selama 1.5 detik
}
```

--- Simulasi: ---

Klik "Start Simulation" di Tinkercad untuk menjalankan setiap versi kode dan mengamati bagaimana LED berperilaku sesuai dengan perubahan sintaks yang diterapkan.

--- Pengumpulan Data: ---

Catat hasil dari setiap simulasi, termasuk apakah LED berfungsi sesuai yang diharapkan dan bagaimana perubahan sintaks memengaruhi semantik (tindakan LED).

## 5. Analisis Hasil Experiment
Dalam analisis ini, kami mengevaluasi hasil dari setiap simulasi yang dilakukan:

--- Hasil Eksperimen Sintaks Pertama (Kode Dasar): ---

Pengamatan: LED menyala dan mati dengan interval 1 detik, sesuai dengan semantik kode.
Analisis: Sintaks yang digunakan sudah sesuai dengan semantik yang diinginkan, yaitu LED berkedip setiap 1 detik.

--- Hasil Eksperimen Sintaks Kedua (Kode dengan Interval Berbeda): ---

Pengamatan: LED menyala selama 0.5 detik dan mati selama 1.5 detik.
Analisis: Modifikasi sintaks menghasilkan perubahan dalam semantik, menunjukkan bahwa perubahan kecil dalam penulisan kode (sintaks) dapat mempengaruhi cara perangkat beroperasi (semantik).

--- Kesimpulan Umum: ---

Eksperimen menunjukkan bahwa sintaks yang benar penting untuk mencapai semantik yang diinginkan dalam pengendalian perangkat IoT. Kesalahan atau perubahan dalam sintaks dapat mengubah semantik dan perilaku perangkat. Penting untuk memastikan bahwa penulisan kode dilakukan dengan teliti untuk menghindari hasil yang tidak diinginkan, terutama dalam aplikasi IoT yang sensitif.
