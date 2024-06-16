<!-- 
Grid Adalah Sistem Tata Letak Berbasis grid dua dimensi
flexbox hanya satu dimensi
-->

## GRID TERMINOLOGY

**GRID CONTAINER**: Sebuah komponen yang `display`-nya kita set sebagai grid.

**GRID**: Mirip seperti tabel dengan kolom dan baris.

**GRID ITEM**: Komponen anak dari grid container.

**GRID LINE**: Garis pemisah grid item, baik horizontal maupun vertikal.

**GRID CELL**: Area di dalam kolom dan baris yang dipisahkan oleh grid line.

**GRID TRACK (BARIS)**: Bagian antara dua grid line atau baris.

**GRID AREA**: Total area dari beberapa grid cell.

**GRID TEMPLATE**: Untuk menentukan kolom dan baris dalam grid:
- `grid-template-columns`: Menentukan kolom.
- `grid-template-rows`: Menentukan baris.

**COLUMN KE SAMPING**: Misalnya `column: 200px 100px 200px`; grid cell pertama lebarnya 200px.

**ROW KE BAWAH**: Misalnya `row: 100px`; grid cell pertama tingginya 100px.

## GRID ITEMS

**GRID ITEMS START dan END**: Bisa ditentukan mulai dari kolom atau baris berapa.

**GRID LINE NAME**:
- `column line`: Sela di antara komponen ke samping.
- `row line`: Sela di antara komponen ke bawah.
- `grid-column-start`: Mulai kesamping.
- `grid-column-end`: Akhir kesamping.
- `grid-row-start`: Mulai dari atas.
- `grid-row-end`: Akhir bawah.

**GRID AREA**: `grid-template-areas` contohnya:
```css
.container {
  display: grid;
  grid-template-columns: 400px auto 400px;
  grid-template-rows: 50px auto 100px;
  grid-template-areas:
    "header header header"
    ". content ."
    "footer footer footer";
}
