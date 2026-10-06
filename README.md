# VIBES.BOOTH ✦ Gen Z Digital Photobooth
### *Blok M & Virtual Companion Edition*

Aplikasi web photobooth digital modern bertema **Neo-Brutalism x Y2K Retro Blok M** yang dibuat dengan arsitektur **Single-File** (HTML, CSS via Tailwind CDN + Custom CSS, dan Vanilla JavaScript). Siap di-deploy langsung ke **Vercel**, GitHub Pages, atau static hosting lainnya tanpa perlu backend atau database server.

---

## 📸 Fitur Utama

### 1. Landing Mode Selection (Mode Pilihan Awal)
- **Mode 1: Classic Photobooth (Bareng Teman / Solo)**: Pengalaman foto photobooth autentik Blok M dengan frame, filter 35mm film, dan stiker lucu.
- **Mode 2: Virtual Frame (Foto Bareng Artis / K-Pop Idol)**: Live overlay transparan karakter idol K-Pop, aktor K-Drama, atau musisi indie Blok M langsung di atas kamera. Dilengkapi opsi posisi (Kiri, Tengah, Kanan), skala ukuran, flip arah, dan upload PNG idol sendiri!
- **Mode 3: Anime & Cartoon Photobooth**: Karakter anime (Neko girl, Cyber Mecha, Maskot Kucing Blok M) yang bisa diposisikan di samping bahu pengguna.
- Tombol **"Ganti Mode"** di header atas untuk berpindah mode kapan saja secara instan.

### 2. Camera & Capture Engine (WebRTC & Canvas)
- **Live Camera Stream**: Menggunakan `navigator.mediaDevices.getUserMedia` dengan orientasi kamera depan (mirror effect) & tombol **Flip Camera** untuk HP.
- **Mode Demo Selfie Bawaan**: Jika kamera tidak diizinkan atau diuji di perangkat tanpa webcam, pengguna bisa menggunakan *Demo Selfie* atau *Upload Foto Sendiri*.
- **3 Layout Format Cetak**:
  - `4-Cuts Vertical Strip` (Life Four Cuts style, 1x4)
  - `2x2 Grid Layout` (Kotak 4 foto)
  - `Single Shot` (Polaroid Style dengan chin besar untuk caption)
- **Interactive Shutter Workflow**:
  - Countdown 3... 2... 1... CHEESE! 📸
  - Layar flash putih otomatis saat capture
  - Efek suara audio synthesizer shutter & beeps via **Web Audio API** (tanpa file audio eksternal)

### 3. Live Film Filters & Aesthetics
1. **Normal**: Realistis dan jernih
2. **35mm Analog Film**: Warm tone, grain texture, saturated film look
3. **Y2K Soft Pink**: Dreamy pastel glow, soft contrast
4. **Monochrome Noir**: High-contrast black & white sinematik
5. **VHS Camcorder**: Cool tint dengan scanlines overlay khas camcorder 90-an
6. **Vintage Sepia**: Golden muted retro 90s

### 4. Frame & Motif Builder
- **Pilihan Warna Bingkai**: Deep Dark, Cream White, Baby Pink, Pastel Blue, Mint Matcha, Electric Yellow, Lilac, & Custom Color Picker.
- **Motif & Pola Grafis**:
  - *Solid Minimal*
  - *🏁 Y2K Checkerboard*
  - *🎞️ 35mm Filmstrip* (dengan lubang perforasi & penomoran film)
  - *💖 Retro Hearts*
  - *📰 Blok M Vintage Newspaper* (edisi akhir pekan)
  - *⚡ Cyber Neon Gradient*
- **Gaya Sudut Foto**: Sharp Square (0px) vs Soft Rounded (12px).

### 5. Drag & Drop Stickers, Watermarks & Captions
- **Sticker Drawer Interaktif**: Sunglasses 🕶️, Y2K Heart 💖, Sparkles ✨, Cherry 🍒, Bow Ribbon 🎀, "VIBE CHECK" badge 🏷️, "HOT GIRL" badge 🏷️, Cyber Star ⭐, 8-Bit Alien 👾, Sakura 🌸.
- Stiker dapat di-drag langsung di atas canvas, diatur ukurannya via slider, dan dihapus kapan saja.
- **Header Watermark Stamp**: Presets seperti `✦ BLOK M VIBES ✦ 2026`, `SEOUL FILM 90s ★`, `JAKARTA NIGHTS`, atau teks kustom.
- **Date & Time Stamp**: Format `YYYY.MM.DD HH:mm` otomatis sesuai waktu lokal.
- **Custom Caption**: Input teks bebas di bagian bawah frame.
- **Barcode Stempel**: Barcode retro ala tiket photobooth autentik.

### 6. High-Res Export & Download
- Menggunakan `<canvas>` composite engine untuk menggabungkan seluruh layer foto, filter, motif bingkai, stiker, dan watermark secara proporsional (object-fit cover) tanpa distorsi.
- Tombol **"Download Photo Strip (PNG)"** mengunduh file resolusi tinggi dengan format penamaan `vibes-booth-[mode]-[timestamp].png`.
- Tombol **"Salin"** untuk menyalin gambar langsung ke clipboard.
- Tombol **"Foto Ulang"** untuk me-reset sesi capture.

---

## 🚀 Cara Menjalankan & Deploy

### Jalankan Lokal:
1. Buka folder `potobooth` di komputer.
2. Klik ganda file `index.html` untuk langsung membukanya di browser Chrome, Edge, Safari, atau Firefox.
3. Atau buka melalui local server (Laragon `http://localhost/potobooth`, Live Server VS Code, dll).

### Deploy ke Vercel (Gratis & 1 Klik):
1. Push project ini ke repository GitHub.
2. Buka dashboard [Vercel](https://vercel.com) -> Klik **"Add New Project"**.
3. Import repository GitHub tersebut.
4. Karena ini adalah static single-file website, langsung klik **"Deploy"** (tanpa perlu setting build step).
5. Selesai! Web photobooth langsung live di URL `https://your-project.vercel.app`.
