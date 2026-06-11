# Biolink — Kedai Nasi Sinar Berkah

Halaman biolink statis (gaya Linktree) untuk bio Instagram/TikTok. Cuma HTML + CSS, di-host gratis di **GitHub Pages**. Tidak ada backend / database.

```
08 - Biolink Web/
├── index.html        ← halaman utama (edit link di sini)
├── style.css         ← desain (warna/font brand Kedai Nasi)
└── assets/
    ├── logo.png      ← Logo-07 (versi warna)
    └── fonts/        ← Creative Vintage + Fabulous Script (display)
```

---

## 1. ISI DULU DATANYA (wajib sebelum live)

Buka `index.html`, cari kata **`GANTI`**, ganti dengan data asli:

| Tombol | Yang diganti | Contoh |
|---|---|---|
| WhatsApp Order | `wa.me/62GANTI` | `wa.me/628123456789` (62 + nomor tanpa 0 depan) |
| Catering & Acara | `wa.me/62GANTI` (boleh nomor sama / beda) | sda |
| GoFood | `GANTI_LINK_GOFOOD` | link share GoFood, atau hapus blok kalau belum daftar |
| GrabFood | `GANTI_LINK_GRABFOOD` | sda |
| Google Maps | `GANTI_LINK_MAPS` | link share lokasi GBP / `maps.app.goo.gl/...` |
| Instagram | `instagram.com/GANTI_USERNAME` | `instagram.com/kedainasisinarberkah` |
| TikTok | `tiktok.com/@GANTI_USERNAME` | `tiktok.com/@kedainasi...` |

> Channel belum ada (mis. belum di GrabFood)? **Hapus** blok `<a class="link-btn"> ... </a>`-nya. Jangan biarkan link `GANTI`.

Data ini masih **pending dari klien** (lihat plan Juni): nomor WA order, status & link GoFood/GrabFood, link Google Maps/GBP, username IG & TikTok.

---

## 2. DEPLOY KE GITHUB PAGES

1. Buat repo baru di GitHub, mis. `sinarberkah-bio` (public).
2. Upload **isi** folder ini ke root repo (`index.html` harus di root, bukan di dalam subfolder).
   ```bash
   cd "08 - Biolink Web"
   git init
   git add .
   git commit -m "biolink kedai nasi sinar berkah"
   git branch -M main
   git remote add origin https://github.com/<user>/sinarberkah-bio.git
   git push -u origin main
   ```
3. GitHub → repo → **Settings → Pages** → Source: `Deploy from a branch` → Branch: `main` / `/ (root)` → Save.
4. Tunggu ±1 menit. URL jadi: `https://<user>.github.io/sinarberkah-bio/`
5. Tempel URL itu ke bio Instagram & TikTok.

### Domain custom (opsional)
Punya domain (mis. `sinarberkah.com`)? Settings → Pages → Custom domain. Atau pakai `bio.sinarberkah.com` lewat CNAME ke `<user>.github.io`.

---

## 3. EDIT NANTI
Tambah/ubah tombol = edit `index.html` (copy satu blok `<a class="link-btn">`), commit, push. Pages auto-update.

Brand colors di `style.css` (`:root`) kalau perlu tweak: maroon `#942D33`, coral `#F48365`, kuning `#EDE944`.
