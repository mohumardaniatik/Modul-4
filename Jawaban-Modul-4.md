# Jawaban Tugas Modul 4

# 1.) 
Cara agar algoritma BFS (Breadth-First Search) menentukan node ke 8,6, dan 7 yaitu sebagai berikut:
1.	Pemilihan Node Awal: Algoritma BFS dimulai dengan memilih simpul awal dari graf. Dalam contoh kode di atas, simpul awal yang dipilih adalah `n3`. Oleh karena itu, BFS akan dimulai dari simpul `n3` dan   mencoba mencari jalur menuju simpul-simpul lain dalam graf.
2.	Penjelajahan Secara Bertahap: Algoritma BFS menjelajahi graf secara bertahap. Ini berarti bahwa simpul-simpul yang bertetangga dengan simpul saat ini akan dijelajahi terlebih dahulu sebelum melanjutkan    ke simpul-simpul lain yang lebih jauh. Hal ini dicapai dengan menggunakan antrian (queue) untuk memproses simpul-simpul.
3.	Penelusuran Jalur: Saat menjalankan BFS, setiap simpul memiliki atribut `distance` dan `predecessor`. Atribut `distance` mengindikasikan jarak dari simpul awal (`n3` dalam hal ini), dan atribut            `predecessor` mengindikasikan simpul sebelumnya dalam jalur yang mengarah ke simpul tersebut.
4.	Penemuan Node ke-8, 6, dan 7: Saat BFS dijalankan, algoritma akan mencari jalur terpendek dari simpul awal (`n3`) ke semua simpul lain dalam graf. Jadi, untuk menemukan simpul ke-8, 6, dan 7, berikut      adalah langkah-langkah yang diambil oleh algoritma:
    −	Simpul `n3` adalah simpul awal, jadi atribut `distance`-nya diatur ke `0`.
    −	Algoritma akan menjelajahi simpul-simpul yang bertetangga dengan `n3`, yaitu `n2` dan `n4`.
    −	Simpul `n2` adalah tetangga pertama, dan jaraknya adalah `1` dari `n3` (`n3 -> n2`).
    −	Selanjutnya, simpul `n4` juga adalah tetangga `n3`, dan jaraknya adalah `1` dari `n3` (`n3 -> n4`).
    −	Kemudian, algoritma akan menjelajahi tetangga-tetangga dari `n2` dan `n4`.
    −	Ini berlanjut hingga semua simpul dalam graf telah dijelajahi.
Jadi, pada akhirnya, algoritma akan menemukan simpul ke-8, 6, dan 7 dalam proses penelusuran BFS, dan atribut-atribut `distance` dan `predecessor` akan menunjukkan jalur terpendek dari `n3` ke ketiga simpul   tersebut.
Kesimpulannya, algoritma BFS akan menemukan jalur terpendek dari simpul awal (`n3`) ke semua simpul dalam graf, termasuk simpul ke-8, 6, dan 7, dan atribut-atribut dalam setiap simpul akan merekam jalur-      jalur ini.


# 2.) 
Cara algoritma BFS dapat menemukan node 5 yaitu sebagai berikut:
1.	Algoritma BFS dimulai dari simpul awal `n0` (dalam kode Anda). Anda menentukan simpul ini sebagai simpul awal yang akan digunakan untuk memulai pencarian.
2.	Simpul awal, yaitu `n0`, diberi warna GRAY untuk menunjukkan bahwa simpul ini telah dikunjungi. Selain itu, jarak dari simpul ini (dalam hal ini 0) dan pendahulu (null) juga dicatat.
3.	Simpul `n0` dimasukkan ke dalam antrian (queue).
4.	Algoritma BFS mulai menjalankan perulangan. Pada tahap ini, algoritma mengeluarkan simpul dari depan antrian, yang merupakan `n0`.
5.	Simpul `n0` adalah tetangga dari `n1` dan `n2`. Karena kedua simpul ini belum pernah dikunjungi (warna WHITE), mereka akan diberi warna GRAY, dan jarak serta pendahulu mereka akan diperbarui berdasarkan simpul `n0`.
−	n1` akan memiliki jarak 1 dari `n0` dan menjadi tetangga `n0`.
−	n2` akan memiliki jarak 1 dari `n0` dan menjadi tetangga `n0`.
6.	Simpul `n1` dan `n2` dimasukkan ke dalam antrian.
7.	Selanjutnya, algoritma mengeluarkan simpul dari depan antrian lagi, yang sekarang adalah `n1`.
8.	Algoritma kemudian memeriksa tetangga `n1`, yaitu `n0`, `n3`, dan `n4`. Namun, `n0` sudah memiliki warna GRAY, sehingga tidak ada perubahan yang terjadi. 
−	`n3` akan memiliki jarak 2 dari `n0` dan menjadi tetangga `n1`.
−	`n4` akan memiliki jarak 2 dari `n0` dan menjadi tetangga `n1`.
9.	Simpul `n3` dan `n4` dimasukkan ke dalam antrian.
10.	Proses ini berlanjut sampai seluruh graf telah dijelajahi. Pada saat BFS selesai, semua simpul yang bisa dicapai dari simpul awal `n0` akan memiliki warna BLACK, dan masing-masing simpul akan memiliki nilai jarak dan pendahulu yang sesuai.
Dalam konteks graf ini, simpul `n5` akan dicapai melalui beberapa langkah:
−	Simpul `n5` adalah tetangga dari `n4`.
−	Simpul `n4` adalah tetangga dari `n3`.
−	Simpul `n3` adalah tetangga dari `n1`.
−	Simpul `n1` adalah tetangga dari `n0`.
Sehingga, perjalanan dari `n0` ke `n5` adalah sebagai berikut:
1.	n0` -> 2. `n1` -> 3. `n3` -> 4. `n4` -> 5. `n5`
Jarak dari `n0` ke `n5` adalah 4 (0 -> 1 -> 2 -> 2 -> 1), dan `n4` adalah pendahulu langsung dari `n5`.
Ini adalah cara algoritma BFS menemukan simpul `n5` dalam graf yang diberikan. Algoritma BFS menjelajahi graf secara berlapis dan mencari jalur terpendek dari simpul awal ke simpul tujuan.


# 3.) 
Cara algoritma BFS dapat menemukan node 9 yaitu sebagai berikut:
1.	Awalnya, algoritma BFS dimulai dari simpul awal, yaitu `n1`.
2.	Simpul awal `n1` diwarnai GRAY, jaraknya diatur ke 0, dan tidak memiliki pendahulu.
3.	Simpul awal `n1` dimasukkan ke dalam antrian.
4.	Algoritma BFS akan memproses simpul-simpul dalam antrian dalam urutan yang sesuai.
5.	Pertama, `n1` yang saat ini ada dalam antrian diambil.
6.	Kemudian, algoritma akan memeriksa semua simpul yang terhubung dengan `n1`, yaitu `n3` dan `n4`.
7.	`n3` adalah simpul yang berwarna WHITE, yang berarti belum dijelajahi.
8.	Algoritma akan memproses `n3`:
   - `n3` akan diwarnai GRAY.
   - Jarak `n3` akan diatur menjadi 1 (jarak dari `n1`).
   - Pendahulu `n3` akan diatur menjadi `n1`.
   - `n3` dimasukkan ke dalam antrian.
9.	Kemudian, `n4` juga diwarnai GRAY, jaraknya diatur menjadi 1 (jarak dari `n1`), dan pendahulu diatur menjadi `n1`.
10.	Antrian sekarang berisi `n3` dan `n4`.
11.	Algoritma mengambil simpul pertama dari antrian, yaitu `n3`.
12.	Sekarang, algoritma akan memeriksa simpul yang terhubung dengan `n3`, yaitu `n1`, `n2`, dan `n4`. Namun, `n1` dan `n4` telah dijelajahi, sehingga satu-satunya simpul yang belum dijelajahi adalah `n2`.
13.	`n2` akan diwarnai GRAY, jaraknya diatur menjadi 2 (jarak dari `n1`), dan pendahulunya adalah `n3`.
14.	Setelah itu, `n3` diubah menjadi warna BLACK dan dikeluarkan dari antrian.
15.	Antrian sekarang berisi hanya `n4` dan `n2`.
16.	Algoritma mengambil simpul pertama dari antrian, yaitu `n4`.
17.	Namun, semua simpul yang terhubung dengan `n4` (yaitu `n1`, `n7`, `n8`) telah dijelajahi, jadi algoritma akan melanjutkan dengan mengambil `n2`.
18.	Algoritma akan memeriksa semua simpul yang terhubung dengan `n2`. Namun, `n1`, `n3`, dan `n4` telah dijelajahi. Satu-satunya simpul yang belum dijelajahi adalah `n5`.
19.	Algoritma akan memproses `n5`:
    - `n5` akan diwarnai GRAY.
    - Jarak `n5` akan diatur menjadi 3 (jarak dari `n1`).
    - Pendahulu `n5` akan diatur menjadi `n2`.
    - `n5` dimasukkan ke dalam antrian.
20.	Selanjutnya, `n2` diubah menjadi warna BLACK dan dikeluarkan dari antrian.
21.	Antrian sekarang hanya berisi `n4` dan `n5`.
22.	Proses di atas terus berlanjut sampai seluruh graf dieksplorasi.
23.	Ketika algoritma menemukan `n9`, maka itu juga akan diubah menjadi warna BLACK dan tidak dimasukkan lagi ke dalam antrian.
24.	Pada akhirnya, hasil pencarian BFS adalah mencetak simpul-simpul yang telah dijelajahi. Simpul `n9` akan tercetak bersama dengan simpul-simpul lain yang menjadi jalur dari `n1` ke `n9`, dan hasilnya akan menunjukkan jarak dari `n1` ke `n9`. Jadi, algoritma BFS akan menemukan `n9` dan menunjukkan bahwa jaraknya adalah 3 (melalui `n1`, `n2`, `n5`).


# 4.)
Cara algoritma BFS menemukan node C yaitu sebagai berikut:
1.	Inisialisasi node awal (start node) dan node target (node yang ingin Anda temukan). Dalam kasus ini, node awal adalah node 6 (n6), dan node target adalah node 3 (n3).
2.	Inisialisasi variabel penanda (flag) untuk menentukan apakah node 3 ditemukan. Misalnya, Anda dapat menggunakan variabel boolean dengan nilai awal "false".
3.	Lakukan langkah-langkah BFS mulai dari node awal (n6) sebagai berikut: a. Tandai node awal (n6) sebagai "GRAY" (sedang dijelajahi). b. Tandai jarak node awal (n6) sebagai 0. c. Tandai node awal (n6) sebagai node "sumber" atau node yang tidak memiliki pendahulu. d. Masukkan node awal (n6) ke dalam antrian (queue) BFS.
4.	Selama antrian BFS tidak kosong, lanjutkan dengan langkah-langkah berikut: 
a. Keluarkan node pertama dari antrian (node saat ini). 
b. Dapatkan semua node tetangga (node yang terhubung) dari node saat ini. 
c. Untuk setiap node tetangga:
•	Jika node tetangga adalah node target (n3), tandai bahwa node target ditemukan dan catat informasi yang diperlukan (jarak, pendahulu, dst.).
•	Jika node tetangga belum pernah dijelajahi (berwarna "WHITE"), tandai node tetangga sebagai "GRAY," catat jarak, dan tandai node tetangga sebagai anak dari node saat ini. Kemudian, tambahkan node tetangga ke antrian BFS. d. Setelah semua tetangga telah diperiksa, tandai node saat ini sebagai "BLACK" (selesai dijelajahi).
5.	Setelah BFS selesai, periksa apakah node target (n3) ditemukan dengan melihat apakah node n3 berubah warnanya menjadi "GRAY" selama proses BFS. Jika warnanya adalah "GRAY," itu berarti node 3 ditemukan; jika tidak, berarti tidak ditemukan.
