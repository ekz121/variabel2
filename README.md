# variabel2

Penjelasan Program C++ untuk Surat Jalan Pengiriman
Deskripsi Program
Program ini adalah aplikasi konsol sederhana yang digunakan untuk menghitung biaya pengiriman paket berdasarkan berat paket dan menghasilkan surat jalan (waybill) dengan informasi pengirim, penerima, dan detail paket. Program ini meminta pengguna untuk memasukkan data seperti nama, alamat, kota, dan berat paket, lalu menampilkan hasil dalam format terstruktur.

Fungsi Utama Program
Input Data:
Meminta pengguna untuk memasukkan informasi pengirim (nama, alamat, kota).
Meminta pengguna untuk memasukkan informasi penerima (nama, alamat, kota).
Meminta pengguna untuk memasukkan berat paket dalam kilogram.
Perhitungan Biaya:
Menghitung biaya pengiriman berdasarkan berat paket dengan tarif tetap Rp1000 per kg.
Output Surat Jalan:
Menampilkan informasi pengirim, penerima, dan detail paket dalam format yang rapi, termasuk biaya pengiriman dengan dua angka desimal.
Elemen-Elemen Kode dan Definisi
Berikut adalah penjelasan rinci tentang setiap elemen dalam kode, termasuk definisi dan fungsinya:

1. Include Directives

```
#include <iostream>
#include <string>
#include <iomanip>
```
`#include <iostream>:`
Definisi: Library standar C++ untuk input/output.
Fungsi: Memungkinkan penggunaan fungsi seperti cout (untuk output) dan cin (untuk input) di konsol.
Contoh Penggunaan: Digunakan untuk menampilkan pesan dan membaca input pengguna.

`#include <string>:`
Definisi: Library standar C++ untuk tipe data string.
Fungsi: Memungkinkan penggunaan tipe data string untuk menyimpan teks, seperti nama, alamat, dan kota.
Contoh Penggunaan: Digunakan untuk mendeklarasikan variabel seperti namaPengirim dan alamatPenerima.

`#include <iomanip>:`
Definisi: Library standar C++ untuk manipulasi format output.
Fungsi: Memungkinkan pengaturan format output, seperti menentukan jumlah angka desimal atau lebar kolom.
Contoh Penggunaan: Digunakan dengan fixed dan setprecision(2) untuk menampilkan biaya pengiriman dengan dua angka desimal.

2. Namespace
```using namespace std;```
Definisi: Deklarasi untuk menggunakan namespace std.
Fungsi: Mengizinkan penggunaan fungsi dan objek dari namespace std tanpa perlu menulis std:: setiap kali. Misalnya, cout dapat digunakan langsung tanpa std::cout.
Catatan: Penggunaan using namespace std; bersifat opsional. Dalam proyek besar, lebih disarankan untuk menulis std:: secara eksplisit untuk menghindari konflik nama.

`3. Fungsi main`

```int main() {
    // Kode program
    return 0;
}
```
Definisi: Fungsi utama dalam program C++ yang menjadi titik masuk eksekusi program.
Fungsi: Semua logika program ditulis di dalam fungsi ini. return 0 menunjukkan bahwa program selesai dengan sukses.
Catatan: Setiap program C++ harus memiliki fungsi main.

4. Deklarasi Variabel
```
string namaPengirim, alamatPengirim, kotaPengirim;
string namaPenerima, alamatPenerima, kotaPenerima;
double beratPaket;
const double tarifPerKg = 1000.0;
double biayaPengiriman;
string namaPengirim, alamatPengirim, kotaPengirim;:

```
Definisi: Variabel bertipe string untuk menyimpan informasi pengirim.
Fungsi: Menyimpan nama, alamat, dan kota pengirim yang dimasukkan pengguna.
string namaPenerima, alamatPenerima, kotaPenerima;:
Definisi: Variabel bertipe string untuk menyimpan informasi penerima.
Fungsi: Menyimpan nama, alamat, dan kota penerima yang dimasukkan pengguna.
double beratPaket;:
Definisi: Variabel bertipe double untuk menyimpan berat paket.
Fungsi: Menyimpan berat paket dalam kilogram (bisa berupa bilangan desimal).
const double tarifPerKg = 1000.0;:
Definisi: Konstanta bertipe double untuk tarif pengiriman per kg.
Fungsi: Menyimpan nilai tarif tetap Rp1000 per kg. Kata kunci const memastikan nilai ini tidak dapat diubah selama program berjalan.
Catatan: Penggunaan konstanta seperti ini membuat kode lebih mudah dimodifikasi jika tarif perlu diubah di masa depan.
double biayaPengiriman;:
Definisi: Variabel bertipe double untuk menyimpan hasil perhitungan biaya pengiriman.
Fungsi: Menyimpan hasil perhitungan beratPaket * tarifPerKg.

5. Input Data
```
cout << "Masukkan Nama Pengirim: ";
getline(cin, namaPengirim);

cout << "Masukkan Alamat Pengirim: ";
getline(cin, alamatPengirim);

cout << "Masukkan Kota Pengirim: ";
getline(cin, kotaPengirim);
cout << "Masukkan Nama Pengirim: ";:
```
Definisi: Menampilkan pesan di konsol.
Fungsi: Meminta pengguna untuk memasukkan nama pengirim.
getline(cin, namaPengirim);:
Definisi: Fungsi untuk membaca satu baris teks dari input pengguna.
Fungsi: Menyimpan input pengguna (termasuk spasi) ke dalam variabel namaPengirim.
Catatan: getline digunakan di sini karena input bisa berupa teks panjang dengan spasi, seperti "John Doe". Jika hanya menggunakan cin, hanya kata pertama yang akan dibaca.
Pola yang Sama: Pola ini diulang untuk meminta alamat, kota pengirim, serta informasi penerima.
cin >> beratPaket;:
Definisi: Membaca input numerik dari pengguna.
Fungsi: Menyimpan berat paket yang dimasukkan pengguna ke dalam variabel beratPaket.
Catatan: cin digunakan di sini karena input adalah angka, bukan teks panjang.
6. Perhitungan Biaya
```
biayaPengiriman = beratPaket * tarifPerKg;
```
Definisi: Operasi aritmatika untuk menghitung biaya pengiriman.
Fungsi: Mengalikan berat paket dengan tarif per kg untuk mendapatkan total biaya pengiriman.
Catatan: Hasil disimpan dalam variabel biayaPengiriman.

7. Output Surat Jalan

```
cout << "\n======= SURAT JALAN =======\n";
cout << "Dari:\n";
cout << "Nama   : " << namaPengirim << endl;
cout << "Alamat : " << alamatPengirim << endl;
cout << "Kota   : " << kotaPengirim << endl;

cout << "\nKepada:\n";
cout << "Nama   : " << namaPenerima << endl;
cout << "Alamat : " << alamatPenerima << endl;
cout << "Kota   : " << kotaPenerima << endl;

cout << "\nInformasi Paket:\n";
cout << "Berat Paket       : " << beratPaket << " kg" << endl;
cout << "Biaya Pengiriman  : Rp" << fixed << setprecision(2) << biayaPengiriman << endl;
cout << "\n======= SURAT JALAN =======\n";:
```

Definisi: Menampilkan header surat jalan.
Fungsi: Memberikan judul pada output untuk memperjelas bahwa ini adalah surat jalan.
cout << "Nama : " << namaPengirim << endl;:
Definisi: Menampilkan informasi pengirim dalam format "Nama : [nama]".
Fungsi: Menampilkan data yang telah dimasukkan pengguna.
endl: Menambahkan baris baru setelah output.
Pola yang Sama: Pola ini diulang untuk menampilkan informasi penerima dan detail paket.
fixed << setprecision(2):
Definisi: Manipulator dari <iomanip> untuk mengatur format output angka.
Fungsi:
fixed: Memastikan angka ditampilkan dalam format desimal tetap (bukan notasi ilmiah).
setprecision(2): Menampilkan dua angka di belakang koma.
Contoh Penggunaan: Jika biayaPengiriman adalah 2500.5, output akan menjadi "Rp2500.50".
8. Return Statement
```
return 0;
```
Definisi: Mengakhiri fungsi main dan mengembalikan nilai ke sistem operasi.
Fungsi: Menandakan bahwa program telah selesai dengan sukses. Nilai 0 biasanya menunjukkan tidak ada error.
Contoh Eksekusi Program
Berikut adalah contoh interaksi dengan program:

```
Masukkan Nama Pengirim: John Doe
Masukkan Alamat Pengirim: Jl. Merdeka No. 123
Masukkan Kota Pengirim: Jakarta

Masukkan Nama Penerima: Jane Smith
Masukkan Alamat Penerima: Jl. Sudirman No. 456
Masukkan Kota Penerima: Bandung

Masukkan Berat Paket (kg): 2.5

======= SURAT JALAN =======
Dari:
Nama   : John Doe
Alamat : Jl. Merdeka No. 123
Kota   : Jakarta

Kepada:
Nama   : Jane Smith
Alamat : Jl. Sudirman No. 456
Kota   : Bandung

Informasi Paket:
Berat Paket       : 2.5 kg
Biaya Pengiriman  : Rp2500.00
```
