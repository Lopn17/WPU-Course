Cascade

Membedah algoritma pertama penamaan CSS, yaitu "Air Terjun" (Cascade). Bagaimana jika ada dua aturan CSS yang memberi perintah berbeda pada satu tombol yang sama? Siapa yang menang?

Position and Order of Appearance: Prinsip membaca dari atas ke bawah. Instruksi yang ditulis paling belakangan akan menimpa instruksi di atasnya.
Origin (Asal Aturan): Mengenali tiga hierarki hukum asal mula sebuah gaya diciptakan:
User Agent Styles: Gaya kodrat bawaan browser (alasan mengapa link secara ajaib selalu berwarna biru di komputer mana pun).
Local User Styles: Gaya modifikasi pengguna browser (seperti saat fitur mode malam/dark mode diaktifkan).
Authored CSS: Gaya yang baru saja kalian ketik mati-matian.
Importance (!important): Menggunakan "bom atom" bernama !important. Kita akan pelajari kapan dia bisa menyelamatkan proyek, dan kapan dia justru menghancurkan sistem hierarki kalian.

Specificity
Ini adalah game "Adu Kuat Skor" dari setiap Selector yang ada. Jika metode Cascade melihat urutan baris, Specificity murni melihat kekuatan bobot dari siapa yang dipanggil.

Konsep Spesifisitas: Pemilih yang sangat spesifik dan detail tidak akan bisa dikalahkan oleh pemilih yang generik, meskipun si generik berada di baris paling bawah.
Sistem Perhitungan (Kalkulator Spesifisitas): Kita akan berlatih layaknya matematika, menghitung bobot dengan struktur nilai 0 0 0 0:
1000 Poin: Inline Style (Paling kuat, disisipkan langsung di dalam tag HTML).
100 Poin: ID (#id).
10 Poin: Class, Pseudo-class, dan Attribute (.class, :hover, dll).
1 Poin: Tag dasar dan Pseudo-element (h1, p, ::before).
0 Poin: Wildcard (*) atau Combinators.
Latihan Menghitung: Menguji nalar kita dengan mengadu bentrokan nilai (misalnya: bentrok antara skor 0-0-1-1 melawan 0-0-0-2). Saya juga akan perlihatkan alat bantu (kalkulator specificity) di internet.
Kalkulator Specificity:
https://specificity.keegan.st/

Inheritance

Konsep "Harta Warisan" elemen web. Mari kita pelajari bagaimana elemen induk (Parent) mewariskan beberapa sifat bawaannya kepada elemen anaknya (Child).

Definisi Pewarisan: Fenomena menurunnya properti (jika warna latar/huruf elemen bungkus luar diubah, maka kotak paragraf di dalamnya otomatis akan mengikuti).
Properti yang Diwariskan vs Tidak: Kalian harus hafal sifat mana yang menurun (color, font-family, teks), dan sifat mana yang tidak mungkin menurun otomatis (border, margin, padding).
Kata Kunci inherit: Kita akan bereksperimen dengan perintah inherit, untuk memaksa sebuah elemen merengek dan meniru 100% karakter induknya (biasanya dipakai untuk mengalahkan gaya User Agent browser).
