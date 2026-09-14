# Self-Hosted RTSP to HLS Live Streaming Server

Sebuah proyek infrastruktur *live streaming* mandiri (*self-hosted*) untuk mengonversi aliran video dari IP Camera (RTSP) menjadi format HTTP Live Streaming (HLS) menggunakan VPS Linux. Sistem ini dirancang untuk stabilitas siaran 24/7, terintegrasi dengan domain kustom, fitur pemulihan *error* otomatis, dan sertifikasi enkripsi SSL/TLS.

## 🚀 Arsitektur & Fitur Utama
* **Zero Third-Party Dependency:** Mengeliminasi kebutuhan layanan *cloud* berbayar dengan memproses tarikan media langsung di dalam server privat.
* **Auto-Recovery System:** Mengonfigurasi `TimeoutStopSec` dan `ExecStartPre` pada *daemon* Systemd untuk memastikan layanan memulihkan diri otomatis saat aliran jaringan dari lokasi kamera terputus (*anti-hang*).
* **Browser Caching Bypass:** Mengintegrasikan *cache buster* parameter dan Nginx *headers* ketat guna mencegah *buffering* statis pada *browser* klien.
* **Low Latency Optimized:** Memodifikasi opsi konfigurasi `hls.js` untuk meminimalkan latensi pemutaran.

## 🛠️ Teknologi yang Digunakan
* **OS Server:** Ubuntu/Debian (VPS)
* **Pemroses Media:** FFmpeg
* **Web Server:** Nginx
* **Antarmuka (Frontend):** HTML5, JavaScript (`hls.js`)
* **Manajemen Proses:** Systemd
* **Keamanan:** Certbot (Let's Encrypt SSL/TLS)

## ⚠️ Disclaimer Privasi
Repositori ini berfungsi murni sebagai demonstrasi teknis dan portofolio. Kredensial sensitif seperti alamat IP publik, pengaturan porta (port forwarding), kredensial autentikasi RTSP, dan nama domain otentik telah disensor dengan menggunakan *placeholder* (misal: `<DOMAIN_ANDA>`).