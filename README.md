| Nama                    | NIM        | Kelas   | Matkul            |
|-------------------------|------------|---------|-------------------|
| Muhammad Rizqy | 312310415  | TI.23.A4| Pemrograman Web 2 |

Praktikum 7-10

1. Membuat Tabel Kategori
Kita akan membuat tabel baru bernama `kategori` untuk mengkategorikan artikel.
Struktur Tabel `kategori`:

Jalankan query berikut:

![image](https://github.com/user-attachments/assets/df47a00d-5dfe-41c6-97ab-322b7b9250eb)

2. Mengubah Tabel Artikel
Tambahkan foreign key `id_kategori` pada tabel `artikel` untuk membuat relasi dengan tabel 
`kategori`. 
Query untuk menambahkan foreign key:

![image](https://github.com/user-attachments/assets/dda32de7-b4c2-4e96-908a-737f686ffb10)

3. Membuat Model Kategori
Buat file model baru di `app/Models` dengan nama `KategoriModel.php`:

![image](https://github.com/user-attachments/assets/1b95d658-8c85-44d9-8ce6-fd8eff10aea5)

4. Memodifikasi Model Artikel
Modifikasi `ArtikelModel.php` untuk mendefinisikan relasi dengan `KategoriModel`:

![image](https://github.com/user-attachments/assets/7322f525-f44d-4567-9e62-779685ea7006)

Menambahkan method `getArtikelDenganKategori()` untuk mengambil data artikel beserta 
nama kategorinya menggunakan join

5. Memodifikasi Controller Artikel
Modifikasi `Artikel.php` untuk menggunakan model baru dan menampilkan data relasi:

![image](https://github.com/user-attachments/assets/1f0c0376-460f-4641-8f99-5d7a9a69b769)

![image](https://github.com/user-attachments/assets/1ccca0a1-56be-46ba-894e-5f81db6628df)

![image](https://github.com/user-attachments/assets/4aaa30dd-035d-482d-9242-a6da1d344378)

![image](https://github.com/user-attachments/assets/a8ab05c9-975a-4e71-a707-0c777a0c7052)

![image](https://github.com/user-attachments/assets/ec7b5a4b-d17e-4da1-8cd4-1e17aa1bbb7b)

![image](https://github.com/user-attachments/assets/02cff5c1-8d92-440f-bbde-c5cf9356b543)

![image](https://github.com/user-attachments/assets/66040985-7704-465c-be37-45c0ec89ed7a)

6. Memodifikasi View
Buka folder view/artikel sesuaikan masing-masing view.
**index.php**

![image](https://github.com/user-attachments/assets/fff913f3-aa5d-4d7b-9890-2f46abb4e30a)

**admin_index.php**

![image](https://github.com/user-attachments/assets/6c98713c-fb44-4f70-be84-b70195c41fb6)

![image](https://github.com/user-attachments/assets/83cad4ec-7c8c-4465-b16c-e80783edfb7b)

![image](https://github.com/user-attachments/assets/9f909071-72e0-4070-be52-025f1fd75166)

![image](https://github.com/user-attachments/assets/d5ad6833-466f-4b36-a528-ab02056c54de)

![image](https://github.com/user-attachments/assets/77f11021-378e-46bd-b490-4fe9a482c0f5)

**form_add.php**

![image](https://github.com/user-attachments/assets/007e1d63-f75b-4720-991e-245eab7d6645)

![image](https://github.com/user-attachments/assets/4c3c2a5f-16ce-4068-b506-f2dc7321fb48)

![image](https://github.com/user-attachments/assets/f08f0878-867d-4bb1-b7e3-9e4d5d7ec436)

**form_edit.php**

![image](https://github.com/user-attachments/assets/bcf71563-8c33-424e-a9fa-0b833ddc0282)

![image](https://github.com/user-attachments/assets/9daab03a-0b06-4ec2-8b6c-2215ccc25aa3)

![image](https://github.com/user-attachments/assets/30fd0aa7-026b-4169-b8f8-9187ba842a69)

7. Testing
Lakukan uji coba untuk memastikan semua fungsi berjalan dengan baik:
• Menampilkan daftar artikel dengan nama kategori.

![image](https://github.com/user-attachments/assets/55a589bc-809f-49a1-be76-99e408f50614)

• Menambah artikel baru dengan memilih kategori.

![image](https://github.com/user-attachments/assets/4c67f2d2-47e9-47d0-8bdd-f1af77af0138)

• Mengedit artikel dan mengubah kategorinya.

![image](https://github.com/user-attachments/assets/88d6a955-f270-461e-a390-ed175a404bd5)

• Menghapus artikel.

sebelum:

![image](https://github.com/user-attachments/assets/319d14aa-3152-4dac-bd8d-ebb78366cb4e)

sesudah:

![image](https://github.com/user-attachments/assets/59e5135d-a9cb-4182-89b8-aa055c878e6b)

8. Membuat Model.
Pada modul sebelumnya sudah dibuat ArtikelModel, pada modul ini kita akan
memanfaatkan model tersebut agar dapat diakses melalui AJAX.

9. Membuat AJAX Controller

![image](https://github.com/user-attachments/assets/46c90da8-8852-4a70-9d5d-2e0d27bb0971)

10. Membuat View

![image](https://github.com/user-attachments/assets/89bec5c2-f3e3-4f14-93b8-19b4ab526df1)

![image](https://github.com/user-attachments/assets/e5922213-a54c-43d8-b8b3-4784ba35caca)

![image](https://github.com/user-attachments/assets/3e53ed3f-7178-47d0-8027-a58e612231ca)

![image](https://github.com/user-attachments/assets/ce508026-8ca8-4f8c-8c6c-c7ebe322d0d1)

11. Persiapan
* Pastikan MySQL Server sudah berjalan.
* Buka database `lab_ci4`.
* Pastikan tabel `artikel` dan `kategori` sudah ada dan terisi data.
* Pastikan library jQuery sudah terpasang atau dapat diakses melalui CDN.

12. Modifikasi Controller Artikel
Ubah method `admin_index()` di `Artikel.php` untuk mengembalikan data dalam format
JSON jika request adalah AJAX. (Sama seperti modul sebelumnya)

![image](https://github.com/user-attachments/assets/3e57d9ad-8b23-41e3-90a6-934de1ab3740)

Penjelasan:
• `$page = $this->request->getVar('page') ?? 1;`: Mendapatkan nomor
halaman dari request. Jika tidak ada, default ke halaman 1.
• `$builder->paginate(10, 'default', $page);`: Menerapkan pagination
dengan nomor halaman yang diberikan.
• `$this->request->isAJAX()`: Memeriksa apakah request yang datang adalah
AJAX.
• Jika AJAX, kembalikan data artikel dan pager dalam format JSON.
• Jika bukan AJAX, tampilkan view seperti biasa.

13. Modifikasi View (admin_index.php)
* Ubah view `admin_index.php` untuk menggunakan jQuery.
* Hapus kode yang menampilkan tabel artikel dan pagination secara langsung.
* Tambahkan elemen untuk menampilkan data artikel dan pagination dari AJAX.
* Tambahkan kode jQuery untuk melakukan request AJAX.

![image](https://github.com/user-attachments/assets/2afe6114-97ea-4cc8-90a8-e79bcc9b3e70)

![image](https://github.com/user-attachments/assets/a4b6cf7a-c63a-49ae-a45b-e2c216a2a945)

![image](https://github.com/user-attachments/assets/dc7a12a7-abb3-4179-b387-368887550d1f)

![image](https://github.com/user-attachments/assets/c633d358-dbb9-49d0-a186-0fbe3bc85f6a)

Pertanyaan dan Tugas
1. Selesaikan semua langkah praktikum di atas.
2. Modifikasi tampilan data artikel dan pagination sesuai kebutuhan desain.

![Screenshot 2025-06-19 214251](https://github.com/user-attachments/assets/33b43aed-d99a-45ac-9182-de22a769b9fa)

3. Tambahkan indikator loading saat data sedang diambil dari server.

![image](https://github.com/user-attachments/assets/8441e3cd-7a62-4a9c-9143-9519ea301e12)

4. Implementasikan fitur sorting (mengurutkan artikel berdasarkan judul, dll.) dengan AJAX.

Berdasarkan ID:

![image](https://github.com/user-attachments/assets/8af8ad7b-445b-47ac-8f49-ed0d4985c003)

Berdasarkan Judul:

![image](https://github.com/user-attachments/assets/863c585d-e393-4157-b21e-f701e8569480)

Berdasarkan Kategori:

![image](https://github.com/user-attachments/assets/b15940da-d1c7-4c69-afd0-cc53375f67e9)

14. Persiapan
Periapan awal adalah mengunduh aplikasi REST Client, ada banyak aplikasi yang dapat digunakan untuk
keperluan tersebut. Salah satunya adalah Postman. Postman – Merupakan aplikasi yang berfungsi
sebagai REST Client, digunakan untuk testing REST API. Unduh apliasi Postman dari tautan berikut:
https://www.postman.com/downloads/

15. Membuat Model.
Pada modul sebelumnya sudah dibuat ArtikelModel, pada modul ini kita akan memanfaatkan model
tersebut agar dapat diakses melalui API.

16. Membuat REST Controller
Pada tahap ini, kita akan membuat file REST Controller yang berisi fungsi untuk menampilkan,
menambah, mengubah dan menghapus data. Masuklah ke direktori app\Controllers dan buatlah file
baru bernama Post.php. Kemudian, salin kode di bawah ini ke dalam file tersebut:

![image](https://github.com/user-attachments/assets/4329ef04-69de-44b5-94ab-289cfcc4e9d2)

![image](https://github.com/user-attachments/assets/852374bc-0a2b-42af-ad3c-2b75b52cf8ac)

![image](https://github.com/user-attachments/assets/98558c92-8f10-4fad-9eab-1f6cd3d21183)

Kode diatas berisi 5 method, yaitu:
• index() – Berfungsi untuk menampilkan seluruh data pada database.
• create() – Berfungsi untuk menambahkan data baru ke database.
• show() – Berfungsi untuk menampilkan suatu data spesifik dari database.
• update() – Berfungsi untuk mengubah suatu data pada database.
• delete() – Berfungsi untuk menghapus data dari database.

17. Membuat Routing REST API
Untuk mengakses REST API CodeIgniter, kita perlu mendefinisikan route-nya terlebih dulu.
Caranya, masuklah ke direktori app/Config dan bukalah file Routes.php. Tambahkan kode
di bawah ini:

![image](https://github.com/user-attachments/assets/91f4967b-0e16-443e-a7d5-9f94048e8759)

Untuk mengecek route nya jalankan perintah berikut:

![image](https://github.com/user-attachments/assets/e1b1a50c-f8ea-46f2-8fed-cec9366d4599)

Selanjutnya akan muncul daftar route yang telah dibuat.

![image](https://github.com/user-attachments/assets/3b2cb57b-ffc3-4e9c-a298-88b2eeff9e74)

Seperti yang terlihat, satu baris kode routes yang di tambahkan akan menghasilkan banyak
Endpoint.
Selanjutnya melakukan uji coba terhadap REST API CodeIgniter.

18. Testing REST API CodeIgniter
Buka aplikasi postman dan pilih create new → HTTP Request

![image](https://github.com/user-attachments/assets/890a0541-a634-4ff5-8dbd-685eca172ffc)

19. Menampilkan Semua Data
Pilih method GET dan masukkan URL berikut:
http://localhost:8080/post
Lalu, klik Send. Jika hasil test menampilkan semua data artikel dari database, maka pengujian
berhasil.

![image](https://github.com/user-attachments/assets/f64d2583-357d-4ccf-9827-49f82399ed25)

20. Menampilkan Data Spesifik
Masih menggunakan method GET, hanya perlu menambahkan ID artikel di belakang URL
seperti ini:
http://localhost:8080/post/2
Selanjutnya, klik Send. Request tersebut akan menampilkan data artikel yang memiliki ID
nomor 2 di database.

![image](https://github.com/user-attachments/assets/6ee45f3c-3175-4ab3-b058-c757f410a51d)

21. Mengubah Data
Untuk mengubah data, silakan ganti method menjadi PUT. Kemudian, masukkan URL artikel
yang ingin diubah. Misalnya, ingin mengubah data artikel dengan ID nomor 2, maka masukkan
URL berikut:
http://localhost:8080/post/2
Selanjutnya, pilih tab Body. Kemudian, pilih x-www-form-uriencoded. Masukkan nama
atribut tabel pada kolom KEY dan nilai data yang baru pada kolom VALUE. Kalau sudah,
klik Send.

![image](https://github.com/user-attachments/assets/483f730c-5453-4b60-84d6-c2d124b96d47)

22. Menambahkan Data
Anda perlu menggunakan method POST untuk menambahkan data baru ke database.
Kemudian, masukkan URL berikut:
http://localhost:8080/post
Pilih tab Body, lalu pilih x-www-form-uriencoded. Masukkan atribut tabel pada kolom KEY
dan nilai data baru di kolom VALUE. Jangan lupa, klik Send.

![image](https://github.com/user-attachments/assets/99d40810-b938-4228-b0cd-ee101d37875c)

23. Menghapus Data
Pilih method DELETE untuk menghapus data. Lalu, masukkan URL spesifik data mana yang
ingin di hapus. Misalnya, ingin menghapus data nomor 3, maka URL-nya seperti ini:
http://localhost:8080/post/3
Langsung saja klik Send, maka akan mendapatkan pesan bahwa data telah berhasil dihapus dari
database.

![image](https://github.com/user-attachments/assets/dbb337cf-e57e-4b50-8d96-abb937c99945)
