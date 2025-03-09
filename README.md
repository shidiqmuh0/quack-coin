# Quack Coin Automate Claim

Bookmarklet ini dibuat untuk mengotomatisasi klik pada tombol "Drop Quack Coin" setiap detik dan secara otomatis berhenti ketika nilai koin pada halaman mencapai 0.

## Cara Kerja
- **Klik Otomatis:** Bookmarklet akan mencari tombol dengan kelas tertentu dan mengkliknya setiap detik.
- **Pengecekan Nilai Koin:** Sebelum mengklik, bookmarklet akan mengecek nilai koin yang terdapat di dalam elemen `<span>` pada link tertentu.
- **Berhenti Otomatis:** Jika nilai koin mencapai 0, proses klik otomatis akan berhenti.

## Cara Menggunakan

1. **Buat Bookmark Baru:**
   - Buka browser Anda (Chrome, Firefox, Edge, dll.).
   - Tambahkan bookmark baru.
   - Beri nama bookmark tersebut, misalnya `Quack Coin Automate Claim`.

2. **Salin dan Tempel Kode Bookmarklet:**
   - Salin kode di bawah ini:
     ```js
     javascript:(function(){const tombol=document.querySelector('button.inline-flex.group');const spanKoin=document.querySelector('a.flex.items-center.gap-2.max-sm\\:hidden span.font-bold');function getNilaiKoin(){return parseInt(spanKoin.textContent)||0;}const intervalKlik=setInterval(function(){const nilaiKoin=getNilaiKoin();if(nilaiKoin===0){clearInterval(intervalKlik);console.log('Nilai koin sudah 0. Proses berhenti.');return;}tombol.click();console.log('Tombol diklik. Nilai koin saat ini:',nilaiKoin);},1000);})();
     ```
   - Tempel kode tersebut ke dalam kolom URL atau alamat dari bookmark yang baru dibuat.

3. **Jalankan Bookmarklet:**
   - Buka halaman website yang memuat tombol "Drop Quack Coin" dan elemen nilai koin.
   - Klik bookmark `Quack Coin Automate Claim`.
   - Bookmarklet akan mulai mengklik tombol secara otomatis setiap detik.
   - Proses akan berhenti secara otomatis ketika nilai koin mencapai 0.

## Catatan
- **Ketersediaan Elemen:** Pastikan bahwa elemen tombol dan nilai koin sudah ada dan terlihat pada halaman sebelum menjalankan bookmarklet.
- **Penggunaan yang Tepat:** Bookmarklet ini dirancang untuk digunakan pada halaman web tertentu. Jika struktur halaman berubah, bookmarklet mungkin perlu disesuaikan.
- **Debugging:** Pesan log akan muncul di konsol browser (buka Developer Tools) untuk membantu memantau proses dan nilai koin saat ini.

Selamat mencoba dan semoga berhasil!
