# 🔭 RukyatVision
**Simulator Visibilitas Hilal Digital berbasis Web**  
*by Ika · © 2026 · MIT License*

---

## 📖 Tentang

**RukyatVision** adalah simulator rukyat hilal digital berbasis web yang dapat memprediksi kemungkinan visibilitas hilal (bulan sabit muda) secara otomatis berdasarkan lokasi GPS pengamat, waktu nyata, posisi bulan, dan kondisi cuaca.

Dibangun menggunakan algoritma astronomi ilmiah yang sama dengan yang digunakan lembaga astronomi internasional:

- 🌙 **Algoritma Chapront** — perhitungan posisi bulan dengan 32 suku koreksi (akurasi ~0.1°)
- 📐 **Model Yallop (1997)** — kriteria visibilitas hilal kelas A–F dari HMNAO Inggris
- 🌍 **Koreksi Parallax Topocentric** — koreksi posisi bulan berdasarkan lokasi pengamat di permukaan bumi
- 🌤️ **Data Cuaca Real-time** — via Open-Meteo API (cloud cover, visibilitas, kode cuaca)

---

## ✨ Fitur Utama

| Fitur | Keterangan |
|---|---|
| 📍 GPS Otomatis | Deteksi lokasi pengamat secara otomatis via browser |
| 🕐 Waktu Real-time | Menggunakan tanggal dan jam perangkat saat ini |
| 🌙 Posisi Bulan Presisi | Algoritma Chapront + koreksi parallax topocentric |
| 🌤️ Cuaca Real-time | Data atmosfer langsung dari Open-Meteo |
| 📊 Model Yallop | Nilai *q* dan kelas visibilitas A–F |
| 🔭 Tampilan Teropong | Visualisasi hilal di layar teropong digital |
| 🎛️ Parameter Manual | Semua slider bisa diatur manual |

---

## 🚀 Cara Penggunaan

### Cara 1 — Buka Langsung (Tanpa Install)
1. Download file `rukyatvision_v2.html`
2. Buka menggunakan **Google Chrome** (direkomendasikan)
3. Klik **"⟳ Deteksi Ulang"**
4. Izinkan akses lokasi saat browser meminta
5. Tunggu deteksi GPS, posisi bulan, dan cuaca selesai
6. Baca hasil prediksi visibilitas hilal (kelas A–F)

### Cara 2 — GitHub Pages (Online)
Akses langsung di: `https://chikaa-ops.github.io/rukyatvision/`  
*(Tidak perlu install apapun)*

---

## 🌐 Kompatibilitas Browser

| Browser | GPS | Cuaca | Canvas | Status |
|---|---|---|---|---|
| Google Chrome | ✅ | ✅ | ✅ | **Direkomendasikan** |
| Microsoft Edge | ✅ | ✅ | ✅ | Bisa |
| Mozilla Firefox | ✅ | ⚠️ | ✅ | Perlu server lokal |
| Safari | ✅ | ❌ | ✅ | Terbatas |

---

## 📐 Dasar Ilmiah

### Kriteria Visibilitas Yallop (1997)

| Kelas | Nilai q | Keterangan |
|---|---|---|
| **A** | q ≥ 0.216 | Mudah terlihat mata telanjang |
| **B** | q ≥ −0.014 | Terlihat mata telanjang, kondisi baik |
| **C** | q ≥ −0.160 | Perlu alat optik, bisa konfirmasi mata telanjang |
| **D** | q ≥ −0.232 | Hanya dengan binokuler atau teleskop |
| **E** | q ≥ −0.293 | Tidak terlihat meski dengan teleskop |
| **F** | q < −0.293 | Di bawah batas absolut visibilitas |

**Rumus q Yallop:**
```
q = (ARCV − (11.8371 − 6.3226·W + 7.1651·W² − 0.7307·W³)) / 10
```
- `ARCV` = Arc of Vision (beda ketinggian bulan − matahari)
- `W` = lebar sabit topocentric (arcmenit)

---

## 📚 Referensi Ilmiah

- Yallop, B.D. (1997). *A Method for Predicting the First Sighting of the New Crescent Moon.* NAO Technical Note No. 69. HM Nautical Almanac Office.
- Chapront, J. & Chapront-Touzé, M. (1991). *Lunar Tables and Programs from 4000 B.C. to A.D. 8000.* Willmann-Bell.
- Odeh, M.S. (2006). New Criterion for Lunar Crescent Visibility. *Experimental Astronomy*, 18, 39–64.
- Meeus, J. (1998). *Astronomical Algorithms* (2nd ed.). Willmann-Bell.
- Ilyas, M. (1994). Lunar Crescent Visibility Criterion and Islamic Calendar. *QJRAS*, 35, 425–461.

---

## ⚠️ Keterbatasan

- Akurasi posisi bulan ~0.1° (bukan ephemeris JPL level)
- Data cuaca dari model numerik, bukan pengukuran langsung
- Tidak menggantikan rukyat lapangan secara fisik
- Untuk penetapan awal bulan resmi, tetap ikuti keputusan sidang isbat Kemenag RI

---

## 📄 Lisensi

```
MIT License

Copyright (c) 2026 Ika

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Kredit

Dikembangkan oleh **Ika** sebagai bagian dari penelitian visibilitas hilal berbasis komputasi.  
Data cuaca disediakan oleh [Open-Meteo](https://open-meteo.com) (CC BY 4.0).

---

*"Melihat hilal bukan sekadar soal mata, tapi juga soal ilmu."* 🌙
