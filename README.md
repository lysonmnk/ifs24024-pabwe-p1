# Praktikum 1: Praktik HTML

Proyek multi-halaman berbasis **HTML murni** (tanpa CSS dalam bentuk apa pun — inline, internal, maupun external). Seluruh tampilan dan struktur dibangun hanya menggunakan elemen HTML bawaan.

## Aturan Umum

1. **Dilarang menggunakan CSS** sama sekali (inline, internal, external). Semua tampilan wajib murni dari elemen HTML.
2. Seluruh halaman (poin 1–4 di bawah) harus **saling terhubung** melalui link navigasi yang diletakkan di bagian atas setiap halaman.

## Struktur Halaman

| No | Halaman | File | Referensi |
|----|---------|------|-----------|
| 1  | IMDb Top 3 Movies | `index.html` | [IMDb Top 250](https://www.imdb.com/chart/top/?ref_=nv_mv_250) |
| 2a | Dev Blog – Halaman Utama | `blog.html` | [dev.to/t/programming](https://dev.to/t/programming) |
| 2b | Dev Blog – Halaman Detail | `blog-detail.html` | (dibuka dari `blog.html`) |
| 3  | Form Pendaftaran Akun | `form.html` | – |
| 4  | Curriculum Vitae (CV) | `cv.html` | – |
| 5  | Integrasi Navigasi | Semua file di atas | – |

---

## 1. IMDb Top 3 Movies — `index.html`

- Teks **"IMDB Chart"** → heading level 3 (`<h3>`)
- Teks **"IMDB Top 3 Movies"** → heading level 1 (`<h1>`)
- Pisahkan judul dan konten dengan garis horizontal (`<hr>`)
- Tampilkan 3 film dalam **tabel 2 kolom**:
  - Kolom 1: gambar cover, ukuran **72×107**
  - Kolom 2: informasi film
- Judul film → heading level 3 (`<h3>`)
- Tahun rilis, durasi, dan rating usia → masing-masing dibungkus `<span>`, lalu seluruhnya dibungkus `<p>`
- Informasi rating → dibungkus `<p>`
- Gunakan `&nbsp;` (Â ) untuk spasi tambahan

## 2. Dev Blogs

### 2a. Halaman Utama Blog — `blog.html`

- Foto profil, ukuran **32×32**
- Teks **"Programming"** → heading level 3 (`<h3>`)
- Teks **"The magic behind computers."** → paragraf (`<p>`)
- Setiap item blog → **tabel 2 kolom**:
  - Kolom 1: foto profil
  - Kolom 2: informasi blog
- Username → tebal (`<b>`/`<strong>`), tanggal posting → `<span>`, keduanya dibungkus `<p>`. Gunakan `<br />` untuk baris baru
- Judul blog → heading level 3 (`<h3>`), dibungkus link (`<a>`) menuju `blog-detail.html`
- Tag blog → `<span>`, dibungkus `<p>`
- Gunakan `&nbsp;` (Â ) untuk spasi

### 2b. Halaman Detail Blog — `blog-detail.html`

- Dibuka saat judul blog di `blog.html` diklik
- Gambar cover, lebar **100%**
- Info author: foto, username (tebal), tanggal posting (`<span>`)
- Judul blog → heading level 1 (`<h1>`)
- `<hr>` pemisah judul dan konten
- Isi konten blog → paragraf (`<p>`)
- `<hr>` pemisah konten dan komentar
- Bagian komentar: foto profil + `<textarea>` 3 baris, placeholder **"Add to the discussion"**

## 3. Form Pendaftaran Akun — `form.html`

- `<fieldset>` dengan `<legend>` **"Daftar Akun"**
- Semua input dibungkus `<fieldset>`:
  - Nama lengkap → `type="text"`
  - Jenis kelamin → `type="radio"`
  - Tempat lahir → `type="text"`
  - Tanggal lahir → `type="date"`
  - Agama → `<select>` (opsi: Islam, Katolik, Protestan, Hindu, Buddha, Konghucu)
  - Hobi → `type="checkbox"`
  - Password → `type="password"`
  - Persetujuan → `type="checkbox"`
- Tombol **Reset** (`type="reset"`) dan tombol **Submit** (`type="submit"`)

## 4. Curriculum Vitae (CV) — `cv.html`

- Foto, ukuran **200**
- Nama → heading level 1 (`<h1>`)
- Judul tiap bagian → heading level 2 (`<h2>`)
- Program Studi → heading level 3 (`<h3>`)
- Email dan WA → dibungkus heading level 6 (`<h6>`)
- Bagian **Pendidikan** dan **Keahlian** → list tidak berurutan (`<ul>`)
- Bagian **Sertifikat** dan **Portfolio** → list berurutan (`<ol>`)

## 5. Integrasi Proyek

Gabungkan seluruh halaman (`index.html`, `blog.html`, `blog-detail.html`, `form.html`, `cv.html`) sehingga saling terhubung lewat **navigation bar** yang konsisten di bagian atas setiap halaman.

---

## Checklist Pengerjaan

- [ ] `index.html` — IMDb Top 3 Movies
- [ ] `blog.html` — Dev Blog (halaman utama)
- [ ] `blog-detail.html` — Dev Blog (detail)
- [ ] `form.html` — Form Pendaftaran Akun
- [ ] `cv.html` — Curriculum Vitae
- [ ] Navigasi antar halaman terpasang di semua file
- [ ] Tidak ada CSS dalam bentuk apa pun (inline/internal/external) di seluruh file

## Catatan untuk AI Assistant

Saat membantu mengerjakan proyek ini:
- **Jangan pernah menambahkan atribut `style`, tag `<style>`, atau file `.css`** — pelanggaran aturan utama tugas.
- Semua tata letak (kolom, tabel, ukuran gambar) harus dicapai dengan elemen HTML native seperti `<table>`, atribut `width`/`height` pada `<img>`, dll.
- Pastikan setiap halaman baru yang dibuat menyertakan navigation bar yang sama di bagian atas.
- Gunakan tag heading (`h1`–`h6`) sesuai level yang ditentukan per bagian, jangan disamaratakan.