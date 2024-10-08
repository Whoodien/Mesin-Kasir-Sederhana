# Mesin-Kasir-Sederhana
Program mesin kasir sederhana ini merupakan tugas asistensi praktikum dasar pemrograman ITS dengan kode P1. Program ini menggunakan input dari user agar dapat bekerja

#include <stdio.h>

#define MAX_ITEMS 20 //Mendefinisikan konstanta yang disebut (MAX_ITEMS) yang berupa item maksimal yang bisa ditampilkan

typedef struct { //Mendefinisikan sebuah struktur baru yaitu (Item) yang memiliki tiga atribut yaitu nama, harga, dan jumlah
    char nama[40];
    float harga;
    int jumlah;
} Item; //Nama dari struktur baru yaitu Item

void tampilkanStruk(Item items[], int count, float diskon) { //Membuat semacam deklarasi struk yang akan dibuat, disini akan menerima nama dari item (menggunakan array), jumlah item (count), dan juga diskon yang akan diberikan
    float total = 0; //Menginisialisasi sebuah variabel total untuk menyimpan total harga
    printf("========= Struk Belanja ========= \n");
    printf("--------- Toko Manusia ----------\n");
    for (int i = 0; i < count; i++) { //Menginisialisasi sebuah loop untuk setiap item (i)
        float subtotal = items[i].harga * items[i].jumlah; //Menambahkan sebuah subtotal dan menghitung harga subtotal untuk setiap harga sebuah item dikalikan dengan banyaknya item yang akan dibeli
        printf("%s (x%d): %.2f\n", items[i].nama, items[i].jumlah, subtotal);  //Print ini untuk menampilkan nama item, berapa banyak item nya beserta harga subtotal
        total += subtotal; //Menambahkan subtotal ke total keseluruhan
    }
    printf("=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-= \n");
    printf("Total Sebelum Diskon : %.2f \n", total);
    if (diskon > 0) { //Fungsi if disini digunakan apabila terdapat diskon
        float totalDiskon = total * (diskon / 100); //Disini karena diskon berupa persen maka akan di buat totaldiskon adalah total dikali diskon/100
        total -= totalDiskon; //Dinyatakan bahwa total ketika ada diskon adalah total dikurangi dengan totaldiskon
        printf("Total Diskon\t: %.2f%% \n", diskon);
        printf("Total Setelah Diskon : %.2f \n", total);
    } else { //Fungsi else disini akan digunakan apabila tidak terdapat diskon atau diskonnya 0
        printf("Tidak ada diskon.\n");
        printf("Total Setelah Diskon : %.2f\n", total);
    }
    printf("=================================");
}

//Disini fungsi utama program akan dijalankan
int main() {
    Item items[MAX_ITEMS]; 
    int count = 0;
    float diskon;

    printf("Masukkan jumlah barang (maksimal %d): ", MAX_ITEMS);
    scanf("%d", &count);

    if (count == 0){
        printf ("Barangnya kok gak ada???");
    }

    else {
        for (int i = 0; i < count; i++) {
            printf("Masukkan nama barang ke-%d \t : ", i + 1);
            scanf("%s", items[i].nama);
            printf("Masukkan harga barang ke-%d \t : ", i + 1);
            scanf("%f", &items[i].harga);
            printf("Masukkan jumlah barang ke-%d \t : ", i + 1);
            scanf("%d", &items[i].jumlah);

        }

        printf("Masukkan diskon (dalam persen, 0 jika tidak ada): ");
        scanf("%f", &diskon);

        tampilkanStruk(items, count, diskon);
    }

    return 0;
}
