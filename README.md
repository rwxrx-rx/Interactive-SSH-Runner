# 🚀 Interactive SSH Runner (Termux / JuiceSSH)

[![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)](https://github.com/features/actions)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)](https://ubuntu.com/)
[![Telegram](https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://telegram.org/)
[![Termux](https://img.shields.io/badge/Termux-000000?style=for-the-badge&logo=gnu-bash&logoColor=white)](https://termux.dev/)

Ubah **GitHub Actions** menjadi **VPS Cloud Linux gratis berkinerja tinggi** yang dapat diakses dengan mudah dari perangkat seluler (Termux atau JuiceSSH) menggunakan `tmate` dan **Telegram Bot**.

Didesain khusus untuk keperluan kompilasi berat (Android Kernel & Recovery Build), *high-speed file mirroring*, hingga pengujian *script* Linux langsung dari HP.

---

## ✨ Fitur Utama

- ⚡ **Koneksi Instan via Telegram:** Kredensial SSH & Web Terminal dikirimkan secara otomatis ke Telegram begitu workflow berjalan.
- 💾 **Penyimpanan Ekstra (Maximized Disk Space):** Otomatis membersihkan *bloatware* bawaan runner untuk mendapatkan **~70 GB Disk Space Kosong** dan **4 GB Swap RAM**.
- 📱 **Mobile-Optimized:** Bekerja mulus di **Termux** (copy-paste instan) maupun **JuiceSSH**.
- 🛠️ **Bawaan Tool Lengkap:** Sudah terkonfigurasi dengan `aria2`, `speedtest-cli`, `fastfetch`, `htop`, `git`, `ccache`, `zip`, `unzip`, dan alat kompilasi lainnya.
- 📤 **Siap Mirroring Telegram:** Kompatibel dengan `telegram-upload` untuk *download & upload* file jumbo hingga 2 GB / 4 GB ke Telegram.
- 🛡️ **Sesi Stabil & Bersih:** Menggunakan *background monitoring loop* tanpa eror `not a terminal`, serta notifikasi otomatis saat sesi ditutup.

---

## 🛠️ Spesifikasi Runner

| Komponen | Spesifikasi |
| :--- | :--- |
| **OS** | Ubuntu Latest (64-bit) |
| **CPU** | 2 vCPU (Intel Xeon / AMD EPYC) |
| **RAM** | ~7 GB RAM + 4 GB Swap |
| **Storage** | ~70 GB SSD Free Space |
| **Network** | Up to 1–3 Gbps Symmetric Internet |
| **Batas Waktu** | Maksimal 6 jam per sesi (*GitHub limit*) |

---

## 🚀 Panduan Persiapan & Penggunaan

### 1. Tambahkan Repository Secrets

Sebelum menjalankan *workflow*, kamu perlu menambahkan **Bot Telegram** milikmu di repositori ini:

1. Buka repositori GitHub ini $\rightarrow$ **Settings** $\rightarrow$ **Secrets and variables** $\rightarrow$ **Actions**.
2. Klik **New repository secret** dan tambahkan dua variabel berikut:

| Secret Name | Deskripsi |
| :--- | :--- |
| `TELEGRAM_BOT_TOKEN` | Token Bot Telegram dari [@BotFather](https://t.me/BotFather) |
| `TELEGRAM_CHAT_ID` | Chat ID Telegram kamu dari [@userinfobot](https://t.me/userinfobot) |

---

### 2. Jalankan Workflow

1. Masuk ke tab **Actions** di repositori ini.
2. Pilih workflow **Interactive SSH Runner (Termux/JuiceSSH)** di panel sebelah kiri.
3. Klik tombol **Run workflow** $\rightarrow$ **Run workflow**.

---

### 3. Hubungkan via Termux atau JuiceSSH

1. Tunggu 10–15 detik hingga **Bot Telegram** mengirimkan pesan berisi kredensial SSH.
2. **Via Termux:**
   Salin baris perintah SSH dari Telegram, *paste* ke Termux, lalu tekan Enter.
   ```bash
   ssh <username>@<host>.tmate.io
   
