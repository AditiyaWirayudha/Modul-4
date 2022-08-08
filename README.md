###### Nama    : Aditiya Wirayudha
###### Kelas   : XI RPL 1
###### No.Abs  : 06

# Modul 4

1) membuat folder dan file yang akan di isi

Nama folder yang harus dibuat 
- barang
- kategori
- layout

Nama file yang harus dibuat
- home.blade.php
- index.blade.php
- app.blade.php

folder dan file-file nya menjadi satu seperti 
contoh gambar yang terlihat seperti dibawah ini

![image](https://user-images.githubusercontent.com/109930265/183360373-1fbac289-aec7-4312-9a18-b1bad53bcf42.png)

>Tugas 2 membuat layout dengan master template blade untuk project anda
2) pada folder layout `file app.blade.php` kita mengambil **css dan js di bootstrap** ini linknya
[Bootstrap](https://getbootstrap.com/docs/5.2/getting-started/introduction/)

>![image](https://user-images.githubusercontent.com/109929687/183342789-f6776591-ea33-4712-88ac-e847218de516.png)
gambar diatas adalah bagian bootstrap yang kita pakai sebagai css dengan menambahkan syntax sebagai berikut
```
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css">
```

selanjutnya bagian js dengan menambahkan syntax sebagai berikut
```
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js"></script>
```

Selanjutnya isi file `app.blade.php` dengan all codenya
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css">
    <title>
        @yield('title')
    </title>
</head>
<body>
<nav class="navbar navbar-expand-lg bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand text-white" href="#">Penjualan</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link text-white" aria-current="page" href="/kategori">Kategori</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-white" href="/barang">Barang</a>
        </li>
       
    </div>
  </div>
</nav>
<div class="container">
    @yield('content')
</div>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
saya tidak menggunakan cara yang saya jelaskan karena di bootstrap sudah ada yang mudah jadi saya tinggal copy dan paste saja

Selanjutnya folder **barang** yang berisi file `index.blade.php`

all codenya akan terlihat seperti dibawah ini karena kurang lebih saya memahami isi code dibawah
```
@extends('layout.app')

@section('title')
    Barang
@endsection 

@section('content')
<div class="mt-3">
    <table class="table table-stripped">
        <thead>
            <tr>
                <th width="5%">No.</th>
                <th>Nama</th>
                <th width="15%">Kategori</th>
                <th width="15%">Qty</th>
                <th width="15%">Harga Beli</th>
                <th width="15%">Harga Jual</th>
                <th width="15%">Aksi</th>
            <tr>
        </thead>
        
        <tbody>
            <tr>
                <td>1</td>
                <td>Meja</td>
                <td>ATK</td>
                <td>1</td>
                <td>50000</td>
                <td>55000</td>
                <td>Hapus | Edit</td>
            </tr>
        </tbody>
    </table>
</div>
@endsection    
```

Selanjutnya pada folder **kategori** file `home.blade.php` 

all codenya akan ditampilkan di bawah ini
```
@extends('layout.app')

@section('title')
    Barang
@endsection 

@section('content')
<div class="mt-3">
    <table class="table table-stripped">
        <thead>
            <tr>
                <th width="5%">No.</th>
                <th>Nama</th>
                <th width="15%">Kategori</th>
                <th width="15%">Qty</th>
                <th width="15%">Harga Beli</th>
                <th width="15%">Harga Jual</th>
                <th width="15%">Aksi</th>
            <tr>
        </thead>
        
        <tbody>
            <tr>
                <td>1</td>
                <td>kursi</td>
                <td>ATK</td>
                <td>1</td>
                <td>50000</td>
                <td>55000</td>
                <td>Hapus | Edit</td>
            </tr>
        </tbody>
    </table>
</div>
@endsection    
```

Hasilnya akan jadi seperti ini
![image](https://user-images.githubusercontent.com/109930265/183360817-274a6f6a-e514-4075-9d60-40dc1e665a8c.png)
![image](https://user-images.githubusercontent.com/109930265/183360884-325bdab9-13bb-40ca-9ed8-69c1c0aeff4e.png)
