# Capstone-Project-3-E-Commerce-Customer-Churn-Data

**Context**  
Pada era modern ini, retensi pelanggan merupakan faktor penting dalam kelangsungan bisnis untuk bersaing dengan kompetitor.Karena profitabilitas perusahaan dipengaruhi oleh banyak hal, tetapi tidak ada yang lebih penting daripada retensi pelanggan. Kemampuan untuk mengembangkan dan mempertahankan basis pelanggan yang setia adalah tujuan utama bagi setiap perusahaan, dan metode pembelajaran yang membantu Anda mengurangi dan mencegah pelanggan churn bisa sangat berharga.

Target :

0 : Tidak berhenti berlangganan

1 : Berhenti berlangganan (churn)

**Problem Statement :**

Perusahaan menganggap pelanggan churn sebagai suatu hal yang sangat penting sehingga perusahaan ingin mengetahui pelanggan yang akan berpindah ke lain hati, sehingga mereka dapat melakukan pendekatan kepada pelanggan untuk menawarkan promo.
Sebelum melakukan penawaran promo, perusahaan perlu mengatur strategi supaya promo yang dilakukan tepat sasaran. Promo yang dilakukan tentu tidak diberikan kepada seluruh pelanggan, melainkan yang diprioritaskan adalah pelanggan yang diprediksi akan churn. Hal ini dilakukan untuk melakukan efisiensi terhadap jumlah promo yang dikeluarkan.
Jika perusahaan salah dalam memberikan promo atau asal memberikan promo terhadap pelanggan yang notabene tidak diprediksi churn, tentunya berakibat pada **operation loss** karena `mengeluarkan biaya untuk promo yang sebenernya tidak diperlukan`.


**Goals :**

Maka berdasarkan permasalahan-permasalahan di atas, perusahaan ingin memiliki kemampuan untuk memprediksi kemungkinan seorang pelanggan akan berhenti menggunakan berlanggan atau tidak, sehingga dapat memfokuskan upaya-upaya retensi pada pelanggan yang terindikasi untuk churn.

Dan juga, perusahaan ingin mengetahui faktor-faktor apa saja yang cenderung mempengaruhi pelanggan bertahan, sehingga mereka dapat membuat program-program yang lebih tepat sasaran dalam mengurangi jumlah pelanggan yang churn.

**Analytic Approach :**

Jadi yang akan kita lakukan adalah menganalisis data untuk menemukan pola yang membedakan pelanggan yang akan berhenti menggunakan berlangganan (churn) atau tidak.

Kemudian kita akan membangun model klasifikasi yang akan membantu perusahaan untuk dapat memprediksi probabilitas seorang pelanggan akan berhenti menggunakan berlangganan (churn) atau tidak.

**Metric Evaluation :**

Karena fokus utama kita adalah pelanggan yang akan berhenti menggunakan layanan, maka target yang kita tetapkan adalah sebagai berikut:

Target :
- 0 : Tidak berhenti berlangganan
- 1 : Berhenti berlangganan (churn)

**Type 1 error** : **False Positive**  (pelanggan yang aktualnya tidak churn tetapi diprediksi churn)\
Konsekuensi: operation loss karena mengeluarkan biaya promo untuk pelanggan yang tidak tepat.
Biaya yang dikeluarkan sebesar 50 USD per pelanggan bulan ([sumber](https://sci-hub.se/https://doi.org/10.1016/j.jretconser.2017.10.007)).

**Type 2 error** : **False Negative**  (pelanggan yang aktualnya churn tetapi diprediksi tidak akan churn)\
Konsekuensi: profit loss karena pelanggan churn. Biaya yang dikeluarkan 5x lipat dari biaya promo ke pelanggan     yaitu 250 USD per pelanggan per bulan ([sumber](https://www.superoffice.com/blog/reduce-customer-churn/)).

Berdasarkan konsekuensinya, maka sebisa mungkin yang akan kita lakukan adalah membuat model yang dapat mengurangi pelanggan churn dari perusahaan tersebut, khususnya jumlah False Negative  pelanggan yang aktualnya churn tetapi diprediksi tidak akan churn), tetapi juga dapat meminimalisir pemberian promo yang tidak tepat. Jadi nanti metric utama yang akan kita gunakan adalah **f2_score**, karena recall kita anggap dua kali lebih penting daripada precision.

**Conclusion**
- Model yang dipilih adalah Random Forest karena danya peningkatan yang stabil pada saat uji coba dan dapat memprediksi pelanggan yang akan Churn
- Dapat meminimalisasi kerugian perusahaan cukup baik sebesar 41.9%
- Memperhatikan variable-variable importnaces karena itu sangat berpengaruh pada pelanggan akan churn atau tidak.


