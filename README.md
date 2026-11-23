# Library Book List (`TesJavaSwing`)

Aplikasi desktop sederhana berbasis **Java Swing** dan **Apache Maven** untuk menampilkan daftar buku dalam bentuk tabel serta menambahkan data buku baru melalui form input interaktif.

> Proyek ini merupakan repository latihan pengelolaan project Java Maven multi-package. Entry point aplikasi utama berada di `org.example.main.BookTable`.

---

## Fitur Aplikasi

Berdasarkan `src/main/java/org/example/main/BookTable.java`:

- **Tabel Daftar Buku (`JTable` + `DefaultTableModel`)**: Menampilkan data awal daftar buku dalam kolom `Book ID`, `Title`, `Author`, dan `Year` di dalam `JScrollPane` (`600 x 400`).
- **Form Input Buku Baru**: Menyediakan field `Book ID`, `Title`, `Author`, dan `Year` beserta tombol **Add Book**.
- **Validasi Input Kosong**: Menampilkan dialog error `JOptionPane` (`"All fields must be filled!"`) apabila ada field yang belum diisi sebelum menambahkan baris baru ke tabel.
- **Reset Form Otomatis**: Mengosongkan kembali seluruh field input setelah data buku berhasil ditambahkan ke tabel.

---

## Teknologi yang Digunakan

- **Java (JDK 8+)** — menggunakan ekspresi lambda pada `ActionListener`
- **Java Swing & AWT** (`javax.swing.*`, `java.awt.*`)
- **Apache Maven** (`pom.xml`, groupId `org.example`, artifactId `TesJavaSwing`, versi `1.0-SNAPSHOT`, packaging `jar`)
- **JUnit `3.8.1`** (`test` scope) — `src/test/java/org/example/AppTest.java`

---

## Struktur Direktori

```text
Coba-lagi-git/
├── pom.xml
├── .gitignore
└── src/
    ├── main/
    │   └── java/
    │       └── org/example/
    │           ├── main/
    │           │   └── BookTable.java    # Entry point utama GUI Library Book List
    │           ├── adaapa/
    │           │   └── hai.java          # Kelas latihan tambahan
    │           ├── apam/
    │           │   └── halo.java         # Kelas latihan tambahan
    │           ├── obet/
    │           │   └── bet.java          # Kelas latihan tambahan
    │           └── test/
    │               └── apa.java          # Variasi percobaan UI Swing
    └── test/
        └── java/
            └── org/example/
                └── AppTest.java          # Unit test JUnit 3 dasar
```

---

## Persyaratan

- **Java Development Kit (JDK)** versi 8 atau lebih baru (`java` & `javac` tersedia di `PATH`)
- **Apache Maven** (`mvn` tersedia di `PATH`)

---

## Cara Build, Menjalankan Aplikasi, dan Testing

1. **Kompilasi project dengan Maven:**

   ```bash
   mvn compile
   ```

2. **Menjalankan aplikasi GUI (`BookTable`):**

   ```bash
   java -cp target/classes org.example.main.BookTable
   ```

3. **Menjalankan unit test (`AppTest.java`):**

   ```bash
   mvn test
   ```

4. **Membuat paket JAR (`target/TesJavaSwing-1.0-SNAPSHOT.jar`):**

   ```bash
   mvn package
   ```
