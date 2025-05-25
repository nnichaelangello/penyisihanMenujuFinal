# Pendahuluan Kompetisi Tahap Penyisihan: Prediksi Mobilitas Urban Cerdas

## Latar Belakang

Dalam ekosistem kota cerdas (*smart city*), mobilitas urban yang efisien dan berkelanjutan merupakan fondasi untuk meningkatkan kualitas hidup, mengurangi kemacetan, dan meminimalkan dampak lingkungan. Dengan pertumbuhan populasi, diversifikasi aktivitas urban, dan variabilitas faktor eksternal, prediksi pola mobilitas menjadi kunci untuk mengoptimalkan sistem transportasi umum. Pendekatan berbasis kecerdasan buatan (AI) memungkinkan analisis data yang kompleks untuk memprediksi jumlah perjalanan harian, mendukung perencanaan transportasi yang responsif dan ramah lingkungan.

Tahap penyisihan kompetisi ini menantang peserta untuk mengembangkan model prediktif berbasis AI guna memprediksi jumlah perjalanan harian menggunakan transportasi umum di berbagai zona kota. Dataset yang disediakan mencerminkan dinamika mobilitas urban dalam sebuah kota fiktif, dengan sumber data yang beragam dan kompleks. Peserta diharapkan untuk menganalisis data secara mendalam, mengidentifikasi pola yang relevan, dan menghasilkan prediksi yang akurat. Tahap ini dirancang untuk mengasah kemampuan peserta dalam menangani data multivariabel, menavigasi ketidaksempurnaan data, dan mengembangkan solusi inovatif dalam konteks masyarakat cerdas (*smart society*).

## Rumusan Masalah

Kompetisi ini berfokus pada prediksi jumlah perjalanan harian (dalam ribuan) menggunakan transportasi umum di berbagai zona kota berdasarkan informasi yang tersedia. Peserta diharapkan menjawab pertanyaan berikut:

1. Bagaimana data yang disediakan dapat dimanfaatkan untuk membangun model prediktif yang akurat dan andal?
2. Fitur mana yang paling memengaruhi jumlah perjalanan, dan bagaimana hubungan antar fitur dapat dioptimalkan untuk meningkatkan performa model?
3. Bagaimana solusi teknis yang dikembangkan dapat mendukung pengelolaan mobilitas urban dalam konteks kota cerdas?

Penilaian dilakukan melalui platform Kaggle berdasarkan akurasi prediksi pada data pengujian, menggunakan metrik *Root Mean Squared Error* (RMSE). 

$$\text{RMSE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2}$$

Peserta didorong untuk menunjukkan kreativitas, ketelitian analisis, dan pemahaman konteks untuk menghasilkan solusi yang kompetitif.

## Informasi Dataset

Dataset terdiri dari 16 file CSV pelatihan yang terbagi dalam empat kategori (Demografi, Aktivitas Urban, Cuaca, dan Infrastruktur Transportasi), serta file pengujian (`mobility_test.csv`). Dataset ini dirancang untuk mensimulasikan skenario mobilitas urban yang realistis namun menantang. Peserta diharapkan untuk mengeksplorasi dataset secara mandiri guna mengidentifikasi fitur dan sumber data yang relevan untuk prediksi jumlah perjalanan harian.

### 1. Kategori Demografi
Berisi informasi tentang karakteristik penduduk di setiap zona kota.

- **File**:
  - `resident_data.csv`
  - `workforce_data.csv`
  - `education_data.csv`
- **Kolom Umum** (bervariasi per file):
  - `zone_id`: Identifikasi unik untuk setiap zona.
  - `resident_count`: Jumlah penduduk.
  - `age_group`: Distribusi kelompok usia (kategorikal).
  - `employment_rate`: Tingkat pekerjaan.
  - `education_level`: Tingkat pendidikan rata-rata.
  - `commute_preference`: Preferensi moda transportasi (kategorikal).

### 2. Kategori Aktivitas Urban
Berisi informasi tentang aktivitas ekonomi dan sosial harian di setiap zona.

- **File**:
  - `business_activity.csv`
  - `event_data.csv`
  - `tourism_data.csv`
  - `traffic_data.csv`
- **Kolom Umum** (bervariasi per file):
  - `zone_id`: Identifikasi unik untuk setiap zona.
  - `date`: Tanggal pengukuran.
  - `business_density`: Kepadatan bisnis.
  - `event_count`: Jumlah acara sosial atau budaya.
  - `tourist_visits`: Jumlah kunjungan wisatawan.
  - `traffic_congestion`: Tingkat kemacetan (kategorikal).

### 3. Kategori Cuaca
Berisi informasi cuaca harian yang dapat memengaruhi pola mobilitas.

- **File**:
  - `weather_conditions.csv`
  - `air_quality.csv`
- **Kolom Umum** (bervariasi per file):
  - `zone_id`: Identifikasi unik untuk setiap zona.
  - `date`: Tanggal pengukuran.
  - `temperature`: Suhu rata-rata harian.
  - `precipitation`: Curah hujan harian.
  - `air_quality_index`: Indeks kualitas udara.

### 4. Kategori Infrastruktur Transportasi
Berisi informasi tentang infrastruktur dan layanan transportasi.

- **File**:
  - `transit_stations.csv`
  - `bike_sharing.csv`
  - `road_network.csv`
  - `parking_data.csv`
- **Kolom Umum** (bervariasi per file):
  - `zone_id`: Identifikasi unik untuk setiap zona.
  - `station_count`: Jumlah stasiun transportasi umum.
  - `bike_availability`: Ketersediaan sepeda sewa.
  - `road_density`: Kepadatan jaringan jalan.
  - `parking_capacity`: Kapasitas parkir.

### 5. Data Pelatihan (`mobility_train.csv`)
Berisi informasi jumlah perjalanan harian untuk pelatihan model.

- **Kolom**:
  - `zone_id`: Identifikasi unik untuk setiap zona.
  - `date`: Tanggal pengukuran.
  - `trips_thousands`: Jumlah perjalanan harian (dalam ribuan).

### 6. Data Pengujian (`mobility_test.csv`)
Digunakan untuk menghasilkan prediksi yang disubmit ke Kaggle. Tidak mencakup variabel target.

- **Kolom**:
  - `zone_id`: Identifikasi unik untuk setiap zona.
  - `date`: Tanggal pengukuran.

## Panduan untuk Peserta

- **Eksplorasi Dataset**: Peserta diharapkan untuk menganalisis dataset secara mendalam guna mengidentifikasi sumber data dan fitur yang relevan untuk prediksi.
- **Tujuan Kompetisi**: Merancang model prediktif untuk memprediksi `trips_thousands` pada data pengujian, dievaluasi menggunakan *Root Mean Squared Error* (RMSE) melalui Kaggle.
- **Format Submission**: File CSV dengan kolom `zone_id`, `date`, dan `trips_thousands`, diunggah ke Kaggle untuk penilaian otomatis.
- **Inovasi dan Kreativitas**: Peserta didorong untuk mengembangkan strategi pengolahan data dan pemodelan yang inovatif untuk menghasilkan solusi yang akurat dan relevan dalam konteks mobilitas urban cerdas.

Dokumen ini memberikan panduan strategis bagi peserta untuk memahami tantangan tahap penyisihan dan memanfaatkan dataset untuk menghasilkan solusi AI yang berdampak signifikan.
