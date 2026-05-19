# UTS Analisis Jejaring Sosial

## Data Mahasiswa
- **Nama:** Mohammad Agung Permana
- **NIM:** 2211310040

## Repository GitHub
https://github.com/ladung-pembalab/uts-ladung-jejaringsosial

---

# Analisis Pola Komunikasi Organisasi Kemahasiswaan

Dalam organisasi kemahasiswaan, hubungan komunikasi antaranggota dapat dianalisis menggunakan pendekatan Social Network Analysis (SNA). Setiap anggota direpresentasikan sebagai node, sedangkan hubungan komunikasi direpresentasikan sebagai edge.

Graf yang digunakan termasuk graf tak berarah karena komunikasi berlangsung dua arah. Selain itu, graf tidak berbobot karena hubungan hanya menunjukkan keberadaan interaksi.

## Matriks Adjacency

|   | A | B | C | D | E |
|---|---|---|---|---|---|
| A | 0 | 1 | 1 | 0 | 0 |
| B | 1 | 0 | 1 | 1 | 0 |
| C | 1 | 1 | 0 | 1 | 0 |
| D | 0 | 1 | 1 | 0 | 1 |
| E | 0 | 0 | 0 | 1 | 0 |

## Analisis Centrality

Node B, C, dan D memiliki nilai degree centrality tertinggi sehingga menjadi anggota yang paling aktif dalam komunikasi organisasi. Node D memiliki betweenness centrality tertinggi sehingga berperan sebagai penghubung utama dalam jaringan.

Nilai closeness centrality menunjukkan bahwa node B, C, dan D mampu menyebarkan informasi dengan lebih cepat dibanding anggota lainnya.

## Analisis Jejaring

Nilai density jaringan sebesar 0,6 menunjukkan bahwa hubungan komunikasi dalam organisasi cukup baik. Diameter graf bernilai 3 dengan average path length sekitar 1,6.

Karakteristik jejaring termasuk small-world network karena sebagian besar anggota dapat terhubung melalui jalur yang relatif pendek.

## Eigenvector Centrality

Node B dan C memiliki nilai eigenvector centrality tertinggi. Hal tersebut menunjukkan bahwa keduanya memiliki pengaruh besar karena terhubung dengan anggota yang juga memiliki posisi penting dalam jaringan.

## Kesimpulan

Analisis jejaring sosial membantu organisasi memahami pola komunikasi antaranggota. Dengan mengetahui node yang paling berpengaruh, organisasi dapat menyusun strategi komunikasi yang lebih efektif dan mengurangi ketergantungan terhadap anggota tertentu.
