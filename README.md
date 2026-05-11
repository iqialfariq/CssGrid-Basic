# 🧠 Penjelasan CSS Grid
<p align="justify">
CSS Grid adalah sistem layout dua dimensi di CSS yang memungkinkan kita mengatur elemen dalam baris dan kolom secara fleksibel. Dengan Grid, kita bisa membuat struktur halaman yang kompleks, responsif, dan rapi tanpa harus bergantung pada teknik lama seperti float atau positioning. 
</p>

---

## 📌 Property dan Value CSS Grid

### 🔀 Grid Template Column
<p align="justify">
Untuk menentukan jumlah dan ukuran kolom dalam sebuah grid layout. Dengan properti ini, kita bisa mengatur apakah kolom berukuran tetap, fleksibel, atau
mengikuti isi konten. value grid-template-column ada 4 : px, %, auto, fr.
</p>

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: 1fr 2fr;
      }
  ```

---

### 🔀 Grid Template Rows
<p align="justify">
Untuk menentukan jumlah dan tinggi baris dalam sebuah grid layout. Nilai yang diberikan berupa daftar spasi, di mana setiap nilai mewakili tinggi dari
baris tertentu value grid-template-rows ada 4 : px, %, auto, fr.
</p>

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-rows: 1fr 2fr;
      }
  ```

---

### 🔀 Grid Auto Columns
<p align="justify">
Untuk menentukan ukuran kolom yang dibuat secara implisit dalam grid. Artinya, jika sebuah item ditempatkan di kolom yang belum didefinisikan dengan
grid-template-columns, maka kolom baru akan otomatis dibuat, dan ukurannya mengikuti nilai grid-auto-columns. value grid-auto-columns ada 4 yaitu:
px, %, auto, fr. 
</p>

  Contoh:
  ```css
      .container {
        display: grid;
        grid-auto-columns: 150px;
      }
  ```

---

### 🔀 Grid Auto Rows 
<p align="justify">
Untuk menentukan tinggi baris yang dibuat secara implisit dalam grid. Jadi, jika sebuah item ditempatkan di baris yang belum didefinisikan dengan grid
template-rows, maka baris baru akan otomatis dibuat, dan ukurannya mengikuti nilai grid-auto-rows. value grid-auto-rows ada 4 yaitu: px, %, auto, fr.
</p>

  Contoh:
  ```css
      .container {
        display: grid;
        grid-auto-rows: 150px;
      }
  ```

---

### 🔀 Grid Auto Flow
<p align="justify">
Untuk mengatur penempatan item atau cell pada grid track, termasuk yang ditulis secara implicit. Biasa nya digunakan untuk mengatur 
kolom secara horizontal dan vertikal.
</p>

value grid-auto-flow ada 4 yaitu:
1) row, 
2) column, 
3) row dense, 
4) column dense. 

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: 100px 100px;
        grid-auto-flow: row;
      }
  ```

---
