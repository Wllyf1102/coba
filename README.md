# Website Form ke Google Sheets

Ini contoh website sederhana HTML + JS yang bisa submit data langsung ke Google Sheets via Google Apps Script Web App.

## Cara pakai
1. Buat Google Spreadsheet baru, sheet bernama `Sheet1` dengan header: `Nama | Email | Pesan | Timestamp`.
2. Buat Apps Script Web App dengan kode `doPost` (lihat contoh di repo).
3. Deploy Web App, copy URL.
4. Ganti `https://script.google.com/macros/s/AKfycbyjKwzUATikFIQEUDmyBSv2Ki6kKRanhU8dbFsxc2qgFmxSKz0XQp10EOav5UjJ3H-iFg/exec` di `index.html` dengan URL Web App.
5. Upload repo ke GitHub, aktifkan GitHub Pages.
6. Tes submit form → data masuk ke Google Sheet.
