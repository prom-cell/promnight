# Cara mengubah tanggal acara (± 1 menit)

Cukup ubah **satu baris** di `index.html`. Semua tanggal, nama hari, countdown, rundown, dan tombol "Simpan di kalender" ikut berubah otomatis. Link undangan dan shortlink **tidak berubah**.

## Langkah

1. Buka **https://github.com/prom-cell/promnight/blob/main/index.html** (pastikan login akun `prom-cell`).
2. Klik ikon **pensil (Edit this file)** di kanan atas.
3. Tekan **Ctrl + F** (di HP: menu ⋮ → Find), cari: `TANGGAL_MULAI`
4. Ubah tanggal di baris ini:

   ```js
   const TANGGAL_MULAI = "2026-11-02";
   ```

   Isi dengan tanggal **hari pertama**, format `"TAHUN-BULAN-TANGGAL"` (pakai tanda kutip, 2 digit untuk bulan dan tanggal).

   | Acara | Isi baris menjadi |
   |---|---|
   | 2–3 November 2026 | `const TANGGAL_MULAI = "2026-11-02";` |
   | 4–5 November 2026 | `const TANGGAL_MULAI = "2026-11-04";` |
   | 9–10 November 2026 | `const TANGGAL_MULAI = "2026-11-09";` |
   | 30 Nov – 1 Des 2026 | `const TANGGAL_MULAI = "2026-11-30";` |

5. Klik **Commit changes…** → **Commit changes**.
6. Tunggu 1–2 menit, lalu buka undangan dan refresh. Selesai.

## Yang ikut berubah otomatis

- Tanggal di halaman depan dan strip info (contoh: `Rab – Kam · 4–5 Nov 2026`)
- Countdown menuju check-in (jam check-in tetap **14.00 WIB**)
- Teks "Menuju check-in Rabu, 4 November 2026…"
- Judul rundown hari 1 dan hari 2
- Info check-in di bagian lokasi
- Tombol **Simpan di kalender**

## Yang perlu diubah sendiri (di luar website)

- **Pesan WhatsApp di spreadsheet RSVP** → tab *Link Undangan*, ganti teks di sel **K2** (contoh `4–5 November 2026`). Semua pesan dan tombol Kirim ikut berubah.
- Pesan/caption yang sudah terlanjur dikirim manual ke grup.

## Kalau ada yang salah

- Halaman kosong/tanggal tidak berubah → cek tanda kutip dan titik koma: `"2026-11-04";`
- Bisa dikembalikan: buka tab **History** file `index.html` di GitHub, pilih versi sebelumnya.
