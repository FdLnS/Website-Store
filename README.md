# FDLN Store – Digital Product Checkout (Next.js + Payment Gateway WBK)

Website sederhana untuk penjualan produk digital (contoh: Spotify, YouTube Premium)  
Menggunakan **Next.js 13/14 (App Router)** dan **integrasi Payment Gateway [WBK](https://pg.wbk.web.id/)** (fitur checkout QRIS/Ewallet otomatis).

---

## 🚀 Fitur

- ✅ Tampilkan produk digital beserta tipe & harga (homepage)
- ✅ Tombol "Pesan" tiap tipe produk, lanjut ke halaman checkout
- ✅ Halaman checkout: pilih produk, tipe, email, dan metode pembayaran
- ✅ Integrasi **Payment Gateway WBK** (QRIS, DANA, OVO, Gopay, ShopeePay)
- ✅ Bukti/instruksi pembayaran tampil otomatis (scan QR/dst)
- ✅ Responsive & mudah dikembangkan

---

## 🛠️ Instalasi & Jalankan

1. **Clone repo / salin source code:**
    ```bash
    git clone [repo-ini]
    cd [nama-folder]
    ```

2. **Install dependencies:**
    ```bash
    npm install
    ```

3. **Buat file `.env.local` di root project:**
    ```
    NEXT_PUBLIC_WBK_APIKEY=isi_apikey_wbk_kamu
    ```
    > Ganti dengan APIKEY milikmu dari dashboard WBK!

4. **Jalankan di mode development:**
    ```bash
    npm run dev
    ```

5. **Akses di browser:**  
   [http://localhost:3000](http://localhost:3000)

---

## 📁 Struktur Folder Utama

src/
app/
page.tsx # Homepage daftar produk
checkout/page.tsx # Halaman checkout
api/payments/route.ts # API route integrasi payment gateway
lib/products.ts # Data produk (bisa diganti sesuai kebutuhan)
components/Navbar.tsx # Navbar custom
.env.local # Simpan APIKEY WBK


---

## ⚡ Catatan Penggunaan

- **Jangan deploy dengan mode `next export`** — gunakan SSR/server (Vercel, Railway, VPS, dsb) agar API route berjalan!
- Payment Gateway WBK hanya untuk simulasi/testing (real payment, cek dashboard WBK kamu).
- Untuk keamanan, **jangan hardcode API key di client-side/JS** untuk produksi.

---

## 👨‍💻 Pengembangan Lanjutan

- Tambahkan fitur email notifikasi otomatis ke pembeli.
- Simpan riwayat transaksi ke database (Supabase/Firebase/dll).
- Tambahkan testimoni otomatis setelah pembayaran sukses.

---

## 📞 Kontak & Lisensi

Website ini dibuat untuk pembelajaran, tugas, dan demo portofolio.  
Lisensi: MIT

**Kontributor:**  
- FDLN Store (fdlnstore.xyz)  

---
