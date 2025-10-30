# Lab6Web - Bootstrap

## Tugas 1

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Refactor Layout Praktikum 4</title>

  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" 
        rel="stylesheet" 
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" 
        crossorigin="anonymous">
</head>

<body>

  <nav class="navbar navbar-expand-lg navbar-dark bg-dark mb-4">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Praktikum 6</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link active" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Artikel</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <div class="container">

    <div class="row mb-4">
      <div class="col-md-4">
        <div class="card text-center">
          <div class="card-body">
            <h5 class="card-title">Heading 1</h5>
            <p class="card-text">Deskripsi singkat heading 1.</p>
          </div>
        </div>
      </div>
      <div class="col-md-4">
        <div class="card text-center">
          <div class="card-body">
            <h5 class="card-title">Heading 2</h5>
            <p class="card-text">Deskripsi singkat heading 2.</p>
          </div>
        </div>
      </div>
      <div class="col-md-4">
        <div class="card text-center">
          <div class="card-body">
            <h5 class="card-title">Heading 3</h5>
            <p class="card-text">Deskripsi singkat heading 3.</p>
          </div>
        </div>
      </div>
    </div>

    <div class="row">
      <div class="col-md-8">
        <div class="card mb-4">
          <div class="card-body">
            <h4 class="card-title">Konten Utama</h4>
            <p class="card-text">
              Ini adalah area untuk artikel atau isi utama website.
              Anda dapat menambahkan teks, gambar, atau elemen lain di sini.
            </p>
          </div>
        </div>
      </div>

      <div class="col-md-4">
        <div class="card mb-4">
          <div class="card-body">
            <h5 class="card-title">Sidebar</h5>
            <p class="card-text">
              Ini adalah bagian sidebar untuk link tambahan atau informasi lainnya.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" 
          integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" 
          crossorigin="anonymous"></script>
</body>
</html>
```

- Navbar (`<nav class="navbar navbar-expand-lg navbar-dark bg-dark mb-4">`)
Bagian atas halaman berwarna gelap dengan teks “Praktikum 6”. Di dalamnya terdapat dua menu yaitu `<a class="nav-link">Home</a>` dan `<a class="nav-link">Artikel</a>`. Navbar ini memakai class `navbar-expand-lg` sehingga tampil penuh di layar besar dan otomatis jadi tombol menu di layar kecil.

- Container utama (`<div class="container">`)
Semua isi halaman dibungkus di dalam container agar posisinya terpusat dan memiliki jarak tepi yang proporsional pada berbagai ukuran layar.

- Baris pertama (`<div class="row mb-4">`)
Berisi tiga kolom sejajar (`<div class="col-md-4">`) yang masing-masing memiliki card Bootstrap (`<div class="card">`). Tiap card berisi judul (`<h5 class="card-title">Heading 1</h5>`, dst.) dan deskripsi singkat (`<p class="card-text">`). Tujuannya untuk menampilkan tiga informasi utama di halaman depan.

- Baris kedua (`<div class="row">`)
  Dibagi menjadi dua kolom:

  * Kolom kiri (`<div class="col-md-8">`) berisi konten utama, yaitu artikel atau isi web yang ditampilkan dalam card.
  * Kolom kanan (`<div class="col-md-4">`) digunakan sebagai sidebar untuk menampilkan informasi tambahan atau tautan lain.
    Keduanya juga menggunakan struktur `<div class="card mb-4">` agar tampil seragam dan terpisah rapi.

- Script Bootstrap JS (`<script src="https://cdn.jsdelivr.net/..."></script>`)
  Berfungsi mengaktifkan fitur interaktif seperti tombol toggle pada navbar saat tampilan layar kecil.


Hasil di browser:

<img width="856" height="1008" alt="image" src="https://github.com/user-attachments/assets/43adf5ef-7cf0-499c-ab01-09bda5dd5e65" />

## Tugas 2

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Refactor Form Praktikum 5</title>

  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" 
        rel="stylesheet" 
        integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" 
        crossorigin="anonymous">
</head>

<body class="bg-light">

  <div class="container mt-5">
    <div class="row justify-content-center">
      <div class="col-md-6">

        <div class="card shadow-sm">
          <div class="card-body">
            <h3 class="text-center mb-4">Formulir Kontak</h3>

            <form>
              <div class="mb-3">
                <label for="nama" class="form-label">Nama Lengkap</label>
                <input type="text" class="form-control" id="nama" placeholder="Masukkan nama Anda">
              </div>

              <div class="mb-3">
                <label for="email" class="form-label">Alamat Email</label>
                <input type="email" class="form-control" id="email" placeholder="nama@contoh.com">
              </div>

              <div class="mb-3">
                <label for="pesan" class="form-label">Pesan</label>
                <textarea class="form-control" id="pesan" rows="3" placeholder="Tulis pesan Anda di sini"></textarea>
              </div>

              <button type="submit" class="btn btn-primary w-100">Kirim</button>
            </form>
          </div>
        </div>

      </div>
    </div>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" 
          integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" 
          crossorigin="anonymous"></script>
</body>
</html>
```

- Bagian awal (`<head>`)
Mengatur informasi dasar halaman seperti `charset="UTF-8"` dan `viewport` agar tampilan menyesuaikan layar perangkat. Elemen `<title>` berisi judul halaman “Refactor Form Praktikum 5”. Terdapat juga link CSS Bootstrap (`<link href="https://cdn.jsdelivr.net/...">`) untuk memuat gaya bawaan Bootstrap.

- Bagian `<body class="bg-light">`
Memberi latar belakang berwarna abu terang pada seluruh halaman. Semua isi halaman diletakkan di dalam `<div class="container mt-5">`, yang memberi jarak atas (margin-top) agar posisi form tidak menempel pada tepi layar.

- Struktur form
Diatur menggunakan grid Bootstrap (`<div class="row justify-content-center">`) untuk menempatkan form di tengah layar. Form diletakkan dalam kolom berukuran sedang (`<div class="col-md-6">`) dan dibungkus dengan card Bootstrap (`<div class="card shadow-sm">`) supaya tampil rapi dengan bayangan halus.

- Bagian isi card (`<div class="card-body">`)
Di dalamnya terdapat judul `<h3 class="text-center mb-4">Formulir Kontak</h3>` dan elemen form. Form menggunakan tag `<form>` tanpa aksi (karena belum ada pengolahan data).  Isi form terdiri dari tiga input utama:

  * `<input type="text" id="nama">` untuk Nama Lengkap.
  * `<input type="email" id="email">` untuk Alamat Email.
  * `<textarea id="pesan">` untuk menulis pesan.

  Setiap input dibungkus dalam `<div class="mb-3">` agar memiliki jarak antar-elemen, dan semua label menggunakan class `form-label` supaya tampil sesuai gaya Bootstrap.

- Tombol kirim (`<button type="submit" class="btn btn-primary w-100">Kirim</button>`)
  Tombol berwarna biru khas Bootstrap (`btn-primary`) dan melebar penuh di kolom (`w-100`).

- Script Bootstrap JS (`<script src="https://cdn.jsdelivr.net/..."></script>`)
  Diletakkan di bagian bawah untuk mengaktifkan fitur interaktif dari Bootstrap jika dibutuhkan.

Hasil di web browser:

<img width="869" height="794" alt="image" src="https://github.com/user-attachments/assets/9cc5fb85-592b-4ac4-86a2-4b5020e0a90e" />

## Tugas 3

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfolio - Syafira Luthfi Azzahra</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

<nav class="navbar navbar-expand-lg navbar-dark bg-primary">
  <div class="container">
    <a class="navbar-brand" href="#">Syafira Luthfi Azzahra</a>
  </div>
</nav>

<div class="container my-5">
  <div class="row align-items-center">
    <div class="col-md-4">
      <img src="https://picsum.photos/300" alt="Foto Saya" class="img-fluid rounded">
    </div>
    <div class="col-md-8">
      <h2>Syafira Luthfi Azzahra</h2>
      <p>Mahasiswi Informatika yang tertarik dalam pengembangan web dan desain UI/UX. 
         Mempunyai semangat tinggi untuk belajar teknologi terbaru dan membangun website interaktif.</p>
    </div>
  </div>
</div>

<div class="container my-5">
  <h3 class="text-center mb-4">Portfolio Saya</h3>
  <div class="row">
    <div class="col-md-4 mb-3">
      <div class="card">
        <img src="https://picsum.photos/400/200" class="card-img-top" alt="Project 1">
        <div class="card-body">
          <h5 class="card-title">Proyek 1</h5>
          <p class="card-text">Website profil menggunakan HTML dan Bootstrap.</p>
        </div>
      </div>
    </div>
    <div class="col-md-4 mb-3">
      <div class="card">
        <img src="https://picsum.photos/401/200" class="card-img-top" alt="Project 2">
        <div class="card-body">
          <h5 class="card-title">Proyek 2</h5>
          <p class="card-text">Form login interaktif dengan validasi JavaScript.</p>
        </div>
      </div>
    </div>
    <div class="col-md-4 mb-3">
      <div class="card">
        <img src="https://picsum.photos/402/200" class="card-img-top" alt="Project 3">
        <div class="card-body">
          <h5 class="card-title">Proyek 3</h5>
          <p class="card-text">Dashboard admin responsif menggunakan Bootstrap Grid.</p>
        </div>
      </div>
    </div>
  </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

- Bagian `<head>`
  Mengatur informasi dasar halaman seperti `charset="UTF-8"` dan `viewport` agar tampilan menyesuaikan perangkat.
  Elemen `<title>` menampilkan judul “Portfolio - Syafira Luthfi Azzahra”.
  Tautan `<link>` menuju Bootstrap CSS digunakan untuk menerapkan gaya bawaan Bootstrap.

- Navbar (`<nav class="navbar navbar-expand-lg navbar-dark bg-primary">`)
  Menampilkan bilah navigasi berwarna biru dengan teks nama “Syafira Luthfi Azzahra”.
  Elemen ini dibungkus dalam `<div class="container">` agar posisinya rapi di tengah halaman.

- Bagian Tentang Saya (`<div class="container my-5">`)
  Terdiri dari dua kolom:

  * Kolom kiri (`<div class="col-md-4">`) menampilkan foto profil (`<img src="https://picsum.photos/300">`) dengan class `img-fluid rounded` agar gambar responsif dan sudutnya melengkung.
  * Kolom kanan (`<div class="col-md-8">`) berisi nama lengkap “Syafira Luthfi Azzahra” dan paragraf deskripsi singkat tentang latar belakang, minat di bidang pengembangan web, dan UI/UX.
    Baris ini menggunakan `align-items-center` agar teks dan gambar sejajar vertikal di tengah.

- Bagian Portfolio (`<div class="container my-5">`)
  Menampilkan judul “Portfolio Saya” di tengah halaman (`text-center`).
  Di bawahnya terdapat tiga card proyek dalam satu baris (`<div class="row">`), masing-masing menggunakan `<div class="col-md-4 mb-3">`.
  Setiap card berisi:

  * Gambar proyek (`<img src="https://picsum.photos/...">`)
  * Judul proyek (`<h5 class="card-title">`)
  * Deskripsi singkat (`<p class="card-text">`)

  Rinciannya:

  1. Proyek 1 – Website profil menggunakan HTML dan Bootstrap.
  2. Proyek 2 – Form login interaktif dengan validasi JavaScript.
  3. Proyek 3 – Dashboard admin responsif memakai Bootstrap Grid.

- Script Bootstrap JS (`<script src="https://cdn.jsdelivr.net/..."></script>`)
  Ditempatkan di bagian akhir untuk mengaktifkan elemen interaktif dari Bootstrap seperti dropdown atau navbar toggle.

Hasil di web browser:

<img width="1903" height="920" alt="image" src="https://github.com/user-attachments/assets/d2cc916b-d9ea-47a8-83d9-4d607e320d75" />
