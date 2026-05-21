# NON PROBABILITY SURVEI
# LATAR BELAKANG
Perkembangan teknologi digital pada era modern saat ini telah membawa perubahan besar dalam berbagai bidang kehidupan, termasuk di bidang pendidikan. Salah satu perkembangan teknologi yang semakin banyak digunakan adalah Artificial Intelligence (AI). Kehadiran AI memberikan berbagai kemudahan bagi mahasiswa dalam mendukung aktivitas belajar mengajar, seperti membantu mencari informasi, memahami materi perkuliahan, menyusun tugas, hingga meningkatkan efisiensi dalam proses pembelajaran. Berbagai platform berbasis AI kini semakin mudah diakses dan dimanfaatkan oleh mahasiswa dalam kegiatan akademik sehari-hari.
Penggunaan AI dalam dunia pendidikan memberikan dampak positif terhadap proses belajar mengajar. Mahasiswa dapat memperoleh informasi dengan lebih cepat, memahami materi yang sulit melalui penjelasan otomatis, serta meningkatkan efektivitas belajar secara mandiri. Selain itu, AI juga mendukung keberlangsungan pembelajaran baik secara online maupun offline, terutama di tengah perkembangan sistem pembelajaran digital yang semakin pesat. Dengan adanya teknologi AI, proses belajar menjadi lebih fleksibel dan mudah dijangkau oleh mahasiswa.
Namun, di balik berbagai manfaat tersebut, penggunaan AI juga menimbulkan beberapa permasalahan dalam kegiatan belajar mengajar mahasiswa. Kemudahan yang diberikan AI dapat menyebabkan mahasiswa menjadi terlalu bergantung pada teknologi dalam menyelesaikan tugas dan memahami materi perkuliahan. Penggunaan AI yang berlebihan dikhawatirkan dapat menurunkan kemampuan berpikir kritis, kreativitas, serta kemandirian mahasiswa dalam proses belajar. Selain itu, terdapat kemungkinan terjadinya penyalahgunaan AI dalam kegiatan akademik, seperti plagiarisme atau penggunaan jawaban instan tanpa memahami materi yang dipelajari.
Perbedaan cara dan intensitas penggunaan AI pada setiap mahasiswa juga dapat memengaruhi kualitas proses belajar mengajar. Sebagian mahasiswa memanfaatkan AI sebagai media pendukung pembelajaran, sementara sebagian lainnya cenderung menggunakan AI secara berlebihan tanpa diimbangi dengan kemampuan belajar mandiri. Kondisi ini menunjukkan bahwa penggunaan AI memiliki pengaruh terhadap keberlangsungan aktivitas belajar mengajar mahasiswa, baik dari sisi positif maupun negatif.
Berdasarkan permasalahan tersebut, diperlukan penelitian untuk mengetahui bagaimana pengaruh penggunaan Artificial Intelligence (AI) terhadap keberlangsungan aktivitas belajar mengajar mahasiswa. Penelitian ini diharapkan dapat memberikan gambaran mengenai dampak penggunaan AI dalam proses pembelajaran serta menjadi bahan pertimbangan dalam pemanfaatan teknologi AI secara bijak dan efektif di lingkungan pendidikan tinggi.
# TUJUAN
Berdasarkan rumusan masalah tersebut, maka tujuan penelitian ini adalah:
1.	Untuk mengetahui pengaruh penggunaan Artificial Intelligence (AI) terhadap aktivitas belajar mengajar mahasiswa. 
2.	Untuk mengetahui pengaruh penggunaan AI terhadap efektivitas proses belajar mahasiswa. 
3.	Untuk menganalisis dampak penggunaan AI terhadap pemahaman materi perkuliahan mahasiswa. 
4.	Untuk mengetahui pengaruh penggunaan AI terhadap kemandirian mahasiswa dalam belajar. 
5.	Untuk mengetahui pengaruh penggunaan AI terhadap kualitas hasil belajar mahasiswa.
# METODE
Penelitian ini menggunakan pendekatan kuantitatif dengan metode survei untuk memperoleh data melalui penyebaran kuesioner kepada responden. Populasi dalam penelitian ini adalah seluruh responden yang sesuai dengan karakteristik penelitian, dengan jumlah sampel sebanyak 33 responden yang diperoleh menggunakan teknik purposive sampling. Data yang digunakan berupa data primer yang diperoleh langsung dari hasil pengisian kuesioner dengan skala Likert 1 sampai 5, mulai dari sangat tidak setuju hingga sangat setuju. Instrumen penelitian terdiri dari 10 item pernyataan, yaitu P1 sampai P10. Pengolahan dan analisis data dilakukan menggunakan software R. Analisis data diawali dengan analisis deskriptif untuk melihat gambaran data responden, kemudian dilanjutkan dengan uji validitas menggunakan korelasi item-total untuk mengetahui kelayakan item pernyataan, serta uji reliabilitas menggunakan metode Cronbach Alpha untuk mengetahui tingkat konsistensi instrumen penelitian. Instrumen dinyatakan valid apabila nilai korelasi lebih besar dari r tabel dan dinyatakan reliabel apabila nilai Cronbach Alpha lebih besar dari 0,70.
# LANGKAH LANGKAH ANALISIS DATA
#IMPORT DATA KE RSTUDIO
Data kuesioner diinput ke dalam software R menggunakan package readxl dengan membaca file Excel yang telah disiapkan.
# IMPORT DATA
    data <- read_excel("C:/Users/ADVAN/OneDrive/Documents/data qusioner teksam.xlsx")
    View(data)
    names(data)

    View(data)
# UJI VALIDITAS
Tujuan dilakukannya uji validitas adalah untuk mengetahui apakah setiap item pernyataan dalam kuesioner mampu mengukur variabel penelitian secara tepat dan sesuai dengan tujuan penelitian. Uji validitas digunakan untuk memastikan bahwa butir-butir pertanyaan yang disusun benar-benar dapat mewakili konsep atau variabel yang diteliti, sehingga data yang diperoleh dapat dipercaya dan layak digunakan dalam proses analisis penelitian selanjutnya.
# UJI VALIDITAS
 # Ambil item kuesioner
    item <- data[, c("P1","P2","P3","P4","P5","P6","P7","P8","P9","P10")]
    corr.test(item)
    total <- rowSums(item)
    cor(item, total)

# UJI REABILITAS 
Uji reliabilitas dilakukan menggunakan metode Cronbach Alpha untuk mengetahui tingkat konsistensi instrumen penelitian. Instrumen dinyatakan reliabel apabila nilai Cronbach Alpha lebih besar dari 0,70.

# Uji reliabilitas Cronbach Alpha
    alpha(item)$total

# Menampilkan hasil cronbach Alphanya saja
    alpha(item)$total$raw_alpha
# UJI SLOVIN
Uji Slovin dilakukan untuk menentukan jumlah sampel penelitian berdasarkan jumlah populasi dan tingkat kesalahan tertentu agar sampel yang digunakan dapat mewakili populasi penelitian.
# Jumlah populasi
    N <- 33

# Tingkat kesalahan
    e <- 0.05

# Rumus Slovin
    n <- N / (1 + N * (e^2))

# Menampilkan hasil
    n

# Pembulatan
    round(n)

#pembulatan ke atas
    ceiling(n)
# HASIL DAN PEMBAHASAN
# UJI VALIDITAS
