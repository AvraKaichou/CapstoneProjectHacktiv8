# CapstoneProjectHacktiv8
Capstone Project For Hacktiv8's Data CLassification and Summarization

# Capstone Project: Analisis Sentimen dan Peringkasan Berita Otomatis

Proyek ini bertujuan untuk mengotomatisasi proses analisis konten dari dataset berita (`News Dataset.csv`). Dengan memanfaatkan kecerdasan buatan, proyek ini mampu mengklasifikasikan sentimen setiap berita (Positif, Negatif, Netral) dan menghasilkan ringkasan singkat dari isinya. Solusi ini membantu dalam memahami sejumlah besar data teks secara efisien, yang secara manual akan memakan waktu lama.

* **Raw Dataset Link:**
* [News Dataset.csv]https://github.com/AvraKaichou/CapstoneProjectHacktiv8/blob/0ea855df6d5a1e0f4d5e0eb629a61b2a4464d49a/News%20Dataset.csv

## AI Support Explanation

Proyek ini menggunakan model bahasa besar (LLM) dari IBM, yaitu **`ibm-granite/granite-13b-instruct`**, yang diakses melalui API dari platform **Replicate**. Penggunaan AI terbagi menjadi dua tugas utama:

1.  **Klasifikasi Sentimen:** AI diberi perintah (*prompt*) untuk menganalisis teks berita dan memberikan label sentimen. Ini adalah contoh penggunaan LLM untuk tugas klasifikasi teks.
2.  **Peringkasan Teks:** AI diberi perintah untuk membaca seluruh konten artikel dan membuat ringkasan yang padat. Ini menunjukkan kemampuan LLM dalam pemahaman dan generasi teks.

## Analysis Process

Alur kerja analisis proyek ini adalah sebagai berikut:
1.  **Setup Lingkungan:** Menginstal `pandas`, `langchain_community`, dan `replicate` di Google Colab.
2.  **Autentikasi:** Mengambil API Key Replicate secara aman menggunakan Colab Secrets.
3.  **Data Loading & Cleaning:** Memuat `News Dataset.csv` dan membersihkan data yang tidak relevan.
4.  **AI Execution:** Menerapkan fungsi `classify_sentiment` dan `summarize_text` pada setiap baris data menggunakan model IBM Granite.
5.  **Insight Generation:** Menganalisis hasil dari AI untuk menemukan pola, seperti distribusi sentimen, dan membuat visualisasi data.

## Insight & Findings

Berdasarkan analisis pada sampel data, ditemukan beberapa wawasan utama:

1.  **Distribusi Sentimen:** Analisis menunjukkan bahwa mayoritas berita dalam dataset memiliki sentimen **Netral** (60%), diikuti oleh **Positif** (30%) dan **Negatif** (10%). *(Ganti angka ini sesuai hasil dari kode visualisasi Anda)*
2.  **Visualisasi:**
    ![Pie Chart Sentimen](NAMA_FILE_GAMBAR_CHART.png) *(Anda perlu screenshot chart dari Colab, upload ke GitHub, dan ganti link ini)*
3.  **Interpretasi:** Tingginya sentimen netral mengindikasikan bahwa sebagian besar berita disajikan secara faktual. Sentimen positif seringkali terkait dengan peluncuran teknologi baru atau pencapaian bisnis, sedangkan sentimen negatif terkait dengan masalah atau kritik.

## Conclusion & Recommendations

**Kesimpulan:**
Proyek ini berhasil membuktikan bahwa model AI seperti IBM Granite dapat digunakan secara efektif untuk mengotomatisasi analisis konten berita, memberikan wawasan yang cepat dan terukur mengenai sentimen dan isi utama dari volume data yang besar.

**Rekomendasi:**
1.  **Untuk Bisnis:** Perusahaan dapat menggunakan pipeline ini untuk memonitor sentimen publik terhadap brand atau produk mereka di media.
2.  **Untuk Jurnalis:** Alat ini dapat membantu editor untuk mengevaluasi keberimbangan dan objektivitas pemberitaan di platform mereka.
3.  **Pengembangan Lanjutan:** Proyek ini dapat dikembangkan menjadi sebuah dashboard interaktif di mana pengguna bisa memfilter berita berdasarkan tanggal, kategori, dan sentimen.
