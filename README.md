# Smoking Health Risk Analysis Dashboard (Indonesia)

Dashboard interaktif Power BI yang menganalisis risiko kesehatan akibat merokok, dikaitkan dengan demografi dan kondisi organ, menggunakan data sintetik yang dimodelkan mengikuti pola statistik
merokok di Indonesia.

## Fitur
- 4 halaman: Overview, Smoking Patterns, Health Risks, Organ Health
- Slicer interaktif ikon organ + toggle kondisi (Healthy/Damaged)
- Visualisasi dinamis gambar organ sesuai pilihan
- DAX measures untuk analisis risiko kesehatan

## Insight Utama
1. Gap gender yang tajam (paling "menjual")

Pria 65% pernah merokok (46.8% aktif + 18.1% mantan), wanita cuma 5.2% ini insight paling kuat karena bukan cuma pola dari data kita, tapi memang mencerminkan kondisi riil Indonesia (data GATS/BPS). Bagus buat pembuka narasi dashboard.

2. Korelasi jelas antara status merokok dan kerusakan organ

Perokok aktif: 43% organ rusak, mantan perokok: 23%, tidak pernah merokok: 12%. Ini insight utama secara analitis nunjukin gradien yang jelas (bukan cuma "ada" vs "nggak ada", tapi makin berkurang seiring berhenti merokok), yang secara medis masuk akal dan bisa jadi talking point kuat kalau ditanya soal validitas data.

3. Paru-paru paling rentan

Karena kita set multiplier kerentanan organ waktu generate data (Lungs = 1.5x lebih rentan dibanding baseline), organ Lungs kemungkinan besar bakal nunjukin persentase kerusakan tertinggi di antara 5 organ cek chart "% Organ Rusak per Organ" yang kita buat di halaman Organ Health buat konfirmasi angka pastinya, terus highlight itu.

4. Kolesterol naik seiring status merokok

Rata-rata kolesterol: perokok aktif 200 mg/dL, mantan 186, tidak pernah 171. Bagus buat pelengkap insight #2, nunjukin dampak bukan cuma di organ tapi juga metabolisme.

## Dataset
Data sintetik (`data/health_dataset_indonesia.csv`), dibuat
mengikuti pola prevalensi merokok Indonesia (BPS/GATS): ## Dataset

Dataset ini merupakan *data sintetik* (bukan data pasien nyata),
dibuat menggunakan Python untuk keperluan pembelajaran dan simulasi
analisis. Distribusi dan korelasi antar variabel dirancang mengikuti
pola statistik merokok di Indonesia yang dipublikasikan oleh
BPS dan survei GATS (Global Adult Tobacco Survey), dengan asumsi:

- **Prevalensi merokok**: pria ~65% (pernah merokok), wanita ~5%,
  sesuai kesenjangan gender yang tercatat secara nasional
- **Konsumsi rata-rata**: ~12-13 batang/hari untuk perokok aktif
- **Konsumsi alkohol**: mayoritas rendah, mencerminkan pola konsumsi
  populasi mayoritas muslim di Indonesia
- **Kerusakan organ**: probabilitas kerusakan organ dimodelkan
  meningkat seiring lama & intensitas merokok, dengan paru-paru
  diberi bobot kerentanan lebih tinggi dibanding organ lain

Karena bersifat sintetik, dataset ini **tidak merepresentasikan
data medis aktual** dan tidak boleh digunakan untuk kesimpulan
klinis tujuannya murni demonstrasi kemampuan analisis data dan
visualisasi.

## Tools
Power BI Desktop, DAX, Power Query, Data Modeling

## Cara Membuka
1. Clone/download repo ini
2. Buka `smoking_health_dashboard.pbix` dengan Power BI Desktop

## Screenshot
(image.png)

## Author
Email: zhafryfarhan@gmail.com
Linkedin: @Zhafry Dimas Farhan
Instagram @zhafryfarhann
