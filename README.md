# TUGAS PRA UTS ANALISIS JEJARING SOSIAL

## Identitas

- **Nama:** Fajar Pratama
- **NIM:** 2211310026
- **Program Studi:** Teknologi Informasi
- **Fakultas:** Teknik
- **Kelas:** 8A

---

# 1. Representasi Graf Jejaring Komunikasi

## Jenis Graf

- Graf bersifat **tak berarah (undirected graph)** karena komunikasi berlangsung dua arah.
- Graf **tidak berbobot** karena hanya menunjukkan ada atau tidaknya hubungan komunikasi.
- **Node:** anggota organisasi `(A, B, C, D, E)`
- **Edge:** hubungan komunikasi antar anggota.

## Hubungan Antar Anggota

- A-B
- A-C
- B-C
- B-D
- C-D
- D-E

## Matriks Adjacency

|   | A | B | C | D | E |
|---|---|---|---|---|---|
| A | 0 | 1 | 1 | 0 | 0 |
| B | 1 | 0 | 1 | 1 | 0 |
| C | 1 | 1 | 0 | 1 | 0 |
| D | 0 | 1 | 1 | 0 | 1 |
| E | 0 | 0 | 0 | 1 | 0 |

---

# 2. Perhitungan Centrality

## Rumus Degree Centrality

:contentReference[oaicite:0]{index=0}

## Hasil Perhitungan

| Node | Degree | Betweenness | Closeness | Eigenvector |
|------|---------|--------------|------------|--------------|
| A | 0.500 | 0.000 | 0.571 | 0.407 |
| B | 0.750 | 0.167 | 0.800 | 0.537 |
| C | 0.750 | 0.167 | 0.800 | 0.537 |
| D | 0.750 | 0.500 | 0.800 | 0.475 |
| E | 0.250 | 0.000 | 0.500 | 0.180 |

## Interpretasi

- Node **B** dan **C** memiliki **Degree Centrality** tertinggi sehingga menjadi anggota paling populer dalam jejaring.
- Node **D** memiliki **Betweenness Centrality** tertinggi sehingga berperan sebagai jembatan penghubung antar anggota.
- Node **B** dan **C** memiliki **Closeness Centrality** tinggi sehingga mampu menyebarkan informasi lebih cepat dibanding node lain.

---

# 3. Analisis Global Jejaring

## Hasil Analisis

- **Density = 0.600**
- **Diameter = 3**
- **Average Path Length = 1.500**

## Penjelasan

- **Density** menunjukkan tingkat keterhubungan jejaring. Nilai `0.6` menandakan hubungan antar anggota cukup padat.
- **Diameter** sebesar `3` berarti jarak komunikasi terjauh membutuhkan tiga langkah perpindahan.
- **Average Path Length** yang rendah menunjukkan komunikasi dalam organisasi relatif cepat.
- Jejaring cenderung memiliki karakteristik **small-world network** karena sebagian besar node dapat dijangkau dengan langkah pendek.
- Penyebaran informasi cukup efektif, namun masih bergantung pada beberapa anggota tertentu.

---

# 4. Eigenvector Centrality / PageRank

Eigenvector Centrality digunakan untuk mengukur tingkat pengaruh suatu node berdasarkan kualitas koneksinya, bukan hanya jumlah koneksi.

## Perbandingan dengan Degree Centrality

- **Degree Centrality** hanya menghitung banyaknya hubungan yang dimiliki node.
- **Eigenvector Centrality** mempertimbangkan apakah hubungan tersebut terhubung dengan node penting atau berpengaruh.

Artinya, seseorang tetap dapat memiliki pengaruh tinggi walaupun jumlah koneksinya sedikit apabila ia terhubung dengan anggota yang sangat berpengaruh.

---

# 5. Identifikasi Node Kunci dan Strategi Mitigasi

Berdasarkan seluruh metrik sentralitas, node yang paling penting adalah **B** dan **D**.

## Alasan

- Node **B** memiliki nilai Degree dan Closeness tinggi sehingga menjadi pusat komunikasi.
- Node **D** memiliki nilai Betweenness tinggi sehingga berperan sebagai penghubung antar kelompok.

## Strategi Mitigasi Organisasi

1. Membentuk jalur komunikasi alternatif agar tidak bergantung pada satu anggota.
2. Membagikan informasi melalui grup bersama.
3. Melakukan regenerasi kepengurusan dan pelatihan komunikasi.
4. Menyimpan dokumentasi kegiatan secara terpusat.
5. Membuat struktur koordinasi yang lebih merata.
