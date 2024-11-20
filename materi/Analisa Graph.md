---
title: Analisa Graph

---

# Analisa Graph
## Social Network Analysis
***Social Network Analysis*** merupakan bidang kajian yang mengekplorasitentang hubungan manusia dengan menggunakan teori graf. Implementasi *Social Network Analysis* dapat menjelaskan relasi atau hubungan antar aktor melalui visualisasi berbentuk graf. Relasi dalam analisis jaringan sosial dapat diproses dalam bentuk perhitungan yang disebut centrality dalam sebuah jaringan sosial sesuai dengan posisi masing-masing aktor di dalam struktur jaringan tersebut.

**Social network** 
terdapat node yang mewakili 
orang atau individu atau aktor. Relasi  antar objek  dapat dinyatakan dengan link atau edges yang terjadi antara aktor tersebut Social network terdiri dari banyak aktor yang mempunyai relasi satu sama lain hingga membentuk peta jaringan sosial yang dinyatakan dengan graph.

**Graph** :

![Gambar1](https://hackmd.io/_uploads/Hkg41vDfyg.png)

**Tabel** : 

| Node |  1   |  2   |  3  |  4  |  5  |  6  |  7  |  8  |  9  |
|:----:|:----:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|  **1**   |   -   | 1     |   1  |    1 |   0  |  0   |    0 |   0  |   0  |
|   **2**   |  1    | -     |  1   | 0    | 0    | 0    |  0   |  0   |   0  |
|    **3**  |   1   |  1    |  -   |  1   |  0   | 0    |  0   |   0  |   0  |
|     **4** |  1    | 0     |  1   |  -   |  1   |  1   |  0   |  0   |   0  |
|   **5**   |   0   |  0    |  0   |  1   |  -   |  1   |  1   |  1   |  0   |
|    **6**  |   0   |   0   |   0  |  1   |  1   |  -   |   1  |   1  |   0  |
|     **7** |   0   |  0    |   0  |   0  |  1   |  1   |  -   | 1    |  1   |
|     **8**|   0   |  0    |  0   |   0  |  1   |  1   |  1   |  -   |  0   |
| **9** | 0 | 0 |  0   |  0   |   0  |   0  |  1   | 0    |  -   |

***NB :***
* Tidak semua node dalam jaringan adalah penting  (aktor)
* Mencari node yang paling penting dalam suatu jaringan

## Centrality
**Centrality** adalah penentuan aktor menggunakan ukuran pada Social Network Centrality dalam teori graf dan social network. Dibagi menjadi empat jenis, yaitu :
1. Degree Centrality 
2. Betweeness Centrality
3. Closeness Centrality 
4. Eigenvector Centrality

## 1. Degree Centrality
* **Degree centrality** adalah jumlah edge yang terkoneksi pada suatu node yang mewakili interaksi.
* Pentingnya node ditentukan oleh jumlah node yang berdekatan dengan node tersebut.
    * Lebih besar derajatnya (degree), maka lebih penting node itu dalam suatu jaringan.
    * Hanya sebagian kecil node yang memiliki derajat tinggi dalam jaringan.
* **Degree centrality :** ![Gambar2](https://hackmd.io/_uploads/HyQ0UvvGyg.png)
* **Normalisasi Degree centrality :** ![Gambar3](https://hackmd.io/_uploads/B1GxPvwzJg.png)

![Gambar1](https://hackmd.io/_uploads/HyQfwDPGyl.png)
Untuk  node 1, degree centrality adalah 3 dan Normalisasi degree centrality adalah 3/(9-1)=3/8.

### Code

```
import networkx as nx
G = nx.Graph([(0, 1), (0, 2), (0, 3), (1, 2), (1, 3)])
dg = nx.degree_centrality(G)

dg
```
**Output**
`{0: 1.0, 1: 1.0, 2: 0.6666666666666666, 3: 0.6666666666666666}`

```
import networkx as nx
G = nx.Graph([(9, 7), (7, 8), (7, 5), (7, 6), (8, 5), (8, 6), (5, 6), (5, 4), (6, 4), (4, 3), (4, 1), (3, 1), (3, 2), (2, 1)])
dg = nx.degree_centrality(G)
pos = nx.spring_layout(G)

nx.draw_networkx(G, pos = pos, with_labels=True,node_size=300)
```
**Output**
![21](https://hackmd.io/_uploads/rkD7kVOMyl.png)

## 2. Betweeness Centrality
***Betweeness Centrality*** merupakan suatu ukuran ( Persamaan (10) ) yang menunjukkan seberapa besar kemampuan suatu node dalam mengendalikan aliran informasi antara node-node lain dalam jaringan.

Skor betweeness Centrality mewakili seberapa besar informasi yang tersebar dari suatu aktor. Semakin besar skor, artinya aktor tersebut semakin berperan dalam penyebaran informasi.

Semakin banyak lintasan yang harus melewati persimpangan itu (misal tidak ada jalan alternatif), maka semakin penting arti persimpangan tersebut. Hal ini menandakan seberapa besar suatu node diperlukan sebagai penghubung dalam penyebaran informasi di dalam jaringan.

Ukuran ini juga dapat digunakan untuk mengidentifikasi boundary spanners, yaitu orang atau node yang berperan sebagai penghubung (jembatan) antara dua komunitas.

* Menghitung jumlah lintasan terpendek yang melewati suatu node.
* Node dengan  betweenness  tinggi  adalah  penting dalam komunikasi dan penyebaran informasi.
* Normalisasi Betweenness Centrality : 

    ![Gambar7](https://hackmd.io/_uploads/S1HvcPPMkx.png)

* Betweenness Centrality

    ![Gambar4](https://hackmd.io/_uploads/ryHcKwvMke.png)

    ![Gambar5](https://hackmd.io/_uploads/rkPsFPvG1e.png)
    ![Gambar6](https://hackmd.io/_uploads/rJj3YPDM1l.png)

## 3. Closeness Centrality
***Closenes centrality*** adalah nilai kedekatan antara satu node dengan node lain dalam jaringan dengan menghitung rata-rata dari jarak relasi node-node tersebut. Skor closeness centrality mewakili kecepatan dalam penyebaran informasi.
* **Average Distance :** ![Gambar8](https://hackmd.io/_uploads/B1AQswPMJl.png)

* **Closeness Centrality :** ![Gambar9](https://hackmd.io/_uploads/S1B4sDvMke.png)

### Contoh Closeness Centrality

![Cuplikan layar 2024-11-17 195430](https://hackmd.io/_uploads/By1ciwwfJg.png)

## 4. Eigenvector Centrality
***Eigenvector Centrality*** adalah ukuran pengaruh sebuah node pada jaringan. Jika suatu node ditunjuk oleh banyak node (yang juga mempunyai sentralitas vektor eigen yang tinggi) maka node tersebut akan mempunyai sentralitas vektor eigen yang tinggi.

## Referensi
1. https://en.wikipedia.org/wiki/Eigenvector_centrality#:~:text=Eigenvector%20centrality%20is%20a%20measure,will%20have%20high%20eigenvector%20centrality.
2. https://www.sciencedirect.com/topics/computer-science/betweenness-centrality