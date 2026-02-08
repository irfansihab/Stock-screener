# 🚀 Panduan Deploy ke Vercel

## Metode 1: Deploy via Vercel Dashboard (PALING MUDAH)

### Step 1: Persiapan File
✅ File yang sudah disiapkan:
- `index.html` - Aplikasi utama
- `README.md` - Dokumentasi
- `vercel.json` - Konfigurasi Vercel
- `.gitignore` - File yang diabaikan

### Step 2: Upload ke GitHub
1. Buka https://github.com dan login
2. Klik tombol **"+"** di pojok kanan atas → **"New repository"**
3. Isi detail repository:
   - Repository name: `stock-screener` atau nama lain
   - Description: "Aplikasi Screening Saham Indonesia"
   - Pilih **Public** (gratis unlimited)
   - ✅ Centang "Add a README file" (skip ini karena kita sudah punya)
4. Klik **"Create repository"**

5. Upload file:
   - Klik **"uploading an existing file"**
   - Drag & drop semua file:
     - index.html
     - README.md
     - vercel.json
     - .gitignore
   - Klik **"Commit changes"**

### Step 3: Deploy ke Vercel
1. Buka https://vercel.com
2. Klik **"Sign Up"** atau **"Login"**
3. Pilih **"Continue with GitHub"** (lebih mudah)
4. Authorize Vercel untuk akses GitHub
5. Di dashboard Vercel, klik **"Add New..."** → **"Project"**
6. Pilih repository `stock-screener` yang baru dibuat
7. Klik **"Import"**
8. Konfigurasi (biarkan default):
   - Framework Preset: **Other**
   - Root Directory: `./`
   - Build Command: (kosongkan)
   - Output Directory: (kosongkan)
9. Klik **"Deploy"**
10. ⏳ Tunggu 30-60 detik
11. 🎉 **SELESAI!** Aplikasi Anda live di internet!

### Step 4: Akses Aplikasi
Anda akan dapat URL seperti:
```
https://stock-screener-xxxxx.vercel.app
```

### Step 5: Custom Domain (Opsional)
1. Di dashboard Vercel, buka project Anda
2. Klik tab **"Settings"** → **"Domains"**
3. Masukkan domain custom (jika punya), contoh: `stockscreener.com`
4. Follow instruksi untuk setting DNS
5. Atau gunakan subdomain gratis Vercel: edit menjadi nama yang lebih pendek

---

## Metode 2: Deploy via Vercel CLI (UNTUK DEVELOPER)

### Install Vercel CLI
```bash
npm install -g vercel
```

### Login
```bash
vercel login
```

### Deploy
```bash
cd /path/to/project
vercel
```

Ikuti instruksi di terminal, lalu aplikasi akan otomatis deploy!

---

## Update Aplikasi Setelah Deploy

### Via GitHub:
1. Edit file di repository GitHub
2. Commit changes
3. Vercel otomatis re-deploy! ✨

### Via Vercel CLI:
```bash
vercel --prod
```

---

## Tips & Tricks

### 1. Preview Deployment
Setiap kali push ke GitHub (branch apapun), Vercel akan membuat **preview deployment** dengan URL unik. Berguna untuk testing sebelum production.

### 2. Environment Variables
Jika nanti butuh API key:
1. Settings → Environment Variables
2. Tambahkan key dan value
3. Redeploy

### 3. Analytics
Vercel menyediakan analytics gratis:
- Jumlah pengunjung
- Performance metrics
- Geographic distribution

### 4. Custom 404 Page
Buat file `404.html` untuk custom error page

---

## Troubleshooting

### ❌ Build Failed
- Cek apakah semua file sudah ter-upload
- Pastikan `index.html` ada di root directory

### ❌ Page Not Found
- Pastikan file bernama `index.html` (bukan `stock-screener.html`)
- Atau gunakan `vercel.json` untuk routing

### ❌ Deploy Lambat
- Tunggu 1-2 menit
- Refresh halaman
- Cek status di dashboard Vercel

---

## Share Aplikasi Anda

Setelah deploy, share URL ke:
1. ✅ Grup WhatsApp/Telegram
2. ✅ LinkedIn post
3. ✅ Twitter/X
4. ✅ Facebook groups (investor)
5. ✅ Stockbit forum
6. ✅ Kaskus subforum investasi

**Template post:**
```
🎉 Launching Aplikasi Screening Saham Indonesia!

Fitur:
✅ Analisis profil risiko
✅ Perhitungan return otomatis
✅ 35+ saham Indonesia
✅ Link ke Stockbit & TradingView
✅ 100% GRATIS

Coba sekarang: https://your-app.vercel.app

#investasi #saham #stockscreener #indonesia
```

---

## Need Help?

- Vercel Docs: https://vercel.com/docs
- Vercel Support: https://vercel.com/support
- GitHub Guides: https://guides.github.com

**Selamat! Aplikasi Anda sudah online! 🚀**
