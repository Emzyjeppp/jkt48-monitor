# 🔴 JKT48 Live Ticket Monitor Dashboard

Aplikasi web dashboard berbasis client-side untuk memantau kuota dan sisa stok tiket *exclusive event* JKT48 secara otomatis dan *real-time*. Sistem ini memanfaatkan **GitHub Actions** sebagai bot otomatis di latar belakang untuk memperbarui data tanpa perlu melakukan *copy-paste* JSON secara manual.

## 🚀 Fitur Utama

- **Live Auto-Fetch (Tanpa Copas):** Menggunakan GitHub Actions untuk melakukan sinkronisasi data dari API resmi JKT48 secara otomatis.
- **Smart Sorting:** Angka sisa tiket/kuota member yang paling sedikit (hampir *sold out*) otomatis diurutkan ke paling atas untuk mempermudah pemantauan saat *war* tiket.
- **Live Search Filter:** Mempermudah pencarian sesi atau nama oshi secara instan tanpa perlu memuat ulang halaman web.
- **Visual Badge Status:** Menampilkan penanda status kuota secara dinamis (*Tersedia*, *Menipis* `< 5`, atau *SOLD OUT*).
- **Zero CORS Error:** Karena data di-generate ke dalam file internal repositori (`data.json`), web aman dari pemblokiran *CORS Policy* browser.

---

## 🛠️ Struktur Repositori

```text
├── .github/
│   └── workflows/
│       └── cron.yml       # Bot otomatis GitHub Actions (Setiap 5 menit)
├── index.html             # Tampilan dashboard utama (GitHub Pages)
├── data.json              # Output data kuota tiket terformat (Auto-generated)
└── README.md              # Dokumentasi proyek