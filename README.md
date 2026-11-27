# StockLab

Game kartu saham digital bertema Nabung Saham. Mainkan sendiri melawan bot, bersama teman di satu perangkat, atau online lewat ruangan.

Tujuan: setelah 6 ronde, kumpulkan **koin sebanyak mungkin** lewat beli-jual saham dan efek kartu. Pemain dengan skor akhir tertinggi menang.

---

## Isi permainan

- **Pemain:** 2 sampai 5. Sebagian bisa manusia, sisanya bot.
- **5 sektor saham:** Agrikultur, Keuangan, Konsumer, Tambang, dan Reksa Dana.
- **Kartu aksi:** 60 kartu (12 per sektor). Kartu aksi bisa dipakai sebagai efek atau disimpan sebagai saham.
- **Kartu ekonomi:** tiap sektor biasa (selain Reksa Dana) punya tumpukan 6 kartu ekonomi tertutup. Tumpukan ini menggerakkan harga.
- **Kartu utang:** 6 kartu untuk semua pemain.
- **Bank:** karakter bankir yang membacakan kejadian di game.

## Persiapan

- Tiap pemain mulai dengan **15 koin** dan belum punya saham.
- Harga awal 4 sektor biasa adalah **5**.
- Urutan sektor di papan diacak tiap game, dengan Reksa Dana selalu di tengah.
- **Harga Reksa Dana** tidak bergerak sendiri. Harganya adalah rata-rata (dibulatkan ke bawah) dari dua sektor di kiri dan kanannya.
- Harga sektor biasa selalu berada di antara **1 dan 9**.

---

## Alur satu ronde

Game berlangsung **6 ronde**. Tiap ronde punya lima langkah berurutan.

### 1. Buka kartu aksi

Bank membuka kartu aksi sebanyak **2 x jumlah pemain**. Semua pemain bisa melihat kartunya sebelum bidding.

### 2. Bidding

- Tiap pemain menawar **rahasia** 1 sampai 10 koin (tidak boleh lebih dari koin yang dimiliki). Waktunya 5 detik. Pemain yang koinnya habis tidak menawar.
- Semua tawaran dibuka bersamaan, lalu koin tawaran **dibayar ke Bank** (hilang).
- **Urutan main** ditentukan dari tawaran terbesar. Kalau seri, urutan ronde sebelumnya dipakai. Urutan ini berlaku untuk fase aksi, jual, dan efek Pajak Jalan.

### 3. Aksi

- Pemain bergantian sesuai urutan, mengambil **1 kartu aksi** tiap giliran, sampai kartu habis (rata-rata 2 kartu per pemain). Waktu memilih 10 detik.
- Setelah mengambil kartu, pilih salah satu:
  - **Simpan:** kartu jadi 1 saham di sektor kartu itu.
  - **Aktifkan:** efek kartu dijalankan, lalu kartu dibuang.

| Kartu | Saat diambil | Efek jika diaktifkan |
|---|---|---|
| **Quickbuy** | - | Ambil dan simpan 2 kartu saham lagi dari kartu yang tersisa. Giliran Anda langsung berakhir dan Anda tidak mengambil giliran lagi di ronde itu. |
| **Rumor** | - | Naikkan atau turunkan harga 1 sektor sebesar 1, maksimal 2 kali (boleh berhenti di 1 kali). Harga tetap di 1 sampai 9, jadi tidak bisa memicu crash atau split. |
| **Trading Fee** | Wajib bayar 1 koin untuk tiap saham sektor itu yang Anda punya, termasuk kartu ini. | Langsung jual semua saham sektor itu di harga sekarang. |
| **Akuisisi** | - | Ambil 1 saham pemain lain (bukan Reksa Dana). Syaratnya jumlah saham Anda di sektor itu harus lebih banyak atau sama. Pemain itu menerima koin sebesar setengah harga saham (dibulatkan ke atas). Kalau tidak ada target, kartu tidak bisa diaktifkan. |
| **Info Bursa** | - | Intip kartu ekonomi teratas dari 2 sektor pilihan Anda (rahasia) dan terima 2 koin dari Bank. |

**Kartu utang:** saat diminta memilih (kecuali saat bidding), Anda bisa menekan tombol **Ambil Utang +10** untuk langsung dapat 10 koin. Konsekuensinya **-13 skor di akhir** untuk tiap kartu utang. Persediaan hanya 6 kartu untuk semua pemain.

### 4. Jual

Sesuai urutan, tiap pemain memilih **satu jenis saham** untuk dijual (boleh berapa pun lembar) di harga sekarang, atau **Hold** (tidak menjual apa-apa).

### 5. Ekonomi

Bank membuka kartu ekonomi teratas di tiap sektor biasa, dari kiri ke kanan, lalu efeknya dijalankan. Setelah semuanya selesai, harga Reksa Dana dihitung ulang.

**Kartu pergerakan harga**

| Kartu | Jumlah per tumpukan (36 kartu, 24 dipakai) | Efek |
|---|---|---|
| Naik | 5 | Harga sektor +1 |
| Melaju | 3 | Harga sektor +2 |
| Boom | 1 | Harga sektor +3 |
| Anjlok | 5 | Harga sektor -1 |
| Terjun | 3 | Harga sektor -2 |
| Crash | 1 | Harga sektor -3 |
| Dividen | 5 | Tiap pemain terima 1 koin per saham sektor itu |
| Sideways | 3 | Tidak terjadi apa-apa |
| Kartu spesial | 10 (masing-masing 1) | Lihat tabel di bawah |

**Kartu spesial**

| Kartu | Efek |
|---|---|
| **Merger** | Ikut efek kartu ekonomi di sebelah kanannya (atau kiri jika paling kanan). |
| **Restrukturisasi Ekonomi** | Harga semua sektor kembali ke 5 dan efek kartu ekonomi lain di ronde itu dibatalkan. |
| **World Oil Regulation** | Kartu ini bertukar tempat dengan kartu ekonomi di sektor Tambang, dan harga Tambang naik 1. |
| **Extra Fee** | Semua pemain membayar 1 koin untuk tiap saham sektor itu yang dimiliki. |
| **Tax Amnesty** | Harga sektor naik 1, dan semua kenaikan di sektor lain ronde ini bertambah 1. |
| **Penerbitan Saham Baru** | Pemilik saham sektor itu mendapat 1 saham tambahan, lalu harga sektor turun 1. |
| **Resesi** | Dijalankan paling awal. Semua harga di atas 5 turun 1. |
| **Pajak Jalan** | Tiap pemain membayar koin sebanyak nomor urutannya (urutan 1 bayar 1 koin, urutan 2 bayar 2 koin, dan seterusnya). |
| **Buyback** | Harga sektor naik 1 (maks 9), semua pemilik menjual semua sahamnya di harga itu, lalu harga kembali ke 5. |
| **Stimulus Ekonomi** | Dijalankan paling akhir. Semua harga di bawah 5 naik 1. |

**Batas harga**

- Harga mencapai **10 atau lebih -> Stock Split:** harga kembali ke 5 dan jumlah saham semua pemain di sektor itu **dua kali lipat**.
- Harga mencapai **0 atau kurang -> Stock Crash:** semua pemain **kehilangan seluruh saham** sektor itu, dan harga dipulihkan ke 3.

Koin yang harus dibayar (Extra Fee, Pajak Jalan, dan sebagainya) tidak bisa membuat koin pemain menjadi minus.

---

## Akhir permainan dan skor

Setelah ekonomi ronde 6, semua saham **dijual paksa** di harga akhir.

**Skor = koin - (13 x jumlah kartu utang)**

Skor tertinggi menang. Layar juara menampilkan podium dan peringkat lengkap.

---

## Bot dan profil

Bot punya gaya main yang berbeda: **Agresif**, **Hati-hati**, **Kolektor**, dan **Analis**. Gaya ini terlihat dari cara mereka menawar, mengambil kartu utang, dan menjual. Pemain manusia bisa memilih avatar profil di layar persiapan.

## Mode online

- **Buat ruangan:** pilih maksimal 2 sampai 5 pemain, ruangan publik atau privat, dan boleh mengisi kursi kosong dengan bot. Ruangan punya kode 6 huruf untuk dibagikan ke teman.
- Pemain yang keluar atau refresh bisa memakai tombol **Gabung kembali** di layar awal untuk kembali ke kursinya.
- Host yang refresh bisa memakai **Lanjutkan game**. Ronde yang sedang berjalan diulang dari awal.
- Pemain yang tidak merespons (waktu habis atau terputus) diberi tanda **AFK**. Pilihannya diambil acak atau diganti bot sampai ia kembali.

## Tampilan dan suara

- Bisa dimainkan di laptop maupun HP.
- Bank membacakan kejadian dengan suara. Tombol 🔊 mematikan semua suara dan efek.
- Avatar bank ikut bicara dan bergerak sesuai kejadian.
