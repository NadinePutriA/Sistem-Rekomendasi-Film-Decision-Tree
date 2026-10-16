# Sistem-Rekomendasi-Film-Decision-Tree
Sistem rekomendasi film berdasarkan genre, usia tontonan, dan negara menggunakan algoritma Decision Tree, dilengkapi visualisasi pohon keputusan dan aturan prediksi.


**Sistem Rekomendasi Film Menggunakan Decision Tree**

**Deskripsi Proyek**

Proyek ini merupakan implementasi sistem rekomendasi film menggunakan algoritma Decision Tree dengan bahasa pemrograman Python. Sistem memanfaatkan informasi genre, usia tontonan, negara asal, dan rating IMDb untuk menghasilkan prediksi apakah suatu film termasuk kategori rekomendasi atau tidak direkomendasikan.

Selain membangun model klasifikasi, proyek ini juga menampilkan visualisasi pohon keputusan menggunakan Scikit-learn dan NetworkX serta menerjemahkan aturan keputusan ke dalam bentuk yang lebih mudah dipahami.

**Tujuan**

1. Menerapkan algoritma Decision Tree untuk klasifikasi rekomendasi film.
2. Mengolah dan membersihkan data film sebelum digunakan dalam pemodelan.
3. Mengubah atribut kategorikal menjadi representasi numerik.

**Dataset**

Dataset yang digunakan adalah LIST_GENRE_FILM_SDA.csv, yang berisi informasi film dengan atribut berikut:
- Judul Film : Nama Film
- Tahun : Tahun rilis film
- Negara : Negara asal film
- Rating IMDb : Nilai rating film dari IMDb
- Usia Tontonan : Kategori usia penonton
- Genre : Genre atau kategori film


**Metodologi**

**1. Data Loading dan Cleaning**

Data dibaca menggunakan library CSV dan Pandas. Tahap pembersihan meliputi konversi rating IMDb menjadi numerik, penghapusan data dengan rating tidak valid, serta penyaringan beberapa nilai genre dan kategori usia tontonan.

**2. Penentuan Label Rekomendasi**

Label target dibuat berdasarkan rating IMDb:
- Rekomendasi (1): rating IMDb lebih dari 5,0.
- Tidak direkomendasikan (0): rating IMDb kurang dari atau sama dengan 5,0.

**3. Encoding Atribut**

Atribut genre, usia tontonan, dan negara diubah menjadi kode numerik agar dapat digunakan sebagai fitur dalam model Decision Tree.

**4. Pemodelan Decision Tree**

Model dibangun menggunakan DecisionTreeClassifier dari Scikit-learn dengan max_depth=5. Fitur yang digunakan adalah genre, usia tontonan, dan negara yang telah di-encoding.

**5. Prediksi dan Penyaringan Film**

Sistem menggunakan kombinasi genre, usia tontonan, dan negara sebagai kriteria penyaringan film. Model kemudian memprediksi kategori rekomendasi untuk film yang sesuai dengan kriteria tersebut.

Film yang diprediksi sebagai rekomendasi disimpan ke dalam file film_rekomendasi.csv.

**6. Visualisasi dan Interpretasi**

Visualisasi dan interpretasi model dilakukan melalui:
- Visualisasi pohon keputusan menggunakan Scikit-learn.
- Penerjemahan aturan keputusan ke dalam bahasa yang lebih mudah dipahami.
- Visualisasi struktur pohon keputusan menggunakan NetworkX.

**Konteks Akademik**

Proyek mata kuliah Struktur Data dan Algoritma (SDA).
Program Studi Sains Data
Universitas Negeri Surabaya

**Catatan**

Model dalam proyek ini mempelajari label rekomendasi yang dibentuk dari rating IMDb, bukan dari penilaian preferensi pengguna secara langsung. Karena itu, hasilnya lebih tepat dipahami sebagai klasifikasi film berdasarkan aturan yang dibangun dari dataset.
