![purwadhika logo](https://static.wixstatic.com/media/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png/v1/fill/w_246,h_39,al_c,usm_0.66_1.00_0.01/2e6af2_f69a4271c3534ae1869a7ed63e278b2b~mv2.png)

Selamat datang di Ujian Modul 3, JCDS Bekasi.
Pada ujian kali ini, Anda akan mengerjakan soal untuk kasus:
- __Classification__: Hunting Basketball Player

Selamat mengerjakan!

### Case: Hunting Basketball Player (POIN: 100)
Anda adalah seorang manager tim basket di Indonesia yang berencana untuk merekrut beberapa pemain basket muda berbakat.

Data pilihan pemain nasional bisa Anda download di repository ini dengan nama file: (__ibl_player.csv__)[https://github.com/ridhoaryo/Ujian_MachineLearning_JCDS_Bekasi01/blob/master/ibl_player.csv]

Anda akan menggunakan dataset NBA PLayer sebagai dasar untuk membangun model machine learning untuk menentukan pemain-pemain muda Indonesia yang pantas Anda rekrut. Kolom `best_player` pada dataset NBA adalah acuan Anda. 0 berarti pemain tersebut tidak cocok untuk Anda rekrut. 1 berarti pemain tersebut layak untuk Anda rekrut.

__Requirements:__

Buatlah sebuah file __Jupyter Notebook (.ipynb)__, bernama "basketball_team_recruitment". Download & gunakan dataset NBA di repository ini dengan nama file: (__nba_all_season.csv__)[https://github.com/ridhoaryo/Ujian_MachineLearning_JCDS_Bekasi01/blob/master/nba_all_season.csv].
1. __(POIN: 5)__ Bersihkan data, lakukan _feature selection_ dan lakukan __standardisasi__.
2. __(POIN: 15)__ Buatlah minimal __5 (lima)__ macam data visualisasi yang dapat menampilkan insight dari para pemain NBA. __Contoh__:
    - Apakah terdapat hubungan antara pemain yang berpostur tinggi dengan rata-rata rebound per-game?
    - Apakah rata-rata poin menentukan seberapa sering pemain diikutkan dalam pertandingan (games played)?
    - Dan lain-lain.
    - Catatan: pairplot dihitung satu macam data visualisasi
    
    Ceritakan juga insight yang Anda temukan.
3. __(POIN: 10)__ Buatlah training dataset dan testing dataset dengan perbandingan training : tesing = 78% : 22% dan random_state = 101.
4. __(POIN: 15)__ Buatlah __3 (tiga) model__ machine learning untuk klasifikasi (pilihan  model bebas), lakukan __hyperparameter tuning__ untuk menentukan nilai parameter terbaik tiap model.
5. __(POIN: 25)__ Hitung __evaluation metrics__ tiap model. Metrics yang __wajib__ dihitung yakni: __accuracy__, __precision__, __recall__, __F1 score__ & __ROC AUC score__ (Khusus ROC AUC, sertakan plot kurvanya dan legend score AUC nya juga). Bandingkan _evaluation metrics_ dari setiap model dan pilih model yang memiliki hasil _evaluation metrics_ terbaik, untuk melakukan prediksi pada testing dataset. Tentukan juga, mana yang menjadi titik krusial Anda:
    
    - Mengurangi probabilitas model melakukan __False Negative__
    
    - Mengurangi probabilitas model melakukan __False Positive__

    Pilih salah satu dari pilihan di atas, dan jelaskan alasannya.

6. __(POIN: 15)__ Pada step ini kita akan mencoba menggunakan teknik oversampling (boleh menggunakan __Random Oversampling__ atau __SMOTE__). Latih model terbaik yang sudah Anda pilih sebelumnya, menggunakan data yang sudah di-oversampling. Lakukan prediksi menggunakan testing dataset, lalu bandingkan hasilnya _apple-to-apple_ dengan model yang sebelumnya dilatih menggunakan data yang tanpa dilakukan _oversampling_.
7. __(POIN: 10)__ Sekarang kita sudah mendapatkan model terbaik dari perbandingan score model tanpa oversampling (__step 5__) dengan model yang menggunakan teknik oversampling (__step 6__). Di step ini, kita akan coba mengatur threshold (_probability_). Mungkin dengan cara ini, kita akan mendapatkan score yang lebih baik. Buatlah sebuah dataframe untuk menunjukkan score dari setiap threshold. __Contoh__:

    Threshold | Precision | Recall |
    --|--|--|
    0.5 | 0.75 | 0.60
    0.75 | 0.85 | 0.40
    0.80 | 0.80 | 0.50

    Anda boleh menentukan sendiri berapa threshold yang ingin Anda coba. Positive atau Negative dari Precision dan Recall, ditentukan dari pilihan jawaban Anda di nomer 5.

    Apakah ada threshold yang menunjukkan score lebih baik dibanding dengan model sebelumnya? Jika ada maka gunakan threshold tersebut untuk step ke-8. Jika tidak, maka gunakan model sebelumnya untuk step ke-8.

8. __(POIN: 5)__ Gunakan model terbaik yang diperoleh, untuk mengklasifikasi pemain pada tabel pemain muda Indonesia (__ibl_player.csv__)di atas, manakah pemain yang patut direkrut atau tidak. Tampilkan hasilnya dalam sebuah __dataframe__.
