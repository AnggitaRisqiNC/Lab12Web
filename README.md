# Lab12Web
Nama : Anggita Risqi Nur Clarita

NIM : 312210450

Kelas : TI.22.A.4

## DAFTAR ISI <br>
| No | Description | Link |
|-----|------|-----|
|1|Modul Praktikum 12|[Click Here](https://drive.google.com/file/d/1s6WQttG6_OT29TGUtrt5VBzUbjNcCdmZ/view)|
|2|Instruksi Praktikum|[Click Here](#instruksi-praktikum)|
|3|Langkah-langkah Praktikum|[Click Here](#langkah-langkah-praktikum)|

## Praktikum
> ### Instruksi Praktikum
> 1. Persiapkan text editor misalnya **VSCode**.
>
> 2. Buat folder baru dengan nama **lab12_form_login** pada docroot webserver **(htdocs)**
>
> 3. Ikuti langkah-langkah praktikum yang akan dijelaskan berikutnya.

## Langkah-langkah Praktikum
### Jalankan Apache dan MySQL server dari menu XAMPP Control

![1](https://github.com/AnggitaRisqiNC/Lab12Web/assets/115614419/c4341cd3-51d1-48e8-8390-9a426078e2d5)


1. **Buat Tabel *user* Pada Database *latihan1***

    Tabel tersebut akan berisi *id, username,* dan *password*. Kolom `id` akan menjadi *primary key* untuk tabel. Kolom `username` akan memiliki *unique index*.

    ![2](https://github.com/AnggitaRisqiNC/Lab12Web/assets/115614419/be064c8e-4359-4bf4-9d09-af12bdbb98fb)

    Setelah tabel user berhasil ditambahkan maka akan muncul output seperti ini:

    ![3](https://github.com/AnggitaRisqiNC/Lab12Web/assets/115614419/ef035bac-79e5-438a-a24c-5a0e2588c6eb)


2. **Buat File *login_session.php***

    ```php
    <?php

    session_start();
    if (!isset($_SESSION['isLogin'])) header('location: login.php');

    ?>
    ```

    File tersebut berisi kode yang berfungsi untuk memeriksa apakah pengguna sudah login atau belum, file ini nantinya akan di include di setiap halaman yang membutuhkan login. Jika pengguna belum login, pengguna akan diarahkan ke halaman login terlebih dahulu.


3. **Buat File *login.php***
    
    File tersebut berisi kode halaman login untuk sistem Data Barang. Pada bagian `if (isset($_POST['submit']))` akan berfungsi mengecek apakah form login dengan tombol "submit" telah dikirim. Jika berhasil dan ditemukan user, maka pengguna akan dialihkan ke halaman utama. Jika gagal login, maka `$errorMsg =` akan membuat *pesan error* untuk login gagal.


    **Output Halaman Login :**

    ![4](https://github.com/AnggitaRisqiNC/Lab12Web/assets/115614419/4896faec-f479-4e94-a922-27035ac077b1)


    ![5](https://github.com/AnggitaRisqiNC/Lab12Web/assets/115614419/68ac7ab8-40a5-4a57-ab3d-ba40cd3a2d61)


4. **Hasil Output Halaman Home :**

    Setelah proses login berhasil, halaman home akan ditampilkan. Halaman home berisi informasi data barang dan fitur yang dapat diakses oleh pengguna yang telah login seperti *tambah barang, ubah barang, hapus barang,* serta *contact* seperti pada [Praktikum 11](https://github.com/AnggitaRisqiNC/Lab11Web) di pertemuan yang lalu.


    ![6](https://github.com/AnggitaRisqiNC/Lab12Web/assets/115614419/2cd538a5-487b-4369-bfa7-53b0787030ae)



5. **Hasil Output Tambah Barang :**


    ![7](https://github.com/AnggitaRisqiNC/Lab12Web/assets/115614419/d4a15bf9-871b-499d-a664-71bf65ecf19b)



6. **Hasil Output Ubah Barang :**


    ![8](https://github.com/AnggitaRisqiNC/Lab12Web/assets/115614419/dbe91903-da4e-42d2-a370-fd710bc20f37)



7. **Hasil Output Contact :** 


    ![9](https://github.com/AnggitaRisqiNC/Lab12Web/assets/115614419/3cf8af8c-96be-439a-b970-c7a88229242a)


## Finish