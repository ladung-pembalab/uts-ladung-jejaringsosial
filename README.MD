# UTS Analisis Jejaring Sosial (Social Network Analysis)

## Identitas Mahasiswa

* **Nama:** Mohammad Agung Permana
* **NIM:** 2211310040

## Repository GitHub

🔗 https://github.com/ladung-pembalab/uts-ladung-jejaringsosial

---

# Analisis Jejaring Sosial pada Organisasi Kemahasiswaan

## Pendahuluan

Komunikasi merupakan salah satu aspek penting dalam keberlangsungan organisasi kemahasiswaan. Penyebaran informasi yang tidak merata dapat menyebabkan terjadinya hambatan koordinasi antaranggota organisasi. Dalam kondisi tertentu, terdapat anggota yang memiliki pengaruh besar dalam penyebaran informasi, sedangkan anggota lain cenderung pasif dan hanya menerima informasi dari pihak tertentu saja.

Untuk memahami pola komunikasi tersebut digunakan metode Social Network Analysis (SNA). Metode ini digunakan untuk menganalisis hubungan sosial antaranggota organisasi berdasarkan pola interaksi yang terjadi.

---

# 1. Representasi Graf Jejaring Organisasi

Pada analisis ini, setiap anggota organisasi direpresentasikan sebagai node (simpul), sedangkan hubungan komunikasi direpresentasikan sebagai edge (sisi).

Graf yang digunakan termasuk graf tak berarah (undirected graph), karena komunikasi dianggap berlangsung dua arah. Selain itu, graf juga bersifat tidak berbobot (unweighted) sebab hubungan hanya menunjukkan adanya interaksi tanpa memperhatikan intensitas komunikasi.

## Representasi Anggota

* A = Ketua
* B = Wakil Ketua
* C = Sekretaris
* D = Bendahara
* E = Anggota

## Hubungan Antaranggota

* A terhubung dengan B dan C
* B terhubung dengan A, C, dan D
* C terhubung dengan A, B, dan D
* D terhubung dengan B, C, dan E
* E terhubung dengan D

## Matriks Adjacency

|   | A | B | C | D | E |
| - | - | - | - | - | - |
| A | 0 | 1 | 1 | 0 | 0 |
| B | 1 | 0 | 1 | 1 | 0 |
| C | 1 | 1 | 0 | 1 | 0 |
| D | 0 | 1 | 1 | 0 | 1 |
| E | 0 | 0 | 0 | 1 | 0 |

Matriks adjacency menunjukkan hubungan komunikasi langsung antaranggota organisasi. Nilai 1 menunjukkan adanya hubungan komunikasi, sedangkan nilai 0 menunjukkan tidak adanya hubungan langsung.

---

# 2. Analisis Degree, Betweenness, dan Closeness Centrality

Centrality digunakan untuk mengetahui tingkat kepentingan suatu node dalam jaringan komunikasi organisasi.

## Hasil Perhitungan

| Node | Degree | Betweenness | Closeness |
| ---- | ------ | ----------- | --------- |
| B    | 3      | 0.33        | 0.80      |
| C    | 3      | 0.33        | 0.80      |
| D    | 3      | 0.50        | 0.80      |
| A    | 2      | 0.00        | 0.57      |
| E    | 1      | 0.00        | 0.50      |

## Degree Centrality

Degree centrality digunakan untuk mengukur jumlah hubungan langsung yang dimiliki setiap anggota.

Node B, C, dan D memiliki nilai degree tertinggi sehingga dapat dikatakan sebagai anggota yang paling aktif dalam komunikasi organisasi.

## Betweenness Centrality

Betweenness centrality digunakan untuk mengetahui node yang berperan sebagai penghubung dalam jaringan.

Node D memiliki nilai betweenness tertinggi karena menjadi jalur utama komunikasi antara anggota inti dengan anggota E.

## Closeness Centrality

Closeness centrality digunakan untuk mengukur kemampuan suatu node dalam menjangkau node lain dengan cepat.

Node B, C, dan D memiliki nilai closeness tertinggi sehingga lebih efektif dalam menyebarkan informasi dibandingkan anggota lainnya.

---

# 3. Analisis Density, Diameter, dan Average Path Length

## Density

Jumlah node = 5
Jumlah edge = 6

```math
Density = 2m / n(n-1)
         = 2(6) / 5(4)
         = 0.6
```

Nilai density sebesar 0,6 menunjukkan bahwa hubungan komunikasi antaranggota organisasi tergolong cukup baik.

## Diameter

Diameter jaringan bernilai 3 karena jalur komunikasi terjauh berada antara node A dan E.

## Average Path Length

Average path length bernilai sekitar 1,6 yang menunjukkan bahwa rata-rata jarak antaranggota relatif pendek.

## Karakteristik Jejaring

Jejaring komunikasi organisasi termasuk kategori small-world network karena sebagian besar anggota dapat saling terhubung melalui jalur yang singkat.

Implikasinya:

* Penyebaran informasi berlangsung lebih cepat.
* Koordinasi organisasi menjadi lebih efektif.
* Ketergantungan terhadap anggota tertentu masih cukup tinggi.

---

# 4. Eigenvector Centrality

Eigenvector centrality digunakan untuk mengukur tingkat pengaruh suatu node berdasarkan kualitas hubungan yang dimiliki.

## Hasil Perhitungan

| Node | Eigenvector Centrality |
| ---- | ---------------------- |
| B    | 0.58                   |
| C    | 0.58                   |
| D    | 0.52                   |
| A    | 0.32                   |
| E    | 0.18                   |

Node B dan C memiliki nilai eigenvector tertinggi karena keduanya terhubung dengan anggota yang memiliki pengaruh besar dalam organisasi.

Berbeda dengan degree centrality yang hanya menghitung jumlah koneksi, eigenvector centrality juga mempertimbangkan kualitas hubungan yang dimiliki node.

---

# 5. Identifikasi Node Kunci dan Strategi Mitigasi

Berdasarkan seluruh hasil analisis, node B dan D merupakan node yang memiliki peran penting dalam organisasi.

## Node B

Memiliki tingkat koneksi yang tinggi serta pengaruh besar dalam komunikasi organisasi.

## Node D

Berfungsi sebagai penghubung utama antaranggota organisasi.

## Strategi Mitigasi

1. Membagi tanggung jawab komunikasi kepada beberapa anggota.
2. Meningkatkan koordinasi antarbidang.
3. Membuat dokumentasi organisasi secara terpusat.
4. Melaksanakan regenerasi kepemimpinan.
5. Memberikan pelatihan komunikasi kepada anggota baru.

## Kesimpulan

Social Network Analysis dapat digunakan untuk memahami pola komunikasi dalam organisasi kemahasiswaan. Dengan mengetahui node yang memiliki pengaruh besar, organisasi dapat meningkatkan efektivitas komunikasi serta mengurangi risiko hambatan koordinasi apabila anggota tertentu tidak aktif.


## Kesimpulan

Analisis jejaring sosial membantu organisasi memahami pola komunikasi antaranggota. Dengan mengetahui node yang paling berpengaruh, organisasi dapat menyusun strategi komunikasi yang lebih efektif dan mengurangi ketergantungan terhadap anggota tertentu.
