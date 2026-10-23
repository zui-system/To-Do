# ZUI TO-DO 26.01 — yang baru dan cara pasang

## Isi paket
| File | Fungsi |
|---|---|
| `index.html` | Aplikasi Zui To-Do 26.01 |
| `firestore.rules` | Aturan Firestore project **zui-todo** (wajib diterbitkan, lihat langkah 1) |

## Yang berubah
1. **Bahasa**: semua menu, tampilan (Hari ini, Papan, Kalender, Ringkasan), lembar detail tugas, nama hari dan bulan kini ikut pilihan Indonesia / Melayu / English.
2. **Tema spesial** (Pengaturan → Tema spesial): 8 tema siap pakai (Zui, Laut, Hutan, Senja, Mawar, Lavender, Kopi, Grafit) untuk semua paket. **Racik sendiri** (paket Pro & Bisnis): warna utama, warna penanda hari ini, latar (netral/berwarna/kertas), huruf, ukuran teks, sudut. Tersimpan di akun pengguna.
3. **Paket & chat tersambung ke Zui Admin** dengan pola yang sama seperti ZUI KONTRAKTOR dan ZUI JURNAL:
   - Percobaan 14 hari (semua fitur Bisnis) mulai 18 Okt 2026, tenggang 3 hari, lalu tugas **hanya-baca**.
   - Paket: **Starter** (semua tampilan, target, sinkron, 8 tema, 5 kategori), **Pro** (+ kategori hingga 50, racik tema sendiri, ekspor CSV), **Bisnis** (+ cadangkan & pulihkan JSON, prioritas chat).
   - Pengguna memilih Rupiah (QRIS) atau Ringgit (DuitNow), membayar, lalu mengirim nomor referensi → masuk **Antrean** Zui Admin.
   - Chat dengan admin (bisa kirim foto bukti) → masuk **Pesan** Zui Admin.
4. **Tombol Keluar** dipindah ke pojok kanan atas (ketuk dua kali untuk keluar). Tombol keluar di Pengaturan dan Profil dihapus.
5. **Halaman terisi**: FAQ, Syarat & Ketentuan, Kebijakan Privasi, Kelola langganan, Berbagi dengan teman (WhatsApp, Telegram, Facebook, X, LinkedIn, Email, SMS, salin tautan), Umpan balik (email info.zuisystem@gmail.com + chat admin).
6. **Bawah menu**: "Zui To-Do versi 26.01 · Aplikasi Zui To-Do dikelola oleh Zui System · PT. Zaor Utama Indonesia".

## Langkah pasang
1. Firebase Console project **zui-todo** → Firestore Database → Rules → hapus isi lama, tempel seluruh `firestore.rules` → **Publish**. Tanpa ini langganan dan chat ditolak.
2. Authentication → Settings → Authorized domains → pastikan domain To-Do dan `admin.zuisystem.com` ada.
3. Unggah `index.html` ke repo GitHub Pages Zui To-Do.
4. Unggah ulang Zui Admin 2.2 (lihat PANDUAN.md di dalamnya), lalu atur harga, QRIS dan DuitNow di **Harga → ZUI TO-DO**.
5. Uji: daftar akun baru di To-Do → Pengaturan → Kelola langganan → kirim permintaan → muncul di Antrean Zui Admin → Aktifkan → status di To-Do berubah jadi paket aktif.

## Catatan
- Alamat yang dibagikan tombol Berbagi: alamat situs tempat To-Do dibuka; bila dibuka di luar situs (mis. pratinjau), memakai `https://todo.zuisystem.com`. Ubah `APP_URL` di `index.html` bila alamatnya lain.
- Harga awal To-Do ada di `index.html` (`DEFP`, `DEFPM`) dan `config.js` Zui Admin (`hargaAwal`). Setelah harga disimpan dari Zui Admin, keduanya memakai harga dari Zui Admin.
- Teks legal (Syarat & Ketentuan, Kebijakan Privasi, Kebijakan Pengembalian Dana, Kontak & Alamat) ada di `DOCS` dalam `index.html` (Indonesia, Melayu, English) dan sama isinya dengan `LEGAL.md`. Bila salah satu diubah, samakan yang lain. Tabel harga di Kebijakan Pengembalian Dana memakai harga langsung dari Zui Admin.
