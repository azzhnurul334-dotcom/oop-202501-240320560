# Laporan Praktikum Minggu 1 (sesuaikan minggu ke berapa?)
Topik: Pengenalan Paradigma

## Identitas
- Nama  : Azizah Nurul Putri
- NIM   : 240320560
- Kelas : 3DSRA

---

## Tujuan
1. Mahasiswa mampu mendefinisikan paradigma prosedural, OOP, dan fungsional.
2. Mahasiswa mampu membandingkan kelebihan dan keterbatasan tiap paradigma.
3. Mahasiswa mampu memberikan contoh program sederhana untuk masing-masing paradigma.
4.  Mahasiswa aktif dalam diskusi kelas (bertanya, menjawab, memberi opini).
---

## Dasar Teori
Paradigma pemrograman adalah cara pandang dalam menyusun program:
1. Prosedural: program dibangun sebagai rangkaian perintah (fungsi/prosedur).
2. OOP (Object-Oriented Programming): program dibangun dari objek yang memiliki data (atribut) dan perilaku (method).
3. Fungsional: program dipandang sebagai pemetaan fungsi matematika, lebih menekankan ekspresi dan transformasi data.
Dalam konteks Agri-POS, OOP membantu memodelkan entitas nyata seperti Produk, Transaksi, dan Pembayaran sebagai objek. Dengan demikian, sistem lebih mudah dikembangkan dan dipelihara.
---

## Langkah Praktikum
1. Setup Project
- Pastikan sudah menginstall JDK (Java Development Kit), IDE (misal: IntelliJ IDEA, VS Code, NetBeans), Git, PostgreSQL, dan JavaFX di komputer.
- Buat folder project oop-pos-<nim>.
- Inisialisasi repositori Git.
- Buat struktur awal src/main/java/com/upb/agripos/.
- Pastikan semua tools dapat berjalan (uji dengan membuat dan menjalankan program Java sederhana).

2. Program Sederhana dalam 3 Paradigma
- Prosedural: program untuk menghitung total harga dua produk.
- OOP: class Produk dengan atribut nama dan harga, buat minimal tiga objek, lalu hitung total.
- Fungsional: gunakan Stream atau lambda untuk menghitung total harga dari minimal tiga objek.

3. Commit dan Push
Commit dengan pesan: week1-setup-hello-pos.
---

## Kode Program
1. procedural
```
// HelloProcedural.java
public class HelloProcedural {
    public static void main(String[] args) {
       String nim = "240320560";
       String nama = "Azizah Nurul Putri";
       String[] produk = {"Kacang Hijau", "Kacang Tanah", "Kedelai"};
       int[] harga = {12000, 16000, 21000};
       int total = 0;
       System.out.println("Hello POS World");
       System.out.println("NIM: " + nim + ", Nama: " + nama);
       System.out.println("Daftar Produk:");
       for (int i = 0; i < produk.length; i++) {
          System.out.println("- " + produk[i] + ": " + harga[i]);
          total += harga[i];
       }
       System.out.println("Total harga semua produk: " + total);
    }
}
 ```
2. oop
```
 //HelloOOP.java
class Produk {
    String nama;
    int harga;
    Produk(String nama, int harga) {
       this.nama = nama;
       this.harga = harga;
    }
 }
 
 public class HelloOOP {
    public static void main(String[] args) {
       String namaMhs = "Azizah Nurul Putri";
       String nim = "240320560
       Produk[] daftar = {
          new Produk("Kacang Hijau", 12000),
          new Produk("Kacang Tanah", 16000),
          new Produk("Kedelai", 21000)
       };
       int total = 0;
       System.out.println("Hello World, I am " + namaMhs + "-" + nim);
       System.out.println("Program Agri-POS World");
       System.out.println("Daftar Produk:");
       for (Produk p : daftar) {
          System.out.println("- " + p.nama + ": Rp" + p.harga);
          total += p.harga;
       }
       System.out.println("Total harga semua produk: Rp" + total);
    }
 }
```
3.functional
```
 // HelloFunctional.java
import java.util.*;
import java.util.stream.*;
public class HelloFunctional {
   public static void main(String[] args) {
      String nama = "Azizah Nurul Putri";
      String nim = "240320560";
      List<String> produk = Arrays.asList("Kacang Hijau", "Kacang Tanah", "Kedelai");
      List<Integer> harga = Arrays.asList(12000, 160000, 21000);
      System.out.println("Hello World, I am " + nama + "-" + nim);
      System.out.println("Program Agri-POS World");
      System.out.println("Daftar Produk:");
      IntStream.range(0, produk.size())
         .forEach(i -> System.out.println("- " + produk.get(i) + ": Rp" + harga.get(i)));
      int total = harga.stream().mapToInt(Integer::intValue).sum();
      System.out.println("Total harga semua produk: Rp" + total);
   }
}
```
---

## Hasil Eksekusi
https://github.com/azzhnurul334-dotcom/oop-202501-240320560/tree/781aab13a44ee202e86dcd39f7452acd77e5f261/praktikum/week1-setup-hello-pos
---

## Analisis
1. Jelaskan bagaimana kode berjalan.  
(Program ditulis dalam paradigma procedural.
Eksekusi dimulai dari method main(String[] args).
2.  Apa perbedaan pendekatan minggu ini dibanding minggu sebelumnya. 
Dua variabel dibuat (Nim dan Nama) untuk menyimpan data mahasiswa.
Program mencetak output dengan menggunakan System.out.println, yang menggabungkan teks dengan isi variabel.
Hasilnya:)
3. Kendala yang dihadapi dan cara mengatasinya.  
lupa menuliskan package sesuai struktur folder, sehingga program tidak bisa dijalankan.
solusi: Memastikan struktur folder sesuai dengan deklarasi package (main/java/com/upb/agripos).
Kendala 2: Error ketika menjalankan javac karena file tidak berada di path yang tepat.
---

## Kesimpulan
1. Praktikum ini memberikan pemahaman tentang tiga paradigma pemrograman di Java, yaitu Procedural, OOP, dan Functional.
2. Procedural menekankan pada penggunaan fungsi/metode sederhana tanpa class tambahan.
3. OOP (Object-Oriented Programming) menggunakan class dan object untuk merepresentasikan data dan perilaku secara lebih terstruktur dengan prinsip seperti enkapsulasi.
4. Functional menggunakan lambda expression atau functional interface untuk menuliskan kode yang lebih ringkas dan deklaratif.
5. Dengan membandingkan ketiga paradigma, mahasiswa dapat memahami bahwa satu masalah yang sama (misalnya “Hello World”) bisa diselesaikan dengan pendekatan berbeda, sesuai kebutuhan dan kompleksitas program.
6. Praktikum ini juga melatih mahasiswa untuk memahami perbedaan pola pikir (paradigm shift) antara pemrograman prosedural, berorientasi objek, dan fungsional.
---

## Quiz
1. Apakah OOP selalu lebih baik dari prosedural? 
*Jawaban:* 
Pendekatan OOP tidak selalu lebih baik dari prosedural, karena keduanya memiliki keunggulan masing-masing. OOP lebih sesuai untuk program yang kompleks dan membutuhkan struktur yang terorganisir, sedangkan pendekatan prosedural lebih efektif digunakan pada program yang sederhana dan memiliki alur kerja yang langsung. Pemilihan pendekatan tergantung pada tujuan dan tingkat kompleksitas program yang dibuat.

2. Kapan functional programming lebih cocok digunakan dibanding OOP atau prosedural?
*Jawaban:*
Functional programming lebih cocok digunakan ketika program berfokus pada pengolahan data yang bersifat berulang, kompleks, atau memerlukan transformasi data secara efisien. Pendekatan ini sangat sesuai untuk kasus seperti analisis data, pemrosesan koleksi (list, array), dan operasi matematis, karena dapat menulis kode yang lebih singkat, mudah diuji, serta meminimalkan kesalahan akibat perubahan data (mutasi). Jadi, functional programming lebih unggul ketika dibutuhkan kode yang ringkas, bersifat deklaratif, dan berorientasi pada hasil, bukan pada langkah-langkah proses seperti pada OOP atau prosedural.

3. Bagaimana paradigma (prosedural, OOP, fungsional) memengaruhi maintainability dan scalability aplikasi? 
*Jawaban:*
Paradigma pemrograman sangat memengaruhi maintainability (kemudahan pemeliharaan) dan scalability (kemampuan aplikasi untuk dikembangkan). Pada paradigma prosedural, program biasanya lebih sederhana tetapi sulit dipelihara saat ukurannya membesar karena logika bercampur dalam satu alur. Paradigma OOP meningkatkan maintainability dan scalability karena kode dibagi menjadi class dan object, sehingga lebih mudah dikelola, diuji, serta dikembangkan tanpa mengubah keseluruhan program. Sementara itu, paradigma fungsional mendukung maintainability dengan cara meminimalkan efek samping dan membuat fungsi bersifat mandiri, sehingga mudah diuji dan diperluas. Dengan demikian, semakin baik struktur paradigma yang digunakan, semakin mudah aplikasi untuk dirawat dan dikembangkan di masa depan.
