# 🌴 Sistem Rekomendasi Nutrisi Tanaman untuk Iklim Khatulistiwa

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/username/repo/blob/main/LICENSE)
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)

Sistem rekomendasi nutrisi tanaman yang dirancang khusus untuk kondisi iklim khatulistiwa dengan suhu tinggi (>30°C). Proyek ini membantu petani menghindari overdosis nutrisi akibat penguapan tinggi dan stres panas.

![Preview Aplikasi](screenshot.png)
![{BC6D40B9-BA37-4B6A-A1DC-6BD37D67469C}](https://github.com/user-attachments/assets/f18ab457-f2e7-491e-9b9a-29fcb906fff7)
![{18605852-F602-42DB-9CEE-6CC0A95D6B86}](https://github.com/user-attachments/assets/dc8359f9-93da-4206-bbc4-df6c24ad2a22)

## 🌡️ Masalah Utama: Overdosis Nutrisi Akibat Suhu Tinggi

Di iklim khatulistiwa, suhu tinggi menyebabkan masalah unik pada nutrisi tanaman:

1. **Peningkatan Penguapan**:
   - Transpirasi tinggi menyebabkan akumulasi garam di zona perakaran
   - Konsentrasi nutrisi meningkat secara signifikan dalam waktu singkat

2. **Stres Termal pada Tanaman**:
   - Efisiensi penyerapan nutrisi menurun pada suhu >32°C
   - Resiko toksisitas amonia meningkat

3. **Gejala Overdosis**:
   - Daun kaku dan dingin (EC aman)
   - Daun lemas dan hangat (EC terlalu tinggi)
   - Ujung daun kuning pucat (overdosis garam)
   - Daun menggulung ke atas (stres panas akut)

## 🛠️ Solusi yang Diberikan

### 1. Penyesuaian EC dan PPM Berbasis Suhu
| Fase Pertumbuhan | EC Target (mS/cm) | Total PPM | Penyesuaian |
|------------------|-------------------|----------|-------------|
| Awal Vegetatif   | 0.4-0.5           | 200-250  | ▼ 60% dari standar |
| Vegetatif Intensif | 0.6-0.8         | 300-400  | ▼ 50% dari standar |
| Transisi Generatif | 0.8-1.0         | 400-500  | ▼ 55% dari standar |
| Generatif        | 1.0-1.2           | 500-600  | ▼ 65% dari standar |

**Formula Penyesuaian**: Setiap kenaikan 1°C di atas 32°C, turunkan EC tambahan 0.1 mS/cm

### 2. Formula Nutrisi Khatulistiwa
**Vegetatif**:
- Nitrogen (N): 25 ppm
- Kalium (K): 80 ppm
- Kalsium (Ca): 60 ppm
- Magnesium (Mg): 30 ppm

**Generatif**:
- Nitrogen (N): 20 ppm
- Kalium (K): 120 ppm (ditingkatkan untuk mitigasi panas)
- Fosfor (P): 25 ppm

> **Peringatan**: Hindari urea/NH₄⁺ >5ppm karena risiko toksisitas amonia di suhu tinggi

### 3. Protokol Aplikasi Harian
1. **Pagi (06:00-07:00)**:
   - Beri larutan nutrisi penuh (EC sesuai fase) 
   - Volume 20% lebih banyak
   
2. **Siang (10:00-11:00)**:
   - Flushing cepat dengan air bersih (EC 0) 
   - 100-200 mL/pot
   
3. **Sore (15:00-16:00)**:
   - Beri larutan nutrisi setengah konsentrasi 
   - Tambah asam humat 0.5%

### 4. Mitigasi Panas
| Teknik | Implementasi | Manfaat |
|--------|--------------|---------|
| Komposisi Media | Cocopeat 50%, Perlit 30%, Biochar 15% | Penahan air + penyerap garam |
| Pendinginan Pot | Aluminium foil + batang pisang kering | Pantulkan radiasi + insulasi |
| Naungan | Paranet 40-50% (jam 11-15) | Turunkan suhu 3-5°C |
| Penjadwalan | Siram saat suhu <30°C | Hindari stres panas |

## 🚑 Action Plan untuk Overdosis

### Tahap Akut (daun mengering):
1. Rendam pot dalam air bersih (30 menit)
2. Semprot daun dengan:
   - Air kelapa 100 mL/L 
   - Asam humat 2 mL/L 
   - Silika 1 mL/L
3. Naungi 70% selama 48 jam

### Pemulihan (3-7 hari):
1. Turunkan EC ke 0.4 mS/cm
2. Beri bakteri rhizobium
3. Naungi 50% selama 3 hari
4. Tambah frekuensi flushing siang hari

## 🚀 Cara Menggunakan

1. Clone repositori:
   ```bash
   git clone https://github.com/sekadau-online/abmixer.git
