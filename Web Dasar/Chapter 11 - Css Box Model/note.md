Mengenali tabiat dasar alami suatu elemen web dan teknik membelokkan sifatnya, serta taktik mengurus isi konten yang tumpah-ruah dari wadahnya.

Tag <div> vs <span>: Menggali inti perbedaan antara ras elemen Block (sifatnya egois, mengambil seluruh baris) melawan ras elemen Inline (sifatnya toleran, hanya menghabiskan ruang sebesar teksnya).
Properti display:
block: Sanggup mematuhi instruksi dimensi (height & width).
inline: Menolak instruksi dimensi, serta pengaturan margin secara vertikal akan kacau.
inline-block: Genetik buatan gabungan (Berjejer sopan layaknya elemen inline, namun dengan dimensi solid seperti block).
Intrinsic vs Extrinsic Sizing: Perbedaan antara elemen yang mengukur badannya sendiri secara alami berdasarkan isi konten (intrinsic), dibandingkan memaksanya dengan ukuran tetap dari luar (extrinsic).
Overflow: Mengatasi teks/gambar yang membludak keluar menggunakan perintah visible (biarkan), hidden (tebang yang tumpah), scroll (pasang gulungan), atau auto.


Overview
Pembedahan anatomi utama yang biasa disebut "The CSS Box Model".

Anatomi Kotak: Mengupas 4 lapisan penyusun wujud semua elemen:
Content: Daging utama (tempat tulisan atau gambar bersemayam).
Padding: Dinding rongga empuk transparan di dalam rumah.
Border: Pagar atau garis yang membatasi wilayah.
Margin: Area transparan penolak tetangga di luar pagar.
Karakteristik Margin: Punya kelebihan bisa diisi angka negatif (untuk efek elemen bertumpuk) dan keajaiban nilai auto (rahasia jadul untuk mendorong kotak persis ke titik tengah layar).
Karakteristik Padding: Jarak napas untuk memperluas ruangan dari dalam, haram menggunakan angka negatif.
3D Box Model Visualizer:
tools.belajarwebdev.

Menegaskan pagar pembatas, serta menyelesaikan isu historis di mana browser selalu salah menghitung lebar elemen yang sebenarnya.

Border: Mengombinasikan width (tebal), style (solid/titik/putus-putus), dan color untuk mempercantik batas luar elemen.
Outline: Pagar bayangan. Mirip border, namun ia melayang dan tidak memakan kapasitas ukuran ruangan di sekitarnya.
Perhitungan Dimensi Klasik: Mengungkap bahwa jika kalian memesan kotak selebar 100px, aslinya kotak kalian akan melebar jauh lebih besar akibat tambahan padding dan border.
Box Sizing (border-box): Mantra pengubah segalanya di era CSS modern. Memerintahkan box-sizing: border-box agar dimensi padding dan border disusutkan merangsek ke dalam. Lebar pesanan kalian akan tetap absolut, tak peduli setebal apa pagarnya.






