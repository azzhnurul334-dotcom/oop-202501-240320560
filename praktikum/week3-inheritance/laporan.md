# Laporan Praktikum Minggu 3 
Topik: [Tuliskan judul topik, misalnya "Class dan Object"]

## Identitas
- Nama  : [Nama Mahasiswa]
- NIM   : [NIM Mahasiswa]
- Kelas : [Kelas]

---

## Tujuan
- Mahasiswa memahami konsep inheritance dalam OOP.
- Mahasiswa mampu membuat kelas induk (parent) dan kelas anak (child)
- Mahasiswa dapat mengimplementasikan pewarisan untuk mengurangi duplikasi kode dan membuat program lebih terstruktur

## Dasar Teori
1. Inheritance adalah mekanisme pewarisan sifat dari class induk ke class anak.
2. Class anak dapat mengakses atribut dan method milik class induk.
3. Keyword extends digunakan untuk melakukan inheritance di Java.
4. Inheritance membuat kode lebih efisien, reusable, dan mudah dikembangkan.
5. Method milik induk dapat dioverride di class anak jika perlu.

## Langkah Praktikum
1. Buat project baru dengan nama sesuai topik, misalnya Agripos.
2. Buat class induk (superclass) dengan nama Produk yang berisi atribut umum seperti kode, nama, harga, dan stok.
3. Buat class turunan (subclass) seperti BenihKacang, PupukUrea, dan Alat yang mewarisi dari class Produk dan menambahkan atribut khusus sesuai kebutuhan.
4. Buat class utama bernama MainInheritance untuk menguji konsep pewarisan dengan membuat objek dari masing-masing subclass dan menampilkan data melalui metode getter.
5. Tambahkan class utilitas seperti CreditBy untuk menampilkan identitas mahasiswa (nama dan NIM).
6. Jalankan program dan amati hasil output di konsol untuk memastikan pewarisan berjalan dengan benar.
7. lalu commit dan push.

## Kode Program
package model;

public class Produk {
    private String kode;
    private String nama;
    private double harga;
    private int stok;

    public Produk(String kode, String nama, double harga, int stok) {
        this.kode = kode;
        this.nama = nama;
        this.harga = harga;
        this.stok = stok;
    }

    public String getKode() { return kode; }
    public String getNama() { return nama; }
    public double getHarga() { return harga; }
    public int getStok() { return stok; }

    public void tampilkanInfo() {
        System.out.println("Kode: " + kode + ", Nama: " + nama + ", Harga: " + harga + ", Stok: " + stok);
    }
}

(Benih Java)

package model;

public class Benih extends Produk {
    private String varietas;

    public Benih(String kode, String nama, double harga, int stok, String varietas) {
        super(kode, nama, harga, stok);
        this.varietas = varietas;
    }

    public String getVarietas() { return varietas; }
    public void setVarietas(String varietas) { this.varietas = varietas; }
}

(Pupuk Java)

package model;

    public class Pupuk extends Produk {
        private String jenis;
    
        public Pupuk(String kode, String nama, double harga, int stok, String jenis) {
            super(kode, nama, harga, stok);
            this.jenis = jenis;
        }
    
        public String getJenis() { return jenis; }
        public void setJenis(String jenis) { this.jenis = jenis; }
    }

(AlatPertanian Java)

package model;

public class AlatPertanian extends Produk {
    private String bahan;

    public AlatPertanian(String kode, String nama, double harga, int stok, String bahan) {
        super(kode, nama, harga, stok);
        this.bahan = bahan;
    }

    public String getBahan() { return bahan; }
    public void setBahan(String bahan) { this.bahan = bahan; }
}

(MainInheritance)

import model.*;
import util.*;

public class MainInheritance {
    public static void main(String[] args) {
        Benih b = new Benih("BNH-001", "Benih Padi IR64", 25000, 100, "IR64");
        Pupuk p = new Pupuk("PPK-101", "Pupuk Urea", 350000, 40, "Urea");
        AlatPertanian a = new AlatPertanian("ALT-501", "Cangkul Baja", 90000, 15, "Baja");

        System.out.println("Benih: " + b.getNama() + ", Varietas: " + b.getVarietas());
        System.out.println("Pupuk: " + p.getNama() + ", Jenis: " + p.getJenis());
        System.out.println("Alat Pertanian: " + a.getNama() + ", Bahan: " + a.getBahan());

        CreditBy.tampilkan("Febiana Saputri", "240320569");
    }
}


## Hasil Eksekusi
(Sertakan screenshot hasil eksekusi program.  
![Screenshot hasil](screenshots/hasil.png)
)
---

## Analisis
(
- Jelaskan bagaimana kode berjalan.  
- Apa perbedaan pendekatan minggu ini dibanding minggu sebelumnya.  
- Kendala yang dihadapi dan cara mengatasinya.  
)
---

## Kesimpulan
(Tuliskan kesimpulan dari praktikum minggu ini.  
Contoh: *Dengan menggunakan class dan object, program menjadi lebih terstruktur dan mudah dikembangkan.*)

---

## Quiz
(1. [Tuliskan kembali pertanyaan 1 dari panduan]  
   **Jawaban:** …  

2. [Tuliskan kembali pertanyaan 2 dari panduan]  
   **Jawaban:** …  

3. [Tuliskan kembali pertanyaan 3 dari panduan]  
   **Jawaban:** …  )
