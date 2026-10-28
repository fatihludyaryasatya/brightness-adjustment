# Tugas Citra Digital

**Nama:** Fatih Ludy Aryasatya
**NIM:** 24260047
**Program Studi:** Teknik Informatika, Universitas Nahdlatul Ulama Indonesia
**Mata Kuliah:** Citra Digital (isi sesuai nama mata kuliah)
**Dosen:** (isi nama dosen)

## Deskripsi
Repository ini berisi tugas pembuktian bahwa citra digital adalah susunan angka, beserta penerapan *brightness adjustment*. Semua proses dikerjakan dengan Python di Google Colab.

## Isi Tugas
1. **Pembuktian citra digital = susunan angka**
   - Membaca metadata gambar (format, ukuran, mode warna, EXIF)
   - Mengubah gambar menjadi array NumPy (tinggi x lebar x 3 kanal RGB, nilai 0-255)
   - Menampilkan nilai piksel nyata (piksel 0,0 dan blok 5x5 per kanal)
   - Menampilkan blok grayscale 8x8 dengan angka di atas gambar
   - Rekonstruksi: array angka diubah kembali menjadi gambar dan diverifikasi identik dengan aslinya
   - Histogram distribusi nilai piksel
2. **Repository GitHub** sebagai tempat upload tugas dan pemantauan progress
3. **Brightness adjustment**
   - Rumus: `g(x,y) = f(x,y) + β`, hasil dibatasi (*clip*) ke rentang 0-255
   - Percobaan β = +60 (lebih terang) dan β = -60 (lebih gelap)
   - Perbandingan nilai piksel, rata-rata intensitas, dan pergeseran histogram

## Struktur File
| File | Keterangan |
|---|---|
| `citra_digital.ipynb` | Notebook Google Colab (seluruh kode) |
| `IMG_1637.HEIC` | Gambar yang digunakan |
| `gray_8x8.csv` | Nilai piksel blok grayscale 8x8 |
| `piksel_5x5.npy` | Array piksel RGB blok 5x5 |
| `blok_8x8.png` | Visualisasi angka piksel 8x8 |
| `hasil_rekonstruksi.png` | Gambar hasil rekonstruksi dari array |
| `histogram_asli.png` | Histogram gambar asli |
| `brightness_perbandingan.png` | Perbandingan gelap, asli, terang |
| `histogram_brightness.png` | Pergeseran histogram setelah brightness |

## Cara Menjalankan
1. Buka `citra_digital.ipynb` di Google Colab.
2. Jalankan sel instal `pillow-heif`.
3. Isi `USERNAME` pada sel pengambilan gambar dengan username GitHub.
4. Jalankan semua sel secara berurutan (**Runtime → Run all**).

## Teknologi
Python, NumPy, Pillow, pillow-heif, Matplotlib, Google Colab

## Kesimpulan
Citra digital tersusun dari matriks angka. Setiap piksel menyimpan nilai intensitas 0-255 untuk tiap kanal warna. Mengubah angka-angka tersebut, misalnya menambah nilai untuk brightness, langsung mengubah tampilan gambar.
