
# Laporan Tugas Kelompok

## **Topik:** Event-Driven Programming
## **Content:** Reactive Programming
## **PIC:** Nieto Salim Maula
## **Kelompok:** 1
## **Tautan Referensi:** [Referensi 1](#), [Referensi 2](#), [Referensi 3](#)

---

## **1. Identifikasi Problem**

Di dunia industri, perangkat Internet of Things (IoT) memainkan peran kunci dalam mengotomatisasi dan memantau berbagai proses. Salah satu tantangan kritis adalah bagaimana perangkat IoT yang menggunakan Arduino dan bahasa pemrograman C/C++ dapat merespons event secara real-time dalam lingkungan yang dinamis dan sering berubah. Respons yang lambat atau tidak akurat dapat mengakibatkan kegagalan sistem, downtime yang mahal, atau bahkan situasi berbahaya, seperti dalam kontrol industri atau sistem keamanan. Oleh karena itu, kemampuan untuk menerapkan *Event-Driven Programming* dengan efisien dan akurat menjadi sangat penting, namun juga sulit dikuasai karena membutuhkan keahlian khusus dalam pengelolaan sumber daya terbatas dan pemrograman tingkat rendah.

## **2. Deskripsi Problem**

Perangkat IoT di industri sering kali harus merespons berbagai event kritis, seperti perubahan suhu, tekanan, atau deteksi anomali lainnya. Namun, perangkat ini biasanya memiliki keterbatasan sumber daya, baik dalam hal daya komputasi maupun energi. Implementasi *Event-Driven Programming* pada Arduino menggunakan C/C++ memungkinkan perangkat ini merespons event dengan cepat dan efisien, namun juga menantang karena memerlukan optimasi yang cermat dalam pemrograman. Kesalahan dalam implementasi dapat menyebabkan respons yang tidak tepat waktu, yang bisa berdampak negatif pada operasional sistem industri.

## **3. Metodologi Experiment**

Untuk menyelidiki efektivitas *Event-Driven Programming* dalam konteks ini, eksperimen dilakukan dengan langkah-langkah berikut:

1. **Identifikasi Event Kritikal:**
   - Menentukan event yang relevan dan kritis dalam aplikasi industri, seperti deteksi suhu yang melebihi ambang batas atau gerakan yang tidak biasa.

2. **Desain Rangkaian dan Implementasi:**
   - Merancang dan merakit rangkaian yang menggunakan sensor untuk mendeteksi event dan aktuator untuk merespons event tersebut, seperti menyalakan LED atau alarm.

3. **Penulisan Kode Optimal:**
   - Mengembangkan kode dalam bahasa C/C++ yang memanfaatkan *Event-Driven Programming* untuk merespons event secara real-time, dengan fokus pada optimasi penggunaan CPU dan daya.

4. **Pengujian Simulasi dan Nyata:**
   - Menggunakan Tinkercad untuk simulasi awal dan menguji perangkat keras nyata untuk memastikan bahwa sistem dapat merespons event dengan tepat dan dalam batas waktu yang diperlukan oleh aplikasi industri.

## **4. Pelaksanaan Experiment**

1. **Persiapan Rangkaian:**
   - Rangkai komponen seperti sensor suhu atau tombol untuk mendeteksi event, dan hubungkan dengan aktuator seperti LED atau buzzer untuk menandakan respons. Pastikan koneksi stabil dan rangkaian sesuai dengan spesifikasi yang direncanakan.

2. **Implementasi Kode dan Pengujian:**
   - Tulis kode dalam C/C++ yang memungkinkan perangkat untuk mendeteksi dan merespons event secara real-time. Unggah kode ke Arduino dan lakukan pengujian dalam kondisi simulasi menggunakan Tinkercad dan perangkat keras nyata.

3. **Pengamatan dan Pengumpulan Data:**
   - Amati bagaimana sistem merespons event, catat waktu respons, penggunaan daya, dan efisiensi sumber daya. Lakukan pengujian berulang kali untuk mengevaluasi stabilitas sistem.

## **5. Analisis Hasil Experiment**

1. **Evaluasi Kecepatan Respons:**
   - Analisis seberapa cepat sistem merespons event kritis dan apakah respons tersebut sesuai dengan kebutuhan aplikasi industri. Bandingkan waktu respons dengan standar yang dibutuhkan.

2. **Efisiensi Penggunaan Sumber Daya:**
   - Evaluasi bagaimana sistem mengelola penggunaan CPU dan daya selama merespons event. Bandingkan hasil ini dengan pendekatan lain, seperti polling, untuk menilai keunggulan *Event-Driven Programming*.

3. **Kesesuaian dengan Kebutuhan Industri:**
   - Bandingkan performa sistem dengan persyaratan industri, seperti keandalan dan efisiensi dalam kondisi nyata. Apakah implementasi ini dapat digunakan dalam skenario industri yang memerlukan respons cepat dan efisien?

4. **Kesimpulan:**
   - Berdasarkan hasil eksperimen, simpulkan efektivitas *Event-Driven Programming* dalam aplikasi industri menggunakan Arduino dan C/C++. Identifikasi tantangan yang tersisa dan saran untuk pengembangan lebih lanjut, terutama dalam konteks penerapan di industri yang memerlukan penguasaan keahlian langka.

