
# Peran Type System dalam IoT

1. **Identifikasi Problem**
Problem: Bagaimana "type system" mempengaruhi keamanan dan keandalan perangkat IoT yang dikembangkan menggunakan bahasa pemrograman seperti C/C++?

2. **Deskripsi Problem**
Deskripsi:
Dalam pengembangan perangkat IoT, penggunaan bahasa pemrograman seperti C/C++ sangat umum karena performa dan efisiensinya. Namun, bahasa ini memiliki manajemen memori manual yang rentan terhadap kesalahan seperti buffer overflow, dereferencing null pointers, dan type mismatch. "Type system" dalam bahasa pemrograman membantu mencegah kesalahan ini dengan memverifikasi tipe data selama kompilasi. Hal ini penting untuk menjaga keamanan dan keandalan perangkat IoT, yang sering kali beroperasi di lingkungan yang tidak aman dan sensitif.

3. **Metodologi Eksperimen**
Metodologi:
Eksperimen ini bertujuan untuk menunjukkan bagaimana "type system" dalam C++ dapat mencegah kesalahan dalam kode yang berpotensi menyebabkan kegagalan fungsi perangkat IoT. Anda akan mengembangkan dua program sederhana di Tinkercad dengan Arduino: satu dengan type checking yang ketat, dan satu lagi dengan type checking yang longgar (atau tidak ada type checking).

Program 1: Menggunakan type checking yang ketat (misalnya, dengan deklarasi tipe data yang jelas dan eksplisit).
Program 2: Tidak menggunakan type checking yang ketat (misalnya, menggunakan casting tipe data secara manual atau tidak mendeklarasikan tipe data dengan jelas).

4. **Pelaksanaan Eksperimen**
Pelaksanaan:

Siapkan Arduino di Tinkercad:

Buat dua proyek baru di Tinkercad, masing-masing untuk Program 1 dan Program 2.
Program 1:

Tulis kode Arduino dengan deklarasi tipe data yang ketat.
Contoh: Mendeklarasikan semua variabel dengan tipe data yang tepat (int, float, dll).
Simulasikan hasilnya dan catat setiap kesalahan yang terjadi.
Program 2:

Tulis kode Arduino tanpa type checking yang ketat.
Contoh: Menggunakan casting tipe data secara manual atau membiarkan tipe data ambigu.
Simulasikan hasilnya dan catat setiap kesalahan yang terjadi.
Bandingkan:

Bandingkan kedua program tersebut dalam hal keandalan dan kemudahan mendeteksi kesalahan.

5. **Analisis Hasil Eksperimen**
Analisis:
Dari eksperimen ini, Anda diharapkan untuk mengamati bahwa Program 1, dengan type checking yang ketat, cenderung lebih aman dan andal. Kesalahan seperti overflow atau tipe data yang tidak kompatibel akan lebih mudah dideteksi selama proses kompilasi, sehingga mengurangi kemungkinan terjadinya error selama runtime. Sementara itu, Program 2 mungkin menunjukkan hasil yang tidak diharapkan atau bahkan menyebabkan kegagalan fungsi pada perangkat, menunjukkan risiko dari type checking yang longgar.

**Kesimpulan:**
"Type system" berperan penting dalam pengembangan IoT untuk memastikan kode lebih aman dan andal. Dengan type checking yang ketat, pengembang dapat mencegah banyak kesalahan umum yang bisa membahayakan fungsi perangkat IoT, terutama ketika digunakan di lingkungan yang rentan terhadap gangguan.

Eksperimen ini diharapkan dapat membantu Anda memahami bagaimana "type system" bekerja dalam konteks pengembangan IoT, dan mengapa penting untuk mempertimbangkan aspek ini saat menulis kode untuk perangkat yang sensitif dan kritis.

