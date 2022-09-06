>**Chapter 1**  
>_Bab 1_

# **The Software Quality Challenge**
# _Tantangan Kualitas Perangkat Lunak_

| Chapter Outline | | |
| -----| --------------- | ------------  |
| 1.1 | The uniqueness of software quality assurance | 4 |
| 1.2 |  The environments for which SQA methods are developed | 7 |
|  | Summary | 11 |
|  | Review questions | 12 |
|  | Topics for discussion | 12 |

Two basic questions should be raised before we proceed to list the variety of
subjects and details of the book:

_Dua pertanyaan dasar harus diajukan sebelum kita melanjutkan untuk membuat daftar variasi dari
topik dan detail buku:_

>(1) Is it justified to devote a special book to software quality assurance (SQA)
or, in other words, can we not use the general quality assurance textbooks
available that are applicable to numerous areas and industries?

>(2) Having decided to develop specialized books for software quality assurance, at which of the various environments of software development, from
amateurs’ hobby to professionals’ work, should we aim our main efforts?
Put simply, what are the unique characteristics of the SQA environment?

>_(1) Apakah dibenarkan untuk mencurahkan buku khusus untuk jaminan kualitas perangkat lunak (SQA)
atau, dengan kata lain, tidak bisakah kita menggunakan buku teks penjaminan mutu umum?
tersedia yang berlaku untuk berbagai area dan industri?_

>_(2) Setelah memutuskan untuk mengembangkan buku khusus untuk jaminan kualitas perangkat lunak, di mana dari berbagai lingkungan pengembangan perangkat lunak, dari:
hobi amatir ke pekerjaan profesional, haruskah kita mengarahkan upaya utama kita?
Sederhananya, apa karakteristik unik dari lingkungan SQA?_

The objective of this chapter is to answer these questions by exploring the
related issues.

_Tujuan dari bab ini adalah untuk menjawab pertanyaan-pertanyaan ini dengan mengeksplorasi
masalah terkait._

After completing this chapter, you will be able to:

_Setelah menyelesaikan bab ini, Anda akan dapat:_

>■ Identify the unique characteristics of software as a product and as production process that justify separate treatment of its quality issues.

>■**Identifikasi karakteristik unik perangkat lunak sebagai produk dan sebagai proses produksi yang membenarkan perlakuan terpisah terhadap masalah kualitasnya.**

>■ Recognize the characteristics of the environment where professional software development and maintenance take place.

>■**Mengenali karakteristik lingkungan tempat pengembangan dan pemeliharaan perangkat lunak profesional berlangsung.**

>■ Explain the main environmental difficulties faced by software development and maintenance teams as a result of the environment in which
they operate.

>■**Jelaskan kesulitan lingkungan utama yang dihadapi oleh tim pengembangan dan pemeliharaan perangkat lunak sebagai akibat dari lingkungan di mana mereka beroperasi.**

# **1.1 The uniqueness of software quality assurance**

_1.1	Keunikan Jaminan Kualitas Perangkat Lunak_

“Lihat ini,” teriak temanku sambil menyodorkan Fitur Dagal kepadaku Pamflet Garansi Terbatas. “Bahkan Fitur Dagal tidak dapat mengatasi perangkat lunak bug." Dia menunjuk ke paragraf pendek di halaman 3 dari selebaran yang menyatakan ketentuan garansi untuk AMGAL, produk Master Perangkat Lunak terkemuka dijual di seluruh dunia. Selebaran tersebut menyatakan sebagai berikut:

>GARANSI TERBATAS

    Fitur Dagal tidak memberikan jaminan, baik tersurat maupun tersirat, dengan sehubungan dengan kinerja, keandalan, atau kesesuaian AMGAL untuk semua yang ditentukan tujuan. Fitur Dagal tidak menjamin bahwa perangkat lunak atau dokumentasinya akan memenuhi kebutuhan Anda. meskipun Fitur Dagal memiliki melakukan pengujian perangkat lunak secara menyeluruh dan meninjau dokumentasi, Fitur Dagal tidak memberikan jaminan apa pun bahwa perangkat lunak dan dokumentasinya bebas dari kesalahan. Fitur Dagal tidak akan menjadi bertanggung jawab atas segala kerusakan, insidental, langsung, tidak langsung atau konsekuensial, timbul sebagai akibat dari data yang rusak, biaya pemulihan, kerugian laba, dan ketiga klaim pihak. perangkat lunak dilisensikan "sebagaimana adanya". pembeli mengasumsikan risiko lengkap yang berasal dari penerapan program AMGAL, kualitas dan kinerja.

    Jika cacat fisik ditemukan dalam dokumentasi atau CD di yang AMGAL didistribusikan, Fitur Dagal akan menggantikan, tanpa biaya, dokumentasi atau CD dalam waktu 180 hari setelah pembelian, asalkan bukti pembelian disajikan.

“Apakah perangkat lunak AMGAL benar-benar istimewa sehingga pengembangnya tidak mampu memenuhi tantangan untuk memastikan produk bebas bug?” lanjut saya teman. “Apakah paket perangkat lunak lain membatasi jaminan mereka dengan cara yang sama?”

Meskipun Fitur Dagal dan AMGAL adalah fiktif, pemeriksaan terhadap jaminan yang ditawarkan oleh pengembang perangkat lunak lain mengungkapkan pola yang sama. Tidak ada pengembang yang akan menyatakan bahwa perangkat lunaknya bebas dari cacat, seperti yang biasa dilakukan ole produsen besar perangkat keras komputer. Penolakan ini sebenarnya mencerminkan perbedaan unsur penting antara perangkat lunak dan industri lainnya produk, seperti mobil, mesin cuci atau radio. Perbedaan tersebut dapat dikategorikan sebagai berikut:

    (1)	Kompleksitas produk. Kompleksitas produk dapat diukur dengan jumlah mode operasional yang diizinkan produk. Sebuah produk industri, bahkan mesin canggih, tidak memungkinkan lebih dari beberapa ribu mode operasi, yang dibuat oleh kombinasi yang berbeda pengaturan mesin. Melihat paket perangkat lunak khas yang dapat ditemukan jutaan kemungkinan operasi perangkat lunak. Memastikan bahwa orang banyak kemungkinan operasional didefinisikan dengan benar dan dikembangkan adalah tantangan bagi industri perangkat lunak.	

    (2)	Visibilitas produk. produk industri terlihat, perangkat lunak produk tidak terlihat. Sebagian besar cacat pada produk industri dapat terdeteksi selama proses produksi. Apalagi tidak adanya bagian dalam produk industri, sebagai suatu peraturan, sangat terlihat (bayangkan sebuah pintu hilang dari mobil baru Anda). Namun, cacat pada produk perangkat lunak (apakah disimpan di disket atau CD) tidak terlihat, seperti fakta bahwa bagian-bagiannya paket perangkat lunak mungkin tidak ada sejak awal.

    (3)	Pengembangan produk dan proses produksi. Mari kita tinjau sekarang fase di mana kemungkinan mendeteksi cacat pada produk industri mungkin muncul:

    (a)	Pengembangan produk. Pada fase ini para desainer dan staf penjaminan mutu (QA) memeriksa dan menguji prototipe produk, untuk mendeteksi cacatnya.

    (b)	Perencanaan produksi produk. Selama fase ini produksi proses dan alat dirancang dan disiapkan. Di beberapa produk ada adalah kebutuhan akan jalur produksi khusus untuk dirancang dan dibangun. Fase ini memberikan peluang tambahan untuk memeriksa produk, yang dapat mengungkapkan cacat yang "lolos" dari tinjauan dan pengujian yang dilakukan selama fase pengembangan.

    (c)	Manufaktur. Pada fase ini, prosedur QA diterapkan untuk mendeteksi kegagalan produk itu sendiri. Cacat pada produk terdeteksi diperiode pertama manufaktur biasanya dapat dikoreksi dengan perubahan desain produk atau bahan atau alat produksi, dengan cara yang menghilangkan cacat tersebut pada produk yang diproduksi di masa depan.

Dibandingkan dengan produk industri, produk perangkat lunak tidak menguntungkan dari peluang untuk mendeteksi cacat pada ketiga fase proses produksi. Satu-satunya fase ketika cacat dapat dideteksi adalah fase pengembangan. Mari kita tinjau apa kontribusi setiap fase terhadap deteksi cacat:

    (a)	Pengembangan produk. Selama fase ini, upaya pengembangan tim dan profesional jaminan kualitas perangkat lunak diarahkan untuk mendeteksi cacat produk yang melekat. Di akhir fase ini prototipe yang disetujui, siap untuk direproduksi, tersedia.
    (b)	Perencanaan produksi produk. Fase ini tidak diperlukan untuk proses produksi perangkat lunak, karena pembuatan salinan perangkat lunak dan pencetakan manual perangkat lunak dilakukan secara otomatis. Ini berlaku untuk produk perangkat lunak apa pun, baik jumlah salinannya kecil, seperti dalam perangkat lunak yang dibuat khusus, atau besar, seperti dalam paket perangkat lunak dijual kepada masyarakat umum.
    (c)	Manufaktur. Seperti disebutkan sebelumnya, pembuatan perangkat lunak terbatas untuk menyalin produk dan mencetak salinan dari manual perangkat lunak. Akibatnya, harapan untuk mendeteksi cacat sangat terbatas selama fase ini.

The differences affecting the detection of defects in software products versus
other industrial products are shown in Table 1.1 and Frame 1.1.

_Perbedaan yang mempengaruhi deteksi cacat pada produk perangkat lunak versus
produk industri lainnya ditunjukkan pada Tabel 1.1 dan Frame 1.1._

It should be noted that significant parts of advanced machinery as well
as of household machines and other products include embedded software
components (usually termed “firmware”) that are integrated into the product. These software components (the firmware) share the same
characteristics of the software products mentioned above. It follows that the
comparison shown above should actually be that of software products versus other industrial products and non-software components of industrial
products that include firmware. Hereinafter, when mentioning software, we
will mean software products as well as firmware.

_Perlu dicatat bahwa bagian penting dari mesin canggih juga
pada mesin rumah tangga dan produk lainnya termasuk perangkat lunak tertanam
komponen (biasanya disebut "firmware") yang terintegrasi ke dalam produk. Komponen perangkat lunak ini (firmware) berbagi hal yang sama
karakteristik produk perangkat lunak yang disebutkan di atas. Oleh karena itu,
perbandingan yang ditunjukkan di atas sebenarnya adalah produk perangkat lunak versus produk industri lainnya dan komponen non-perangkat lunak industri
produk yang menyertakan firmware. Selanjutnya, ketika menyebutkan perangkat lunak, kami
akan berarti produk perangkat lunak serta firmware._

The fundamental differences between the development and production
processes related to software products and those of other industrial products
warrant the creation of a different SQA methodology for software. The need
for special tools and methods for the software industry is reflected in the professional publications as well in special standards devoted to SQA, such as
ISO 9000-3, “Guidelines for the application of ISO 9001 to the development, supply and maintenance of software”. This point is supported by the fact
that targeted guidelines have not been prepared by ISO for other industries,

_Perbedaan mendasar antara pengembangan dan produksi
proses yang terkait dengan produk perangkat lunak dan produk industri lainnya
menjamin pembuatan metodologi SQA yang berbeda untuk perangkat lunak. Kebutuhan
untuk alat dan metode khusus untuk industri perangkat lunak tercermin dalam publikasi profesional serta dalam standar khusus yang ditujukan untuk SQA, seperti
ISO 9000-3, “Pedoman penerapan ISO 9001 untuk pengembangan, penyediaan dan pemeliharaan perangkat lunak”. Poin ini didukung oleh fakta
bahwa pedoman yang ditargetkan belum disiapkan oleh ISO untuk industri lain,_

| Characteristic | Software Products | Other industrial products|
| -----| --------------- | ------------  |
| Complexity | Usually, very complex product allowing for very large number of operational options | Degree of complexity much lower, allowing at most a few thousand operational options |
| Visibility of product |  Invisible product, impossible to detect defects or omissons by sight (e.g. of a diskette or CD storing the software) | Visible product, allowing effective detection of defects by sight |
| Nature of development and produciton process  | Opportunities to detect defects arise in only one phase, namely product development | Opportunities to detect defects arise all phases of development and production ■ Product development ■ Product production planning■ Manufacturing|