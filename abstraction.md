
- **Topik:** Abstraction
- **Content:** Domain Spesific Language
- **PIC:** Micho Dhani Firmansyah
- **Kelompok:** 1 | Prinsip Bahasa Pemrograman | Praktek
- **Tautan Referensi:** [Abstraction - ChatGPT](https://chatgpt.com/share/fd2954f2-e305-4cc4-87a4-84a7b9b166d4)

---
# <p style="text-align: center;">Pertanyaan 👨🏼</p>
hai, aku ingin melakukan eksperimen terkait topik "Abstraction pada IoT menggunakan bahasa Arduino" kalau bisa sih dengan patokan rangkaian kegiatan berikut
 
1. Identifikasi Problem
2. Deskripsi Problem
3. Metodologi Experiment
4. Pelaksanaan Experiment
5. Analisis Hasil Experiment

kalau bisa berikan contoh konteks dalam bahasa Arduinonya ya

---
# <p style="text-align: center;">Jawaban AI 🤖</p>
Untuk topik "Abstraction pada IoT menggunakan bahasa Arduino," kita bisa melakukan eksperimen dengan struktur berikut:

### 1. Identifikasi Problem
**Problem Statement**:  
Pada sistem IoT, perangkat sering kali membutuhkan kontrol atas berbagai sensor dan aktuator yang berbeda-beda. Menulis kode untuk setiap perangkat secara langsung (hardcoding) dapat menghasilkan kode yang sulit dibaca, dipelihara, dan diperluas. Bagaimana kita bisa menggunakan prinsip *abstraction* untuk menyederhanakan kontrol perangkat ini?

### 2. Deskripsi Problem
**Deskripsi**:  
Ketika membangun proyek IoT dengan banyak sensor dan aktuator, kita sering kali berurusan dengan berbagai detail spesifik perangkat keras. Ini membuat kode menjadi kompleks dan terfragmentasi. Prinsip *abstraction* memungkinkan kita untuk menyembunyikan kompleksitas ini dan membuat kode lebih modular dan mudah dipahami. Tujuan dari eksperimen ini adalah untuk menunjukkan bagaimana *abstraction* dapat diterapkan dalam kode Arduino untuk mengelola beberapa perangkat secara lebih efisien.

### 3. Metodologi Experiment
**Langkah-langkah**:
1. **Membangun Rangkaian Sederhana**: Buat rangkaian yang terdiri dari beberapa sensor (misalnya, sensor suhu, sensor cahaya) dan aktuator (misalnya, LED, buzzer).
2. **Menulis Kode tanpa Abstraction**: Tulis kode Arduino untuk mengontrol semua perangkat secara langsung tanpa menggunakan abstraction.
3. **Menulis Kode dengan Abstraction**: Tulis ulang kode menggunakan konsep *abstraction* untuk mengabstraksi kontrol perangkat.
4. **Perbandingan**: Bandingkan kode yang dihasilkan dari kedua pendekatan dalam hal keterbacaan, modularitas, dan kemudahan pemeliharaan.

### 4. Pelaksanaan Experiment
**❗Langkah 1: Rangkaian Sederhana**
- Hubungkan sensor suhu (misalnya, DHT11), sensor cahaya (LDR), LED, dan buzzer ke Arduino.

**❗Langkah 2: Kode tanpa Abstraction**
```cpp
#include <DHT.h>

#define DHTPIN 2
#define DHTTYPE DHT11
#define LDRPIN A0
#define LEDPIN 13
#define BUZZERPIN 12

DHT dht(DHTPIN, DHTTYPE);

void setup() {
  pinMode(LEDPIN, OUTPUT);
  pinMode(BUZZERPIN, OUTPUT);
  dht.begin();
  Serial.begin(9600);
}

void loop() {
  float temp = dht.readTemperature();
  int lightLevel = analogRead(LDRPIN);
  
  if(temp > 30) {
    digitalWrite(LEDPIN, HIGH);
    digitalWrite(BUZZERPIN, HIGH);
  } else {
    digitalWrite(LEDPIN, LOW);
    digitalWrite(BUZZERPIN, LOW);
  }
  
  Serial.print("Temperature: ");
  Serial.println(temp);
  Serial.print("Light Level: ");
  Serial.println(lightLevel);
  
  delay(1000);
}
```

**❗Langkah 3: Kode dengan Abstraction**
```cpp
#include <DHT.h>

#define DHTPIN 2
#define DHTTYPE DHT11
#define LDRPIN A0
#define LEDPIN 13
#define BUZZERPIN 12

DHT dht(DHTPIN, DHTTYPE);

class Sensor {
public:
  virtual int read() = 0;
};

class TemperatureSensor : public Sensor {
public:
  int read() {
    return dht.readTemperature();
  }
};

class LightSensor : public Sensor {
public:
  int read() {
    return analogRead(LDRPIN);
  }
};

class Actuator {
public:
  virtual void activate(int value) = 0;
};

class LED : public Actuator {
public:
  void activate(int value) {
    digitalWrite(LEDPIN, value);
  }
};

class Buzzer : public Actuator {
public:
  void activate(int value) {
    digitalWrite(BUZZERPIN, value);
  }
};

TemperatureSensor tempSensor;
LightSensor lightSensor;
LED led;
Buzzer buzzer;

void setup() {
  pinMode(LEDPIN, OUTPUT);
  pinMode(BUZZERPIN, OUTPUT);
  dht.begin();
  Serial.begin(9600);
}

void loop() {
  int temp = tempSensor.read();
  int lightLevel = lightSensor.read();
  
  led.activate(temp > 30 ? HIGH : LOW);
  buzzer.activate(temp > 30 ? HIGH : LOW);
  
  Serial.print("Temperature: ");
  Serial.println(temp);
  Serial.print("Light Level: ");
  Serial.println(lightLevel);
  
  delay(1000);
}
```

### 5. Analisis Hasil Experiment
**Analisis**:  
- **Keterbacaan**: Kode dengan *abstraction* lebih mudah dibaca karena penggunaan kelas dan metode abstrak yang lebih spesifik.
- **Modularitas**: Dengan abstraction, kode menjadi lebih modular, memisahkan logika sensor dan aktuator dari kode utama.
- **Pemeliharaan**: Kode dengan *abstraction* lebih mudah untuk diperbarui atau diperluas karena setiap sensor atau aktuator dapat diubah tanpa mempengaruhi keseluruhan kode.

**Kesimpulan**:  
Penerapan *abstraction* pada sistem IoT dengan Arduino memberikan struktur yang lebih baik pada kode, membuatnya lebih mudah dipahami dan dipelihara. Ini sangat penting dalam proyek-proyek besar di mana berbagai sensor dan aktuator digunakan.

Itu adalah contoh eksperimen yang bisa kamu lakukan untuk memahami prinsip *abstraction* dalam konteks IoT menggunakan Arduino. Jika ada yang perlu diperjelas atau dimodifikasi, kasih tahu saja!

---
# <p style="text-align: center;">Pertanyaan Lanjutan 🤓</p>

<p style="text-align: center;">bisa elaborasikan lebih lanjut kah terkait cara kerja abstraction pada contoh yang kamu berikan?</p>

---
# <p style="text-align: center;">Jawaban AI 🤖</p>
Tentu! Mari kita bahas lebih dalam bagaimana *abstraction* bekerja dalam contoh kode Arduino yang sudah saya berikan.

### Apa Itu *Abstraction*?
*Abstraction* adalah konsep dalam pemrograman di mana detail yang tidak relevan disembunyikan, dan hanya informasi penting yang ditampilkan. Dengan abstraction, kita bisa fokus pada hal-hal penting tanpa harus pusing dengan detail implementasi. Dalam konteks Arduino, abstraction berarti kita menyembunyikan detail pengoperasian hardware (seperti membaca sensor atau mengaktifkan aktuator) di balik antarmuka yang lebih sederhana.

### Bagaimana Abstraction Diterapkan di Contoh Kode?

Dalam contoh kode yang diberikan, kita melakukan abstraction dengan cara membuat kelas-kelas (*classes*) untuk sensor dan aktuator. Berikut adalah rincian bagaimana abstraction bekerja di sini:

#### 1. Kelas Sensor dan Actuator
Pada kode ini, ada dua kelas abstrak: `Sensor` dan `Actuator`. Kelas abstrak ini tidak mengimplementasikan metode apapun, tetapi mendefinisikan antarmuka (interface) yang harus diikuti oleh kelas turunannya.

- **Sensor**: Kelas ini mendefinisikan metode `read()`. Setiap sensor yang kita buat akan mengimplementasikan metode ini untuk membaca data dari sensor tertentu.

    ```cpp
    class Sensor {
    public:
      virtual int read() = 0;
    };
    ```

- **Actuator**: Kelas ini mendefinisikan metode `activate(int value)`. Setiap aktuator akan mengimplementasikan metode ini untuk mengaktifkan atau menonaktifkan perangkat tertentu (misalnya, menyalakan LED atau buzzer).

    ```cpp
    class Actuator {
    public:
      virtual void activate(int value) = 0;
    };
    ```

#### 2. Kelas Khusus untuk Sensor dan Actuator
Kemudian, kita membuat kelas turunan yang mewarisi kelas `Sensor` dan `Actuator`, masing-masing untuk sensor suhu (`TemperatureSensor`) dan sensor cahaya (`LightSensor`), serta untuk LED (`LED`) dan buzzer (`Buzzer`).

- **TemperatureSensor**: Kelas ini mengimplementasikan metode `read()` untuk membaca suhu menggunakan objek `DHT`.

    ```cpp
    class TemperatureSensor : public Sensor {
    public:
      int read() {
        return dht.readTemperature();
      }
    };
    ```

- **LightSensor**: Kelas ini mengimplementasikan metode `read()` untuk membaca tingkat cahaya dari LDR.

    ```cpp
    class LightSensor : public Sensor {
    public:
      int read() {
        return analogRead(LDRPIN);
      }
    };
    ```

- **LED**: Kelas ini mengimplementasikan metode `activate(int value)` untuk mengontrol LED (ON atau OFF).

    ```cpp
    class LED : public Actuator {
    public:
      void activate(int value) {
        digitalWrite(LEDPIN, value);
      }
    };
    ```

- **Buzzer**: Kelas ini mengimplementasikan metode `activate(int value)` untuk mengontrol buzzer (ON atau OFF).

    ```cpp
    class Buzzer : public Actuator {
    public:
      void activate(int value) {
        digitalWrite(BUZZERPIN, value);
      }
    };
    ```

#### 3. Penggunaan Abstraction dalam *Loop*
Di dalam fungsi `loop()`, kita bisa menggunakan objek-objek ini tanpa memikirkan bagaimana mereka bekerja di balik layar. Kita hanya memanggil metode `read()` dari sensor dan `activate(int value)` dari aktuator.

```cpp
void loop() {
  int temp = tempSensor.read();  // Baca suhu dari sensor suhu
  int lightLevel = lightSensor.read();  // Baca tingkat cahaya dari sensor cahaya
  
  led.activate(temp > 30 ? HIGH : LOW);  // Nyalakan LED jika suhu > 30
  buzzer.activate(temp > 30 ? HIGH : LOW);  // Nyalakan buzzer jika suhu > 30
  
  Serial.print("Temperature: ");
  Serial.println(temp);
  Serial.print("Light Level: ");
  Serial.println(lightLevel);
  
  delay(1000);
}
```

#### Keuntungan dari Abstraction

1. **Keterbacaan**: Kode menjadi lebih bersih dan mudah dibaca karena kita tidak perlu melihat detail implementasi dari masing-masing perangkat. Kita hanya fokus pada logika aplikasi.
  
2. **Modularitas**: Jika kita ingin mengganti sensor atau aktuator dengan jenis lain, kita hanya perlu membuat kelas baru yang mengimplementasikan antarmuka yang sama. Tidak perlu mengubah logika aplikasi utama.

3. **Pemeliharaan**: Jika ada perubahan dalam cara kerja sensor atau aktuator (misalnya, jika kita pindah dari DHT11 ke DHT22), kita hanya perlu mengubah kelas yang bersangkutan tanpa menyentuh kode di bagian lain.

### Kesimpulan
*Abstraction* memungkinkan kita untuk menulis kode yang lebih modular, mudah dibaca, dan lebih mudah untuk dikembangkan atau diubah. Dalam konteks Arduino dan IoT, ini sangat berguna karena kita sering kali berhadapan dengan berbagai perangkat keras yang berbeda-beda. Dengan abstraction, kita dapat menyembunyikan detail perangkat keras tersebut dan fokus pada logika aplikasi yang lebih tinggi.

Semoga penjelasan ini membantu memahami cara kerja *abstraction* dalam contoh kode yang diberikan. Kalau ada yang masih kurang jelas, jangan ragu untuk tanya lagi!

---

© T1 - PBP - TIF423