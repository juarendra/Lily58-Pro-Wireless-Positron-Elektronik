# ⌨️ ZMK Firmware untuk Lily58 Wireless

[![ZMK Build Status](https://github.com/juarendra/LILY58-ZMK-Config/actions/workflows/build.yml/badge.svg)](https://github.com/juarendra/LILY58-ZMK-Config/actions)

Repositori ini berisi konfigurasi khusus untuk *firmware* **ZMK** pada *keyboard split* **Lily58 Wireless**. Konfigurasi ini dirancang untuk memberikan pengalaman mengetik nirkabel yang stabil dan efisien menggunakan protokol Bluetooth Low Energy (BLE).

## 🛠️ Ringkasan Konfigurasi

| Item | Detail |
| :--- | :--- |
| **Keyboard** | Lily58 |
| **Konektivitas** | Wireless (Bluetooth Low Energy / BLE) |
| **Firmware** | ZMK (Zephyr Keyboard Firmware) |
| **Controller** | Nice!Nano v2 (atau yang kompatibel) |
| **Keymap File** | `config/lily58.keymap` |

## 💡 Keymap & Fitur Utama

Keymap ini dioptimalkan untuk produktivitas dengan memanfaatkan desain ergonomis 58 tombol milik Lily58.

### Lapisan (Layers)

| Layer | Nama | Deskripsi |
| :--- | :--- | :--- |
| **Layer 0** | `BASE` | Keymap utama (QWERTY / [Custom Layout]) |
| **Layer 1** | `LOWER` | Simbol, angka, dan kontrol dasar. |
| **Layer 2** | `RAISE` | Navigasi (Arrow keys), Media, dan kontrol sistem. |
| **Layer 3** | `ADJ` | Pengaturan Bluetooth (Profiles, Clear) dan Reset. |

### Fitur Unggulan

* **Wireless First:** Optimasi penggunaan daya baterai untuk daya tahan maksimal.
* **Split Sync:** Sinkronisasi profil Bluetooth yang lancar antara sisi kiri (Master) dan kanan.
* **Mod-Tap/Layer-Tap:** Penggunaan tombol multifungsi untuk efisiensi maksimal pada jempol.

## ⚙️ Cara Membangun (Build) dan Mendapatkan Firmware

*Firmware* ini dibangun secara otomatis oleh **GitHub Actions** setiap kali ada perubahan pada file di dalam folder `config/`.

1.  **Edit Keymap:** Ubah *layout* Anda di `config/lily58.keymap`.
2.  **Commit:** Lakukan *commit* dan *push* perubahan ke GitHub.
3.  **Akses Actions:** Buka tab [Actions](https://github.com/juarendra/LILY58-ZMK-Config/actions) pada repositori ini.
4.  **Download:** Pilih *workflow run* terbaru yang berhasil (tanda centang hijau ✅), gulir ke bawah ke bagian **Artifacts**, dan unduh **`firmware.zip`**.

*File `firmware.zip` akan berisi dua file: `lily58_left-nicenano_v2-zmk.uf2` dan `lily58_right-nicenano_v2-zmk.uf2`.*

## ⚡ Cara Flash Firmware (Nice!Nano)

Langkah-langkah untuk memasang *firmware* ke *controller* Anda:

1.  **Persiapan:** Pastikan baterai terhubung (jika nirkabel) atau gunakan daya via USB.
2.  **Hubungkan:** Sambungkan sisi **kiri** ke komputer menggunakan kabel USB-C.
3.  **Bootloader Mode:** Tekan tombol **`RESET`** pada *controller* **dua kali dengan cepat**. *Controller* akan terbaca sebagai *drive* eksternal bernama `NICENANO`.
4.  **Flash Sisi Kiri:** *Drag and drop* file `lily58_left-nicenano_v2-zmk.uf2` ke *drive* tersebut. *Controller* akan otomatis keluar dan *reboot*.
5.  **Flash Sisi Kanan:** Ulangi proses yang sama untuk sisi kanan menggunakan file `lily58_right-nicenano_v2-zmk.uf2`.
6.  **Pairing:** Nyalakan kedua sisi, pasangkan (pair) via Bluetooth ke komputer/laptop Anda.

## 🤝 Kontribusi

Jika Anda menemukan masalah atau ingin memberikan saran:

* **Bug Report:** Silakan buka [Issues](https://github.com/juarendra/LILY58-ZMK-Config/issues).
* **Pull Request:** Kirimkan [Pull Requests](https://github.com/juarendra/LILY58-ZMK-Config/pulls) untuk perbaikan keymap atau fitur.

---

*Dibuat oleh [@juarendra](https://github.com/juarendra). Terakhir diperbarui: 17 Januari 2026*