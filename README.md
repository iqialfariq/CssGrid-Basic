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

### 🔀 Grid Template Areas 
<p align="justify">
Untuk mendefinisikan grid template menggunakan nama dari area yang di tulis pada property grid areas. value grid-template-areas ditentukan oleh nama
area nya itu sendiri.
</p>

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: 1fr 2fr;
        grid-template-rows: auto 1fr auto;
        grid-template-areas:
          "header header"
          "sidebar content"
          "footer footer";
        gap: 10px;
      }
  ```

---

### 🔀 Grid Area
<p align="justify">
Digunakan untuk memberi nama pada area grid agar mudah direferensikan dengan grid-template-areas. value grid-area ditentukan oleh nama area nya itu 
sendiri. 
</p>

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: 1fr 2fr;
        grid-template-rows: auto 1fr auto;
        grid-template-areas:
          "header header"
          "sidebar content"
          "footer footer";
        gap: 10px;
      }
      .header {
        grid-area: header;
        background: darkcyan;
      }
  ```

---

### 🔀 Column Gap
<p align="justify">
digunakan untuk menentukan jarak horizontal antar kolom pada layout berbasis CSS Grid atau Multi-column layout. 
</p>

value column-gap ada 4 yaitu: 
1) px, 
2) em, 
3) rem, 
4) %. 

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        column-gap: 20px;
      }
  ```

---

### 🔀 Rows Gap
<p align="justify">
Untuk menentukan jarak vertikal antar baris pada layout berbasis CSS Grid. 
</p>

value rows-gap ada 4 yaitu: 
1) px, 
2) em, 
3) rem,
4) %. 

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        rows-gap: 20px;
      }
  ```

---

### 🔀 Justify Items 
<p align="justify">
untuk mengatur posisi horizontal (sepanjang inline axis atau mepet atas) dari semua item di dalam sebuah grid container.  
</p>

value justify-items ada 4 yaitu: 
1) start, 
2) end, 
3) center, 
4) stretch. 

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        justify-items: center;
        gap: 20px;
      }
  ```

---

### 🔀 Align Items 
<p align="justify">
untuk mengatur posisi vertikal (sepanjang block axis atau mepet kiri) dari semua item di dalam sebuah container (baik Grid maupun Flexbox).  
</p>

value align-items ada 4 yaitu: 
1) start, 
2) end, 
3) center, 
4) stretch. 

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: repeat(2, 100px);
        grid-template-rows: 200px 200px;
        align-items: center;
        gap: 20px;
      }
  ```

---

### 🔀 Place Items
<p align="justify">
untuk menerapkan align items dan justify-items dalam satu deklarasi atau satu baris.  
</p>

value place-items ada 4 yaitu: 
1) start, 
2) end, 
3) center, 
4) stretch. 

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: repeat(2, 100px);
        grid-template-rows: 200px 200px;
        place-items: center;
        gap: 20px;
      }
  ```

---

### 🔀 Justify Content 
<p align="justify">
untuk mengatur seluruh grid container pada sumbu horizontal. Ini bisa dilakukan ketika ukuran total grid lebih kecil dari ukuran containernya, 
biasanya ketika grid items nya menggunakan ukuran yang fixed (px) 
</p>

value justify-content ada 7 yaitu: 
1) start, 
2) end, 
3) center, 
4) stretch, 
5) space-around, 
6) space-between, 
7) space-evenly.

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: repeat(3, 100px);
        justify-content: space-evenly;
        background: lightgray;
      }
  ```

---

### 🔀 Align Content 
<p align="justify">
untuk mengatur posisi keseluruhan grid tracks (baris) di sepanjang block axis (vertikal). 
</p>

value align-content ada 7 yaitu: 
1) start, 
2) end, 
3) center, 
4) stretch, 
5) space-around, 
6) space-between, 
7) space-evenly.

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: repeat(2, 100px);
        grid-template-rows: repeat(2, 50px);
        height: 300px;
        align-content: center;
        gap: 10px;
        background: lightgray;
      }
  ```

---

### 🔀 Place Content 
<p align="justify">
untuk menerapkan align content dan justify-content dalam satu deklarasi atau satu baris. 
</p>

value place-content ada 7 yaitu: 
1) start, 
2) end, 
3) center, 
4) stretch, 
5) space-around, 
6) space-between, 
7) space-evenly.

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: repeat(2, 100px);
        grid-template-rows: repeat(2, 50px);
        height: 300px;
        width: 500px;
        place-content: center;
        gap: 10px;
        background: lightgray;
      }
  ```

---

### 🔀 Grid Column Start  
<p align="justify">
untuk menentukan garis kolom tempat sebuah item grid akan dimulai. Dengan kata lain, ini mengatur posisi awal elemen di dalam grid container
berdasarkan garis kolom yang sudah ditentukan. 
</p>

value grid-column-start ada 4 yaitu: 
1) auto, 
2) nomor, 
3) span n, 
4) nama. 

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: repeat(4, 100px);
        gap: 10px;
      }
      .container .b {
        background: lightblue;
        grid-column-start: 2;
      }
  ```

---

### 🔀 Grid Column End
<p align="justify">
untuk menentukan garis kolom tempat sebuah item grid berakhir. Dengan kata lain, ini mengatur titik akhir horizontal dari area grid yang ditempati
elemen. 
</p>

value grid-column-end ada 4 yaitu: 
1) auto, 
2) nomor, 
3) span n, 
4) nama. 

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: repeat(4, 100px);
        gap: 10px;
      }
      .container .b {
        background: lightblue;
        grid-column-start: 2;
        grid-column-end: 4;
      }
  ```

---

### 🔀 Grid Column
<p align="justify">
untuk shorthand (singkatan) pada grid-column-start dan grid-column-end sekaligus. Dengan kata lain, properti ini menentukan rentang kolom yang
ditempati sebuah item grid, dari garis awal hingga garis akhir. value grid-column adalah nomor line kolom itu sendiri
</p>

value grid-column ada 4 yaitu: 
1) auto, 
2) nomor, 
3) span n, 
4) nama.

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: repeat(2, 100px);
        grid-template-rows: repeat(4, 50px);
        gap: 10px;
      }
      .container .b {
        background: salmon;
        grid-column: 1 / 3;
      }
  ```

---

### 🔀 Grid Row Start 
<p align="justify">
untuk menentukan garis baris (row line) tempat sebuah item grid akan dimulai. Dengan kata lain, ini mengatur titik awal vertikal dari area grid yang
ditempati elemen. 
</p>

value grid-row-start ada 4 yaitu: 
1) auto, 
2) nomor, 
3) span n, 
4) nama. 

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: repeat(2, 100px);
        grid-template-rows: repeat(4, 50px);
        gap: 10px;
      }
      .container .b {
        background: salmon;
        grid-row-start: 1;
      }
  ```

---

### 🔀 Grid Row End 
<p align="justify">
untuk menentukan garis baris (row line) tempat sebuah item grid berakhir. Dengan kata lain, ini mengatur titik akhir vertikal dari area grid yang
ditempati elemen. 
</p>

value grid-row-start ada 4 yaitu: 
1) auto, 
2) nomor, 
3) span n, 
4) nama. 

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: repeat(2, 100px);
        grid-template-rows: repeat(4, 50px);
        gap: 10px;
      }
      .container .b {
        background: salmon;
        grid-row-start: 1;
        grid-row-end: 3;
      }
  ```

---

### 🔀 Grid Row
<p align="justify">
untuk shorthand (singkatan) pada grid-row-start dan gridrow-end sekaligus. Dengan kata lain, properti ini menentukan rentang baris (row) yang ditempati
sebuah item grid, dari garis awal hingga garis akhir. value grid-row adalah nomor line baris itu sendiri 
</p>

value grid-row-start ada 4 yaitu: 
1) auto, 
2) nomor, 
3) span n, 
4) nama. 

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: repeat(2, 100px);
        grid-template-rows: repeat(4, 50px);
        gap: 10px;
      }
      .container .b {
        background: salmon;
        grid-row: 1 / 2;
      }
  ```

---

### 🔀 Justify Self
<p align="justify">
untuk mengatur perataan (alignment) horizontal sebuah item grid di dalam sel grid-nya sendiri. Jadi, meskipun grid container sudah punya aturan
distribusi kolom, setiap item bisa diatur secara individual dengan justify-self. 
</p>

value justify-self ada 4 yaitu: 
1) start, 
2) end, 
3) center, 
4) stretch 

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: repeat(2, 100px);
        grid-template-rows: repeat(4, 50px);
        background: lightgray;
        gap: 10px;
      }
      .container .b {
        background: salmon;
        justify-self: start;
      }
  ```

---

### 🔀 Align Self
<p align="justify">
untuk mengatur perataan (alignment) vertikal sebuah item grid atau flex di dalam sel/grid track-nya sendiri. Jadi, meskipun container sudah punya
aturan global (align-items), setiap item bisa diatur secara individual dengan align-self. 
</p>

value align-self ada 4 yaitu: 
1) start, 
2) end, 
3) center, 
4) stretch. 

  Contoh:
  ```css
      .container {
        display: grid;
        grid-template-columns: repeat(2, 100px);
        grid-template-rows: repeat(4, 50px);
        background: lightgray;
        gap: 10px;
      }
      .container .b {
        background: salmon;
        align-self: center;
      }
  ```

---

### 🔀 Special Function

  ```
  repeat ()
  untuk mengulang sebuah ukuran columns atau rows yang sama tetapi lebih dari satu 
  ```

  ```
  min-content dan max-content
  untuk menentukan seberapa besar ukuran grid track bedasarkan konten pada sebuah item. 
  ```

  ```
  auto-fill dan auto-fitt
  untuk menentukan jumlah item untuk berada pada grid track  
  ```

  ```
  minmax () 
  untuk menentukan ukuran minimal dan maksimal dari grid track 
  ```
