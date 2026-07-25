# QRIS-SCORE — Versi Web (Dashboard Lembaga Keuangan)

Folder khusus versi **Web** QRIS-SCORE: Dashboard Lembaga Keuangan/Koperasi
(ringkasan portofolio, daftar pengajuan, simulasi kalkulator skor, analitik
& proyeksi dampak, pengaturan bobot 25:50:25). Siap langsung dipublish
sebagai GitHub Pages repo tersendiri.

## Cara publish ke GitHub Pages

1. Buat repository baru di GitHub, misalnya `qris-score-web`.
2. Upload/push **seluruh isi folder ini** (`index.html`) ke root repo tersebut.
   - Lewat GitHub web: buka repo → **Add file → Upload files** → seret `index.html` → Commit.
   - Atau lewat git:
     ```bash
     cd qris-score-web
     git init
     git add .
     git commit -m "Deploy QRIS-SCORE web"
     git branch -M main
     git remote add origin https://github.com/USERNAME/qris-score-web.git
     git push -u origin main
     ```
3. Buka **Settings → Pages** di repo GitHub.
4. Pilih **Source: Deploy from a branch**, branch `main`, folder `/ (root)** → Save.
5. Tunggu 1–2 menit, situs akan aktif di:
   `https://USERNAME.github.io/qris-score-web`
6. **Catat URL ini** — dibutuhkan untuk mengonfigurasi folder `qris-score-showcase`.

## Isi folder

```
index.html   ← satu file mandiri, semua kode (HTML/CSS/JS) sudah inline di dalamnya
```

## Catatan

- Klik **"Masuk sebagai Demo"** untuk langsung masuk tanpa isi form — semua
  data adalah data dummy/simulasi untuk keperluan kompetisi Jambi Spark 2026.
- Butuh koneksi internet aktif (font, Tailwind CSS, dan jsPDF dimuat dari CDN).
- Ditulis dengan vanilla JavaScript (tanpa React/framework), jadi kompatibel
  penuh dengan GitHub Pages tanpa proses build apa pun.
