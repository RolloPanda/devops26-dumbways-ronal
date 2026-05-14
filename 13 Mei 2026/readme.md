                Internet
                    │
            Request dari User
                    │
             ┌─────────────┐
             │   Domain    │
             │ ade.xyz     │
             └──────┬──────┘
                    │
            Port 80 / 443
                    │
        ┌────────────────────┐
        │ Reverse Proxy      │
        │ Nginx              │
        └─────────┬──────────┘
                  │
      ┌───────────┴───────────┐
      │                       │
┌──────────────┐      ┌──────────────┐
│ Frontend App │      │ Backend App  │
│ React/Vue    │      │ Node.js API  │
│ Port 3000    │      │ Port 5000    │
└──────────────┘      └──────────────┘

Cara Kerja Reverse Proxy

Reverse Proxy adalah server perantara yang menerima request dari client lalu meneruskannya ke aplikasi backend.

Alur kerjanya:

User mengakses domain seperti ade.xyz
Request masuk ke server Nginx
Nginx membaca konfigurasi:
Jika request frontend → diarahkan ke port frontend
Jika request API → diarahkan ke backend
Backend memproses request
Hasil dikembalikan ke Nginx
Nginx mengirim response ke user
Fungsi Reverse Proxy

Beberapa fungsi reverse proxy:

Menyembunyikan port aplikasi backend
Menggunakan domain tanpa menampilkan port
Membagi traffic ke beberapa service
Menambah keamanan
Bisa digunakan untuk SSL/HTTPS
Mempermudah deployment