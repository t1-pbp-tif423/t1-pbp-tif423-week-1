- Topik: Sensor Interface & Actuator Control
- PIC: Farras Ahmad Rasyid
- Kelompok: 1 | Prinsip Bahasa Pemrograman | Praktek
---
## 1. Definisi
Sensor Interface:

Definisi: Sensor interface adalah mekanisme atau cara perangkat IoT berinteraksi dengan sensor untuk mengumpulkan data dari lingkungan fisik. Sensor ini bisa mendeteksi berbagai parameter seperti suhu, kelembaban, cahaya, gerakan, dll. Data yang dihasilkan oleh sensor ini kemudian dikirimkan ke microcontroller atau mikroprosesor untuk diolah lebih lanjut.
Contoh: Misalnya, sebuah sensor suhu (thermistor atau sensor DHT11) mengukur suhu ruangan dan mengirimkan data ini ke microcontroller seperti Arduino.

Actuator Control:

Definisi: Actuator control adalah proses di mana perangkat IoT mengontrol aktuator untuk melakukan tindakan fisik di dunia nyata berdasarkan data yang diterima atau kondisi yang terdeteksi. Aktuator bisa berupa motor, relay, LED, speaker, dll., yang berfungsi untuk mengubah energi listrik menjadi gerakan, cahaya, atau bentuk energi lainnya.
Contoh: Sebuah motor servo yang digerakkan untuk membuka atau menutup pintu berdasarkan perintah dari microcontroller.


## 1. Identifikasi Problem
Masalah: Di lingkungan IoT, sering kali diperlukan pengambilan keputusan otomatis berdasarkan kondisi lingkungan yang terukur oleh sensor. Misalnya, bagaimana cara mengaktifkan kipas angin secara otomatis jika suhu ruangan mencapai batas tertentu?

Pertanyaan Utama:

Bagaimana menghubungkan dan mengintegrasikan sensor suhu dengan sistem IoT?
Bagaimana mengendalikan aktuator (misalnya, kipas atau LED) berdasarkan data yang diterima dari sensor tersebut?
## 2. Deskripsi Problem
Deskripsi: Dalam skenario ini, kita ingin membuat sistem otomatisasi suhu ruangan. Sensor suhu akan mengukur suhu ruangan, dan ketika suhu mencapai ambang batas tertentu (misalnya 30°C), aktuator (seperti kipas atau LED) akan diaktifkan secara otomatis.

Objektif:

Membuat sistem IoT sederhana yang dapat membaca data dari sensor suhu dan menggunakan data tersebut untuk mengontrol aktuator.
Mempelajari cara kerja interface sensor dengan mikrokontroler dan cara mengontrol aktuator berdasarkan input dari sensor.
## 3. Metodologi Experiment
Langkah-langkah:

Pemilihan Sensor dan Aktuator:

Pilih sensor suhu yang sesuai (misalnya, LM35 atau DHT11).
Pilih aktuator yang sesuai, seperti LED untuk visualisasi atau motor untuk kontrol fisik.
Rancangan Sistem:

Buat rangkaian elektronika yang menghubungkan sensor dengan mikrokontroler (Arduino).
Hubungkan aktuator ke mikrokontroler sehingga dapat dikendalikan oleh data yang diterima dari sensor.
Pengembangan Perangkat Lunak:

Tulis kode Arduino untuk membaca data dari sensor suhu.
Implementasikan logika untuk mengaktifkan aktuator ketika suhu mencapai ambang batas.
## 4. Pelaksanaan Experiment
Langkah 1: Rangkaian Elektronik:

Komponen:

Sensor suhu (DHT11)
Arduino Uno
LED sebagai aktuator
Resistor (220 ohm)
Breadboard dan kabel penghubung
Proses Perakitan:

Hubungkan pin data sensor suhu ke pin A0 Arduino.
Hubungkan LED ke pin 13 Arduino melalui resistor 220 ohm.
Hubungkan semua komponen ke sumber daya (5V) dan ground pada Arduino.

Langkah 2: Pemrograman:

Kode Arduino:
```c++
int sensorPin = A0; // Pin untuk sensor suhu
int ledPin = 13;    // Pin untuk LED
int threshold = 30; // Ambang suhu dalam derajat Celsius

void setup() {
  pinMode(ledPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  int sensorValue = analogRead(sensorPin);
  float voltage = sensorValue * (5.0 / 1023.0);
  float temperatureC = (voltage - 0.5) * 100.0;
  Serial.println(temperatureC);

  if (temperatureC > threshold) {
    digitalWrite(ledPin, HIGH); // Nyalakan LED
  } else {
    digitalWrite(ledPin, LOW);  // Matikan LED
  }

  delay(1000); // Delay 1 detik
}
```
Langkah 3: Pengujian Sistem:

Jalankan program dan amati perubahan suhu yang terdeteksi oleh sensor.
Amati apakah LED menyala ketika suhu melebihi ambang batas yang telah ditentukan.
## 5. Analisis Hasil Experiment
Observasi:

Ketika suhu yang terdeteksi oleh sensor melebihi 30°C, LED akan menyala, menunjukkan bahwa sistem IoT berhasil mengontrol aktuator berdasarkan input sensor.
Jika suhu di bawah ambang batas, LED tetap mati.
Analisis:

Hasil ini menunjukkan bahwa sensor interface bekerja dengan baik dalam mengirimkan data ke mikrokontroler.
Aktuator control juga berhasil mengaktifkan LED sebagai respons terhadap data yang diterima dari sensor, menunjukkan keberhasilan sistem IoT dalam pengambilan keputusan otomatis.
Kesimpulan:

Rangkaian yang dibuat berhasil mengimplementasikan Sensor Interface dan Actuator Control dalam skenario sederhana IoT.
Sistem ini dapat dikembangkan lebih lanjut dengan menggunakan aktuator lain seperti motor atau relay untuk aplikasi yang lebih kompleks.
Saran Pengembangan:

Integrasikan sistem ini dengan platform IoT seperti Blynk untuk pemantauan dan kontrol jarak jauh.
Coba gunakan sensor dan aktuator yang lebih kompleks untuk menambah fungsionalitas sistem.