# Catat Pengeluaran — versi iPhone dari Windows

Ini **web app (PWA)**, bukan IPA native atau aplikasi App Store. Anda bisa menaruhnya di layar utama iPhone melalui Safari tanpa Mac. Kode situs boleh diunggah ke GitHub Pages; catatan pribadi **tidak diunggah ke repo** dan disimpan di penyimpanan browser pada iPhone. Tidak ada akun dan tidak ada sinkronisasi antarperangkat.

## Pasang dari PC Windows dan iPhone

1. Di Windows, ekstrak ZIP ini. Di dalamnya ada folder `CatatPengeluaranWeb` dengan `index.html`, `app.js`, `styles.css`, `sw.js`, `manifest.webmanifest`, `icons`, dan `.nojekyll`.
2. Buka **GitHub Desktop > File > New repository**. Isi nama, misalnya `catat-pengeluaran-iphone`, lalu klik **Create repository**. Pilih **Repository > Show in Explorer**.
3. Salin **semua isi** folder `CatatPengeluaranWeb` ke folder repositori yang terbuka. Jangan menyalin folder luar saja: `index.html` harus berada langsung di folder utama repositori.
4. Di GitHub Desktop isi Summary `Tambahkan aplikasi iPhone`, klik **Commit to main**, lalu **Publish repository**. Jika akun Anda memakai GitHub Free, pilih repo **Public** agar GitHub Pages tersedia. Hanya kode aplikasi yang terbuka untuk publik; jangan unggah JSON cadangan atau foto struk ke repositori.
5. Buka repositori di GitHub.com. Masuk **Settings > Pages**. Pada **Build and deployment**, pilih **Deploy from a branch**; pilih **main** dan **/(root)**, lalu klik **Save**. Tunggu sampai muncul alamat situs seperti `https://namaakun.github.io/catat-pengeluaran-iphone/`.
6. Di iPhone, buka alamat itu dengan **Safari**. Ketuk **Bagikan** (ikon kotak dengan panah) > **Add to Home Screen / Tambahkan ke Layar Utama** > aktifkan **Open as Web App** jika muncul > **Add / Tambah**. Jalankan dari ikon Catat Pengeluaran di layar utama.
7. Bila ingin memindahkan catatan Android, ekspor JSON di aplikasi Android, pindahkan file cadangan itu ke aplikasi **Files** di iPhone, lalu di aplikasi web pilih **Pengaturan > Impor JSON**. Impor mengganti data yang ada di iPhone. Lakukan impor dari ikon layar utama setelah pemasangan.

Aplikasi dapat dibuka tanpa internet setelah pernah dimuat lengkap sekali karena berkas aplikasi disimpan untuk offline. Kunjungi situs lagi saat online jika Anda menerbitkan pembaruan. Catatan lokal dan foto tetap bergantung pada data situs Safari; **ekspor JSON secara rutin**, terutama sebelum membersihkan data browser, mengganti iPhone, atau menghapus ikon aplikasi.

## Yang tersedia

Transaksi pemasukan dan pengeluaran, transfer internal, tanggal kalender, kategori baru yang otomatis disimpan, item favorit, catat cepat, jadwal rutin dan konfirmasi pembayaran, jeda/lewati periode, kalender dengan penanda pengeluaran, rekap diagram, target dan streak, foto struk sebagai bukti, tema terang/gelap, ekspor/impor JSON. Format cadangan dasar memakai struktur yang sama dengan aplikasi Android.

**Perbedaan dari aplikasi native:** tidak memakai Face ID/Touch ID. PIN web hanya mengunci tampilan; berkas data lokal dan JSON cadangan tidak terenkripsi. Semua perangkat mempunyai catatan masing-masing; tidak sinkron otomatis. Jangan gunakan mode Private Browsing untuk catatan utama.

## Memeriksa sebelum digunakan serius

Jalankan `node --check app.js`. Pemeriksaan logika lokal dilakukan untuk tanggal, pengulangan jadwal, kategori, dan jumlah keuangan. Belum diuji langsung di Safari iPhone dari lingkungan pengembangan ini; coba satu transaksi dan ekspor/impor contoh terlebih dahulu.
