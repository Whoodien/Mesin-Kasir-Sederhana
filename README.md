# Mesin-Kasir-Sederhana
Program mesin kasir sederhana ini merupakan tugas asistensi praktikum dasar pemrograman ITS dengan kode P1. Program ini menggunakan input dari user agar dapat bekerja

## Input dan Output
Program ini bergantung kepada input yang dimasukkan oleh pengguna yang dimana berupa berapa banyak jenis barang yang ada, nama barang, banyak barang, harga barang, dan diskon yang berlaku. Output dari kode ini akan menampilkan jenis barang, berapa banyak barang yang dibeli, harga, harga sebelum diskon, serta harga setelah ada diskon.

## Isi Pemrograman Secara Singkat
Mendefinisikan konstanta yang disebut (MAX_ITEMS) yang berupa item maksimal yang bisa ditampilkan. Mendefinisikan sebuah struktur baru yaitu (Item) yang memiliki tiga atribut yaitu nama, harga, dan jumlah. Membuat semacam deklarasi struk yang akan dibuat, disini akan menerima nama dari item (menggunakan array), jumlah item (count), dan juga diskon yang akan diberikan. Menginisialisasi sebuah variabel total untuk menyimpan total harga, serta menginisialisasi sebuah loop untuk setiap item (i). Menambahkan sebuah subtotal dan menghitung harga subtotal untuk setiap harga sebuah item dikalikan dengan banyaknya item yang akan dibeli, lalu menambahkan subtotal ke total keseluruhann. Tentukan apakah ada diskon atau tidak dengan fungsi if else.

Lalu masuk ke dalam fungsi main. Pada fungsi main akan mengprint suatu kalimat yang menyuruh pengguna untuk memasukkan berapa jenis barang yang mereka punya. Di sini akan terdapat loop sesuai dengan berapa banyak jenis barang yang pengguna masukkan. Pada fungsi ini juga pengguna di minta untuk memasukkan besar diskon. Ketika hal - hal diatas baris kode nya selesai di eksekusi, maka akan dipanggil fungsi struk yang akan menampilkan struk yang sudah diolah.
