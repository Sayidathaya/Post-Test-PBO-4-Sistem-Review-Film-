# Post Test PBO 4 Sistem Review Film
## Sayid Rafi A'thaya
## 2409116036
## SI Kelas A Akt 24


# 🎬 Sistem Manajemen Rating Film

---

## 📂 Struktur Folder (MVC)
<img width="269" height="250" alt="Image" src="https://github.com/user-attachments/assets/989e6050-4978-49d1-ba81-e918254a33d5" />

---

## ActionFilm.java

<img width="1102" height="566" alt="Image" src="https://github.com/user-attachments/assets/1da0cca0-f644-4d8b-b2b7-1b400615b668" /> 

## 📌 Penjelasan

* `ActionFilm` **extends Film** → artinya class ini adalah subclass dari `Film`.
* Menambahkan atribut khusus: `explosionCount` untuk menyimpan jumlah adegan ledakan.
* **Constructor** dipakai untuk menginisialisasi data film action beserta jumlah ledakan.
* **Overriding**: method `showDetail()` ditulis ulang sesuai dengan kebutuhan genre action (menampilkan jumlah ledakan).
* Konsep OOP yang terlihat di sini:

  * **Inheritance**: mewarisi atribut `title`, `director`, `releaseYear` dari `Film`.
  * **Polymorphism (Overriding)**: method `showDetail()` menimpa method abstrak di superclass.

---

## ✅ Kesimpulan

File **`ActionFilm.java`** menunjukkan penerapan **Abstraction** (mengimplementasi method abstrak `showDetail()` dari class `Film`) dan **Polymorphism** melalui **Overriding**. Dengan demikian, class ini sudah sesuai dengan ketentuan tugas:

* Menggunakan **abstract class** (`Film`) → Abstraction.
* Menggunakan **Overriding** (`showDetail()`) → Polymorphism.

---

## ComedyFilm.java

<img width="1083" height="544" alt="Image" src="https://github.com/user-attachments/assets/6ff5992e-72a2-4361-8176-4bb6583cdd3b" />

---

## 📌 Penjelasan

* `ComedyFilm` **extends Film** → subclass dari `Film`.
* Menambahkan atribut khusus: `jokeCount` untuk menyimpan jumlah lelucon dalam film.
* **Constructor** digunakan untuk menginisialisasi data film komedi dan jumlah lelucon.
* **Overriding**: method `showDetail()` diimplementasikan ulang agar menampilkan informasi sesuai genre komedi.
* Konsep OOP yang diterapkan:

  * **Inheritance** → mewarisi atribut `title`, `director`, `releaseYear` dari `Film`.
  * **Polymorphism (Overriding)** → method `showDetail()` menimpa method abstrak dari `Film`.

---

## ✅ Kesimpulan

File **`ComedyFilm.java`** memperlihatkan penerapan **Abstraction** (implementasi method abstrak `showDetail()` dari `Film`) serta **Polymorphism** lewat **Overriding**. Dengan begitu, class ini sudah memenuhi syarat:

* **Abstraction** melalui abstract class `Film`.
* **Polymorphism (Overriding)** pada method `showDetail()`.

---

## DramaFilm.java

<img width="1094" height="542" alt="Image" src="https://github.com/user-attachments/assets/ea539867-83c1-41af-bf06-19ec0f4a28ab" />

---

## 📌 Penjelasan

* `DramaFilm` **extends Film** → merupakan subclass dari `Film`.
* Menambahkan atribut khusus: `mainTheme` untuk menyimpan tema utama film.
* **Constructor** digunakan untuk menginisialisasi data film drama beserta tema utamanya.
* **Overriding**: method `showDetail()` diimplementasikan ulang untuk menampilkan detail khas film drama.
* Konsep OOP yang digunakan:

  * **Inheritance** → mewarisi atribut `title`, `director`, `releaseYear` dari `Film`.
  * **Polymorphism (Overriding)** → `showDetail()` menimpa method abstrak dari `Film`.

---

## ✅ Kesimpulan

File **`DramaFilm.java`** memperlihatkan penerapan **Abstraction** (mengimplementasikan method abstrak `showDetail()` dari `Film`) dan **Polymorphism** melalui **Overriding**.
Dengan ini, class sudah memenuhi ketentuan tugas:

* **Abstraction** lewat abstract class `Film`.
* **Polymorphism (Overriding)** di method `showDetail()`.

---

## Film.java

<img width="1050" height="882" alt="Image" src="https://github.com/user-attachments/assets/87ddc0d0-270b-404b-bcd8-ab6c916758e0" />

---

## 📌 Penjelasan

* **Abstract Class** → `Film` dideklarasikan sebagai `abstract`, sehingga tidak bisa dibuat objek langsung, hanya bisa diturunkan.
* **Atribut umum**: `title`, `director`, `releaseYear` berlaku untuk semua film.
* **List<Rating>** → menyimpan daftar review menggunakan class bantu `Rating`.
* **Method abstrak** `showDetail()` → wajib diimplementasikan oleh subclass (`ActionFilm`, `ComedyFilm`, `DramaFilm`).
* **Overloading**:

  * `addRating(String comment)` → hanya komentar, skor default 0.
  * `addRating(String comment, int score)` → komentar + skor.
* **showRatings()** → menampilkan daftar review untuk film tertentu.

---

## ✅ Kesimpulan

File **`Film.java`** adalah pusat penerapan **Abstraction** karena mendefinisikan method abstrak `showDetail()` yang harus diimplementasikan subclass. Selain itu, file ini juga menerapkan **Polymorphism (Overloading)** lewat dua versi `addRating()`. Dengan demikian:

* **Abstraction** → lewat abstract class dan method `showDetail()`.
* **Polymorphism (Overloading)** → lewat method `addRating()`.

---

## Rating.java

<img width="1098" height="584" alt="Image" src="https://github.com/user-attachments/assets/daa5767e-0957-43fb-ab68-3a07bf16be0d" />

---

## 📌 Penjelasan

* Class **`Rating`** berfungsi sebagai entitas data untuk menyimpan review film.
* Atribut **private** `comment` dan `score` menunjukkan **encapsulation** karena tidak bisa diakses langsung dari luar.
* Untuk mengakses nilainya, digunakan **getter**: `getComment()` dan `getScore()`.
* Objek ini dipakai dalam class `Film` untuk menyimpan daftar review (`List<Rating>`).

---

## ✅ Kesimpulan

File **`Rating.java`** adalah class sederhana yang mendukung sistem review. Penerapan **Encapsulation** terlihat pada penggunaan **private fields** dan **getter methods** untuk menjaga akses data.

* **Encapsulation** → melindungi data `comment` dan `score` agar hanya bisa dibaca melalui getter.

---

## FilmService.java

<img width="1085" height="608" alt="Image" src="https://github.com/user-attachments/assets/6abd23ec-7322-4f79-9d6b-566033e75076" />

---

## 📌 Penjelasan

* **Atribut** `films` bertipe `List<Film>` untuk menyimpan berbagai jenis film.
* **addFilm(Film film)** → menambahkan objek film (baik itu Action, Comedy, atau Drama).
* **showAllFilms()** → memanggil `film.showDetail()`.

  * Inilah bentuk **Polymorphism (Overriding)** → method yang dijalankan berbeda sesuai tipe objek film (`ActionFilm`, `ComedyFilm`, `DramaFilm`).
* **Encapsulation** → `films` dibuat private agar tidak bisa dimanipulasi langsung dari luar.

---

## ✅ Kesimpulan

File **`FilmService.java`** berperan sebagai manajer daftar film.

* **Polymorphism (Overriding)** → ditunjukkan saat pemanggilan `film.showDetail()`, di mana setiap subclass `Film` punya implementasi berbeda.
* **Encapsulation** → data `films` dilindungi dengan private, hanya bisa diakses lewat method publik.

---

## Main.java

<img width="1227" height="858" alt="Image" src="https://github.com/user-attachments/assets/121a187b-930d-486f-a603-37d43f469b12" />

---

## 📌 Penjelasan

* **FilmService** dibuat untuk menampung daftar film.
* **Objek Film** dibuat dari berbagai genre: `ActionFilm`, `ComedyFilm`, `DramaFilm`.
* **addFilm()** → menyimpan film ke dalam `FilmService`.
* **addRating()** → menunjukkan **Overloading**:

  * `addRating("Super lucu!")` → hanya komentar.
  * `addRating("Penuh aksi keren!", 9)` → komentar + skor.
* **showDetail()** → menunjukkan **Overriding**, karena tiap subclass `Film` menampilkan detail dengan format berbeda.
* **showRatings()** → menampilkan semua review yang ditambahkan.

---

## ✅ Kesimpulan

File **`Main.java`** mendemonstrasikan implementasi semua konsep OOP dalam aplikasi ini:

* **Abstraction** → penggunaan `Film` sebagai abstract class melalui objek turunannya.
* **Polymorphism (Overloading)** → pemanggilan `addRating()` dengan parameter berbeda.
* **Polymorphism (Overriding)** → pemanggilan `showDetail()` sesuai tipe film (Action, Comedy, Drama).

---

## Output

<img width="614" height="474" alt="Image" src="https://github.com/user-attachments/assets/3a158b32-7489-4e7d-b865-119b20c080d3" />

---

### 📌 Analisis Output

1. **Polymorphism (Overriding)**

   * Saat `filmService.showAllFilms()` dipanggil, method `showDetail()` menampilkan detail sesuai jenis film:

     * ActionFilm → ada info jumlah ledakan.
     * ComedyFilm → ada info jumlah joke.
     * DramaFilm → ada info tema utama.

   Ini membuktikan bahwa **method overriding** berjalan sesuai harapan.

2. **Polymorphism (Overloading)**

   * Pada review:

     * `"Super lucu!"` → dipanggil dengan method `addRating(String comment)` (skor default 0).
     * `"Penuh aksi keren!", 9` → dipanggil dengan `addRating(String comment, int score)`.
       Terlihat jelas perbedaan hasil skor, menunjukkan **overloading** berhasil.

3. **Abstraction**

   * Objek `film1`, `film2`, `film3` didefinisikan dari subclass (`ActionFilm`, `ComedyFilm`, `DramaFilm`), tetapi semua diperlakukan sebagai **tipe `Film`** dalam `FilmService`.
   * `Film` sendiri tidak bisa diinstansiasi langsung karena merupakan abstract class.

4. **Encapsulation**

   * Atribut `comment` dan `score` dalam `Rating` hanya bisa diakses via getter, ditampilkan saat `showRatings()`.

---

### ✅ Kesimpulan Output

* Program sudah berhasil **mendemonstrasikan Abstraction, Overloading, dan Overriding** sesuai ketentuan tugas.
* Output final menampilkan **detail film per genre** (hasil overriding) dan **review film dengan skor berbeda** (hasil overloading).
* Build sukses menunjukkan tidak ada error pada runtime.

---
