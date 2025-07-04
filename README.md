# Analisis Sentimen dan Topik Publik Inflasi di Indonesia melalui Twitter

Repositori ini berisi proyek analisis teks yang bertujuan untuk memahami percakapan publik terkait **isu inflasi** di Indonesia berdasarkan tweet berbahasa Indonesia dari **Januari 2024 hingga Januari 2025**. Proyek ini mencakup proses crawling data, preprocessing teks, analisis kata penting (TF-IDF), dan pemodelan topik (*Latent Dirichlet Allocation/LDA*) untuk menemukan insight dari 2.000 tweet.

## Tujuan Proyek
1. Mengumpulkan tweet terkait kata kunci *inflasi* dari Twitter.
2. Melakukan preprocessing teks secara menyeluruh (case folding, tokenisasi, stopwords removal, stemming).
3. Mengidentifikasi kata-kata penting dengan TF-IDF.
4. Menemukan topik pembicaraan utama dengan LDA.
5. Menyajikan hasil dalam bentuk visualisasi seperti bar chart, word cloud, PCA, dan pyLDAvis.
   
## Tools dan Library
Python
`pandas`, `matplotlib`, `nltk`, `Sastrawi`, `gensim`, `scikit-learn`
`tweet-harvest` (Node.js) untuk pengambilan data dari Twitter
`pyLDAvis` untuk visualisasi topik

## Alur Pengerjaan

### 1. Crawling Tweet

Menggunakan `tweet-harvest` untuk mengambil hingga 2000 tweet dengan kata kunci:
inflasi since:2024-01-11 until:2025-01-11 lang:id

### 2. Preprocessing Teks

Langkah preprocessing:

* Case folding (huruf kecil)
* Menghapus tanda baca
* Tokenisasi
* Stopwords removal
* Stemming (Sastrawi)

### 3. Analisis

* **TF-IDF**: Menentukan kata penting berdasarkan frekuensi relatif.
* **LDA (Latent Dirichlet Allocation)**: Mengelompokkan topik utama percakapan.

### 4. Visualisasi

* Word Cloud
* Bar Chart Top Words
* PCA Projection
* pyLDAvis Interactive Visualization

## Hasil Utama

* Ditemukan beberapa **topik dominan** yang sering muncul dalam percakapan terkait inflasi.
* TF-IDF mengungkap kata penting seperti: *harga, naik, kebutuhan, pemerintah*.
* Visualisasi membantu memetakan fokus percakapan pengguna Twitter terhadap fenomena ekonomi ini.

## Evaluasi Model

* Skor koherensi LDA digunakan untuk mengukur kualitas topik.
* Eksperimen jumlah topik dilakukan untuk mencari nilai koherensi terbaik.

## Insight

Hasil analisis dapat digunakan untuk:

* Memahami sentimen publik terhadap kebijakan ekonomi.
* Mengidentifikasi isu utama yang menjadi perhatian masyarakat.
* Memberikan rekomendasi bagi pengambil kebijakan dan analis sosial.
