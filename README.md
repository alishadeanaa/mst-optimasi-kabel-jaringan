# 🌐 Optimasi Jaringan Internet Antar SMA di 3 Kota Menggunakan Minimum Spanning Tree (MST)

Proyek ini bertujuan untuk mengoptimalkan pemasangan kabel jaringan internet antar Sekolah Menengah Atas (SMA) di tiga kota di Indonesia: **Wonosobo, Surabaya, dan Sidoarjo**. Optimasi dilakukan dengan mencari **Minimum Spanning Tree (MST)** dari graf jaringan sekolah, menggunakan tiga algoritma graf populer:

- **Prim's Algorithm**
- **Kruskal's Algorithm**
- **Borůvka's Algorithm**

---

## 🎯 Tujuan Proyek

- Menentukan **rute koneksi jaringan terpendek** untuk menyambungkan semua sekolah di masing-masing kota.
- Menganalisis **kinerja masing-masing algoritma MST** berdasarkan ukuran dan kepadatan graf (jumlah vertex dan edge).
- Memberikan **rekomendasi algoritma terbaik** sesuai kondisi tiap kota.

---

## 📊 Hasil Analisis Performa Algoritma

| Kota      | Jumlah Sekolah | Algoritma Unggul | Penjelasan                                                                 |
|-----------|----------------|------------------|---------------------------------------------------------------------------|
| Wonosobo | 17             | **Prim**         | Ukuran graf kecil membuat penggunaan adjacency list dan heap sangat efisien. |
| Surabaya | 132            | **Kruskal (waktu)** / **Prim (ruang)** | Kruskal unggul dari segi kecepatan eksekusi, sedangkan Prim efisien dalam penggunaan ruang pada graf besar. |
| Sidoarjo | 64             | **Kruskal**       | Penggunaan ruang dan waktu lebih efisien karena struktur daftar sisi lebih sederhana. |

---

## 🧠 Rekomendasi Penggunaan Algoritma

- **Graf kecil (≤ 20 vertex)** → Gunakan **Prim**, karena efisien baik dari sisi ruang maupun waktu.
- **Graf menengah (20–100 vertex)** → Gunakan **Kruskal**, karena sorting daftar sisi lebih optimal di ukuran ini.
- **Graf besar (≥ 100 vertex)**:
  - **Prim** unggul dalam efisiensi ruang (terutama bila menggunakan adjacency list).
  - **Kruskal** lebih cepat dalam eksekusi (sorting edge list).
- **Graf sangat padat** → Pertimbangkan menggunakan **Prim dengan adjacency matrix**, karena traversal heap lebih efisien untuk banyak koneksi antar simpul.

📌 *Kesimpulan*: Pemilihan algoritma harus mempertimbangkan **jumlah vertex**, **kepadatan graf**, dan **kebutuhan ruang/waktu** di setiap kota.


