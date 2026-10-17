# Sistem-Rekomendasi-Film-Decision-Tree
Sistem rekomendasi film berdasarkan genre, usia tontonan, dan negara menggunakan algoritma Decision Tree, dilengkapi visualisasi pohon keputusan dan aturan prediksi.

## Deskripsi Proyek

Repository ini berisi implementasi sistem rekomendasi film menggunakan algoritma **Decision Tree Classifier** dengan bahasa pemrograman Python. Proyek ini dikembangkan untuk memenuhi tugas mata kuliah Struktur Data dan Algoritma pada Program Studi Sains Data, Universitas Negeri Surabaya.

Sistem memanfaatkan informasi film berupa genre, usia tontonan, negara, dan rating IMDb untuk membangun model klasifikasi yang menentukan apakah suatu film masuk ke dalam kategori rekomendasi atau tidak direkomendasikan.

Selain membangun model klasifikasi, proyek ini juga mengimplementasikan visualisasi pohon keputusan menggunakan Scikit-learn dan NetworkX agar struktur keputusan model dapat diamati secara visual.

## Tujuan Proyek

- Menerapkan algoritma Decision Tree dalam sistem rekomendasi film.
- Melakukan pembersihan dan preprocessing data film.
- Mengubah fitur kategorikal menjadi representasi numerik.
- Membentuk kategori rekomendasi berdasarkan rating IMDb.
- Memvisualisasikan struktur pohon keputusan dan aturan klasifikasi.
- Menghasilkan daftar film yang memenuhi kriteria rekomendasi berdasarkan input yang ditentukan.

## Dataset

Dataset yang digunakan adalah `LIST_GENRE_FILM_SDA.csv`, yang memuat informasi film dengan atribut berikut:

| Atribut | Keterangan |
|---|---|
| Judul Film | Nama film |
| Tahun | Tahun rilis film |
| Negara | Negara asal film |
| Rating IMDb | Rating film berdasarkan IMDb |
| Usia Tontonan | Kategori usia penonton |
| Genre | Genre atau kategori film |

## Metodologi

### 1. Data Cleaning
Data dibaca dari file CSV, kemudian dilakukan pembersihan untuk menangani rating yang tidak valid dan menyaring data berdasarkan kriteria yang ditetapkan dalam kode.

### 2. Feature Encoding
Fitur kategorikal seperti genre, negara, dan usia tontonan dikonversi menjadi kode numerik agar dapat digunakan oleh model Decision Tree.

### 3. Pembentukan Label Rekomendasi
Label target dibentuk berdasarkan rating IMDb:
- `1`: Rekomendasi, jika rating IMDb lebih dari 5,0.
- `0`: Tidak direkomendasikan, jika rating IMDb kurang dari atau sama dengan 5,0.

Dengan demikian, kategori rekomendasi merupakan label yang dibentuk dari aturan rating dalam proyek, bukan penilaian preferensi pengguna secara langsung.

### 4. Pemodelan Decision Tree
Model dibangun menggunakan `DecisionTreeClassifier` dari Scikit-learn dengan konfigurasi `max_depth=5`. Data dibagi menjadi data latih dan data uji, dengan model dilatih menggunakan bagian data latih.

### 5. Prediksi Rekomendasi Film
Sistem menyaring film berdasarkan genre, usia tontonan, dan negara yang ditentukan. Film yang memenuhi filter kemudian diproses menggunakan model untuk menghasilkan prediksi kategori rekomendasi.

### 6. Visualisasi Pohon Keputusan
Struktur pohon keputusan ditampilkan menggunakan dua pendekatan:
- `plot_tree` dari Scikit-learn.
- Visualisasi graf menggunakan NetworkX dengan struktur node dan edge.

Kode juga menyediakan fungsi untuk menampilkan aturan keputusan dalam bentuk teks.

## Konteks Akademik

Program Studi S1 Sains Data  
Universitas Negeri Surabaya

Mata Kuliah: Struktur Data dan Algoritmai film berdasarkan aturan yang dibangun dari dataset.
