---
title: Ajabar Boolean dan Gerbang Logika

---

# Aljabar Boolean & Gerbang Logika
## Aljabar boolean
Aljabar Boolean adalah sistem matematika untuk manipulasi variabel yang dapat memiliki salah satu dari dua nilai. 
* Dalam logika formal, nilai-nilai ini adalah "benar" dan "salah." 
* Dalam sistem digital, nilai-nilai ini adalah "nyala" dan "mati," 1 dan 0, atau "tinggi" dan "rendah." 

Ekspresi Boolean dibuat dengan melakukan operasi pada variabel Boolean.
Operator Boolean yang umum termasuk AND (AND), (OR), dan (NOT).

### Tujuan
* Memahami hubungan antara logika Boolean dan sirkuit komputer digital.
* Belajar cara merancang sirkuit logika sederhana.
* Memahami bagaimana sirkuit digital bekerja bersama-sama untuk membentuk sistem komputer yang kompleks.

### Manfaat dalam Pemrograman
Aljabar Boolean sering digunakan dalam pemrograman untuk mengevaluasi ekspresi logika.

### Macam-macam operator Aljabar Boolean
**Operator Biner:**
Aljabar Boolean memiliki dua operator biner:
Penjumlahan (+): Digunakan untuk operasi disjungsi (OR).
Perkalian (⋅): Digunakan untuk operasi konjungsi (AND).

**Operator Uner:**
Komplemen (’): Digunakan untuk menghasilkan nilai yang berlawanan dari suatu elemen. Misalnya, jika a = 1, maka a’ = 0, dan sebaliknya.

**Aksioma-Aksioma:**
Untuk setiap a, b, c ∈ B, berlaku aksioma-aksioma berikut:
Closure: a + b ∈ B dan a ⋅ b ∈ B.
Identitas: a + 0 = a dan a ⋅ 1 = a.
Komutatif: a + b = b + a dan a ⋅ b = b ⋅ a.
Distributif: a ⋅ (b + c) = (a ⋅ b) + (a ⋅ c) dan a + (b ⋅ c) = (a + b) ⋅ (a + c).
Komplemen: Untuk setiap a ∈ B, terdapat elemen unik a’ ∈ B sehingga a + a’ = 1 dan a ⋅ a’ = 0

### Contoh dalam pemrograman python
![Picture2](https://hackmd.io/_uploads/SJH3jLtJkg.png)


### Tabel kebenaran operator boolean
#### Aljabar boolean
* Sebuah operator Boolean dapat dijelaskan sepenuhnya menggunakan tabel kebenaran. 
* Tabel kebenaran untuk operator Boolean D (AND) dan (OR) seperti dibawah. 
* Operator AND  juga dikenal sebagai produk Boolean. Operator OR adalah jumlah Boolean..

![Picture1](https://hackmd.io/_uploads/HJaQjLFJyl.png)

### Boolean Algebra
* Tabel kebenaran untuk operator Boolean (NOT)ditunjukkan di sebelah kanan. 
* Operasi NOT paling sering dilambangkan dengan garis atas. 

![Picture3](https://hackmd.io/_uploads/H1zLhItyJl.png)

* Sebuah fungsi Boolean memiliki: 
Setidaknya satu variabel Boolean, 
Setidaknya satu operator Boolean, dan 
Setidaknya satu input dari himpunan {0,1}. 
* Fungsi ini menghasilkan output yang juga merupakan anggota dari himpunan {0,1}.
* Tabel kebenaran untuk fungsi Boolean. : 
   
![Picture4](https://hackmd.io/_uploads/H1JypLtyyg.png)

ditunjukkan sebelah kanan. Untuk mempermudah evaluasi fungsi Boolean, tabel kebenaran berisi kolom tambahan (diarsir) untuk menyimpan evaluasi dari bagian-bagian subfungsi.

![Picture5](https://hackmd.io/_uploads/Hy3b6ItJ1e.png)

* Sebagian besar identitas Boolean memiliki bentuk AND (perkallian) serta bentuk OR (jumlah). Kami menyajikan identitas kami menggunakan kedua bentuk tersebut. 

![Picture6](https://hackmd.io/_uploads/HkDLaUKkyg.png)

* Kelompok kedua

![Picture7](https://hackmd.io/_uploads/SyTKpLFk1x.png)

* Kelompok 3 

![Picture8](https://hackmd.io/_uploads/rkkA6LtJ1g.png)

* Terkadang, lebih ekonomis membangun sirkuit dengan menggunakan komplemen fungsi dan mengkomplementasi hasilnya dibandingkan mengimplementasikan fungsi secara langsung. Hukum DeMorgan memudahkan penemuan komplemen dari fungsi Boolean, yang menyatakan: 

![Picture9](https://hackmd.io/_uploads/ByxECItkJx.png)

## Gerbang Logika

* Fungsi Boolean diimplementasikan dalam sirkuit komputer digital yang disebut gerbang (gates). 
* Gerbang adalah perangkat elektronik yang menghasilkan hasil berdasarkan dua atau lebih nilai input. 
* Dalam kenyataannya, gerbang terdiri dari satu hingga enam transistor, tetapi desainer digital menganggapnya sebagai satu kesatuan. 
* Sirkuit terintegrasi mengandung kumpulan gerbang yang sesuai untuk tujuan tertentu.
* Tiga gerbang AND, OR, dan  NOT.

![Picture10](https://hackmd.io/_uploads/SJjlyvtJkx.png)

* Gerbang yang sangat berguna lainnya adalah gerbang eksklusif OR (XOR).  
* Output dari operasi XOR adalah benar hanya ketika nilai-nilai input berbeda.

![Picture11](https://hackmd.io/_uploads/BJQBJwFJyl.png)
