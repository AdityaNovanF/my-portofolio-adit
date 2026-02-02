# Fitur Keamanan Portfolio

## 🔒 Proteksi yang Diterapkan

Website portfolio ini telah dilengkapi dengan berbagai lapisan keamanan untuk melindungi source code:

### 1. **Disable Right Click**
- Mencegah pengunjung membuka context menu dengan klik kanan
- Menghambat akses cepat ke "Inspect Element"

### 2. **Keyboard Shortcuts Protection**
- **F12** - Disabled
- **Ctrl+Shift+I** - Disabled (Inspect Element)
- **Ctrl+Shift+J** - Disabled (Console)
- **Ctrl+Shift+C** - Disabled (Element Picker)
- **Ctrl+U** - Disabled (View Source)
- **Ctrl+S** - Disabled (Save Page)

### 3. **DevTools Detection**
- Mendeteksi saat Developer Tools dibuka
- Otomatis redirect ke halaman blank jika terdeteksi
- Monitoring ukuran window untuk deteksi DevTools

### 4. **Anti-Copy Protection**
- Disable text selection pada seluruh halaman
- Mencegah copy-paste konten
- Mencegah drag & drop elemen

### 5. **Console Protection**
- Membersihkan console secara berkala (setiap 1 detik)
- Anti-debugging techniques
- Mencegah logging di console

### 6. **Security Headers (Vercel)**
- `X-Frame-Options: DENY` - Mencegah clickjacking
- `X-Content-Type-Options: nosniff` - Mencegah MIME sniffing
- `X-XSS-Protection` - Proteksi XSS
- `Content-Security-Policy` - Kontrol resource loading
- `Referrer-Policy: no-referrer` - Proteksi privacy

### 7. **Additional Protection**
- Anti-printing (halaman kosong saat di-print)
- Prevent iframe embedding
- Disable view source
- Automatic page clearing on DevTools detection

## ⚠️ Catatan Penting

**Proteksi ini TIDAK 100% aman!** Seseorang yang berpengalaman masih bisa:
- Menggunakan proxy/browser extension
- Disable JavaScript
- Menggunakan curl/wget untuk download source
- Menggunakan debugging tools yang lebih advanced

**Tujuan proteksi ini adalah:**
- Mempersulit user biasa untuk melihat code
- Mengurangi kemungkinan copy-paste langsung
- Memberikan lapisan keamanan dasar

## 🚀 Deployment di Vercel

1. Push ke GitHub repository
2. Connect dengan Vercel
3. Deploy otomatis dengan konfigurasi `vercel.json`
4. Security headers akan otomatis diterapkan

## 💡 Tips Keamanan Lebih Lanjut

Untuk keamanan maksimal, pertimbangkan:
1. **Minifikasi HTML/CSS/JS** - Gunakan build tools seperti Webpack
2. **Obfuscation** - Acak nama variabel dan fungsi
3. **Server-Side Rendering** - Gunakan framework seperti Next.js
4. **API Protection** - Jangan expose sensitive data di client-side
5. **Rate Limiting** - Batasi request ke server

## 📝 Lisensi & Copyright

© 2026 Aditya Novan Firmansyah. All rights reserved.

Unauthorized copying, modification, or distribution of this website's code is strictly prohibited.
