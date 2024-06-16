# CSS Display and Flexbox Guide

## Display

### Display Types

- **Inline:** Hanya mengambil tempat secukupnya.
- **Block:** Mengambil tempat dari kiri ke kanan, satu baris penuh. Jika ada 2 konten, konten akan otomatis ke baris berikutnya.
- **Inline-block:** Ditampilkan secara inline, tetapi kita bisa mengubah tinggi dan lebar komponen layaknya block.

### Trial

- Inline: Tidak ada width dan height.
- Normal flow: Konten akan dibagi menjadi 2 block (content: konten 1 dan konten 2).
- Inline-block: Menjadi block tetapi 2 konten akan tetap dalam satu baris (content: konten 1 dan konten 2).

## Flexbox

### Flex Container

- **display: flex;**
  - Flex Container adalah komponen yang display-nya diatur sebagai flex. Misalnya, jika kita punya DIV dan kita set display-nya sebagai flex, maka DIV tersebut menjadi Flex Container.

### Flex Direction

- **Default:** Dari kiri ke kanan.
- **Options:**
  - `flex-direction: row;`
  - `flex-direction: row-reverse;`
  - `flex-direction: column;`
  - `flex-direction: column-reverse;`

### Flex Wrap

- **Default:** Flex item ditampilkan dalam satu garis baik secara vertikal (Row) maupun horizontal (Column).
- **Wrap:** Jika tidak menggunakan wrap, komponen akan terus tampil ke kanan sampai butuh scroll. Jika menggunakan wrap, komponen yang tidak muat akan turun ke baris berikutnya.
  - `flex-wrap: wrap;`

### Flex Item

- Flex Item adalah komponen yang berada di dalam Flex Container. Flex Item adalah anak (children) langsung dari Flex Container.

### Axes

- **Main Axis:** Kiri ke kanan.
- **Cross Axis:** Atas ke bawah.

### Margin and Padding

- **Margin:** Margin untuk semua komponen (luar).
- **Padding:** Padding untuk semua komponen (dalam).

### Order Flex Item

- Mengatur urutan Flex Item.

### Flex Grow and Shrink

- **Flex Grow:** Mengatur kesempatan untuk mengembangkan komponen (dalam scope container).
- **Flex Shrink:** Mengatur kesempatan untuk mengecilkan komponen (dalam scope container).

### Flex Basis

- Minimal ukuran dari suatu Flex Item. Hanya bisa digunakan bersama `flex-shrink` atau `flex-grow`.

### Flex Alignment

#### Justify Content

Menentukan jarak antar Flex Item.

- **justify-content: center;**
  - Tengah (jika tidak ada width, tidak bisa ke tengah).
- **justify-content: flex-start;**
  - Mulai dari kiri.
- **justify-content: flex-end;**
  - Mulai dari kanan.
- **justify-content: space-between;**
  - Ada space antara item.
- **justify-content: space-around;**
  - Ada jarak space di sekitar item.
- **justify-content: space-evenly;**
  - Ada jarak space yang merata.

#### Align Items

Mengatur letak Flex Item dalam Cross Axis (atas ke bawah).

- **align-items: center;**
  - Tengah dari atas ke bawah.
- **align-items: flex-start;**
  - Mulai dari atas kiri.
- **align-items: flex-end;**
  - Mulai dari bawah kiri.
- **align-items: stretch;**
  - Ditariik dari atas sampai bawah.
- **align-items: baseline;**
  - Default dari size base-nya.
- **align-items: space-around;**
  - Ada jarak space di sekitar item.
- **align-items: space-evenly;**
  - Ada jarak space yang merata.

### Align Content

(Jika menggunakan wrap, pakai ini)

**Note:** Mirip seperti `align-items`, tetapi `align-content` hanya bisa dilakukan jika kontennya di-wrap.

### Gap

Biasanya kita menggunakan margin untuk jarak antar Flex Item. Dalam Flexbox, lebih baik menggunakan `gap`.

**Penggunaan:**

- `row-gap: 10px;`
- `column-gap: 10px;`
- `gap: row px column px;`
