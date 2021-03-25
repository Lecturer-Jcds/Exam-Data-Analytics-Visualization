# Soal Ujian Data Analytics & Visualization

[![logopwdk.png](https://i.postimg.cc/66VC3Rgx/logopwdk.png)](https://postimg.cc/s1XMHB3T)


<hr>


#

### **Soal 1 - MySQL World Database - 30 Points**

MySQL secara default menyertakan database ```world``` yang dapat digunakan oleh user untuk mempelajari teknik penggunaan database di MySQL. Database ```world``` merupakan sample real database dan dirilis sekitar awal tahun 2000-an. Database ini berisi 3 buah tabel yang saling berhubungan satu sama lain:

- Tabel ```city``` berisi informasi tentang __4079__ kota di dunia.
- Tabel ```country``` berisi informasi tentang __239__ negara/wilayah yang dianggap negara di dunia.
- Tabel ```countrylanguage``` berisi informasi tentang bahasa yang digunakan oleh negara-negara di dunia.

*__Soal :__* Aktifkan server MySQL Anda, lalu gunakan database ```world``` dan tuliskan langkah-langkah/query MySQL untuk menyelesaikan perintah berikut:

1. Tampilkan daftar __10 kota terpadat di Indonesia__. Urutkan data dari kota dengan populasi terbanyak. Kolom yang diwajibkan tampil adalah __id kota__, __nama kota__, __kode negara__, __distrik/provinsi__ dan __populasi__. Output yang diharapkan:

    ```bash
    +-----+----------------+-------------+------------------+------------+
    | ID  | Name           | CountryCode | District         | Population |
    +-----+----------------+-------------+------------------+------------+
    | 939 | Jakarta        | IDN         | Jakarta Raya     |    9604900 |
    | 940 | Surabaya       | IDN         | East Java        |    2663820 |
    | 941 | Bandung        | IDN         | West Java        |    2429000 |
    | 942 | Medan          | IDN         | Sumatera Utara   |    1843919 |
    | 943 | Palembang      | IDN         | Sumatera Selatan |    1222764 |
    | 944 | Tangerang      | IDN         | West Java        |    1198300 |
    | 945 | Semarang       | IDN         | Central Java     |    1104405 |
    | 946 | Ujung Pandang  | IDN         | Sulawesi Selatan |    1060257 |
    | 947 | Malang         | IDN         | East Java        |     716862 |
    | 948 | Bandar Lampung | IDN         | Lampung          |     680332 |
    +-----+----------------+-------------+------------------+------------+
    ```

2. Tampilkan daftar __10 kota terpadat di dunia beserta asal negaranya__. Urutkan data dari kota dengan populasi terbanyak. Kolom yang diwajibkan ada minimal adalah __id kota__, __nama kota__, __distrik/provinsi__, __nama negara__ dan __populasi__. Output yang diharapkan:

    ```bash
    +------+-------------------+------------------+--------------------+------------+
    | id   | nama_kota         | district         | negara             | population |
    +------+-------------------+------------------+--------------------+------------+
    | 1024 | Mumbai (Bombay)   | Maharashtra      | India              |   10500000 |
    | 2331 | Seoul             | Seoul            | South Korea        |    9981619 |
    |  206 | SÃ£o Paulo        | SÃ£o Paulo       | Brazil             |    9968485 |
    | 1890 | Shanghai          | Shanghai         | China              |    9696300 |
    |  939 | Jakarta           | Jakarta Raya     | Indonesia          |    9604900 |
    | 2822 | Karachi           | Sindh            | Pakistan           |    9269265 |
    | 3357 | Istanbul          | Istanbul         | Turkey             |    8787958 |
    | 2515 | Ciudad de MÃ©xico | Distrito Federal | Mexico             |    8591309 |
    | 3580 | Moscow            | Moscow (City)    | Russian Federation |    8389200 |
    | 3793 | New York          | New York         | United States      |    8008278 |
    +------+-------------------+------------------+--------------------+------------+
    ```

3. Tampilkan daftar __10 negara yang tercatat merdeka paling awal__. Daftar negara yang tidak diketahui tahun kemerdekaannya, tidak perlu diikutsertakan. Kolom yang diwajibkan ada minimal adalah __kode negara__, __nama negara__, __benua__, __regional__ dan __tahun merdeka (*Independence Year*)__. Output yang diharapkan:

    ```bash
    +------+----------------+-----------+------------------+---------------+
    | code | name           | continent | region           | tahun_merdeka |
    +------+----------------+-----------+------------------+---------------+
    | CHN  | China          | Asia      | Eastern Asia     |         -1523 |
    | ETH  | Ethiopia       | Africa    | Eastern Africa   |         -1000 |
    | JPN  | Japan          | Asia      | Eastern Asia     |          -660 |
    | DNK  | Denmark        | Europe    | Nordic Countries |           800 |
    | SWE  | Sweden         | Europe    | Nordic Countries |           836 |
    | FRA  | France         | Europe    | Western Europe   |           843 |
    | SMR  | San Marino     | Europe    | Southern Europe  |           885 |
    | GBR  | United Kingdom | Europe    | British Islands  |          1066 |
    | PRT  | Portugal       | Europe    | Southern Europe  |          1143 |
    | AND  | Andorra        | Europe    | Southern Europe  |          1278 |
    +------+----------------+-----------+------------------+---------------+
    ```

4. Tampilkan daftar __benua yang memiliki lebih dari 10 negara di dalamnya__. Kolom yang ditampilkan minimal: __nama benua__, __jumlah negara di dalam benua__, __total populasi__ dan __rata-rata angka harapan hidup (*Life Expectancy*)__ kemudian urutkan dari benua yang memiliki populasi terbanyak. Output yang diharapkan:

    ```bash
    +---------------+---------------+------------+-------------------+
    | Benua         | Jumlah_Negara | Populasi   | Rata_AngkaHrpnHdp |
    +---------------+---------------+------------+-------------------+
    | Asia          |            51 | 3705025700 |          67.44118 |
    | Africa        |            58 |  784475000 |          52.57193 |
    | Europe        |            46 |  730074600 |          75.14773 |
    | North America |            37 |  482993000 |          72.99189 |
    | South America |            14 |  345780000 |          70.94615 |
    | Oceania       |            28 |   30401150 |          69.71500 |
    +---------------+---------------+------------+-------------------+
    ```

5. Tampilkan daftar __negara-negara Asia yang memiliki angka harapan hidup lebih dari rata-rata angka harapan hidup negara-negara Eropa__. Kolom yang diwajibkan ada yaitu __nama negara__, __nama benua__, __angka harapan hidup__ dan **Pendapatan Nasional Bruto/GNP (_Gross National Product_)**. Urutkan data dari negara Asia dengan angka harapan hidup tertinggi. Output yang diharapkan:

    ```bash
    +-----------+-------+-------------------+------------+
    | Nama      | Benua | AngkaHarapanHidup | GNP        |
    +-----------+-------+-------------------+------------+
    | Macao     | Asia  |              81.6 |    5749.00 |
    | Japan     | Asia  |              80.7 | 3787042.00 |
    | Singapore | Asia  |              80.1 |   86503.00 |
    | Hong Kong | Asia  |              79.5 |  166448.00 |
    | Israel    | Asia  |              78.6 |   97477.00 |
    | Jordan    | Asia  |              77.4 |    7526.00 |
    | Cyprus    | Asia  |              76.7 |    9333.00 |
    | Taiwan    | Asia  |              76.4 |  256254.00 |
    | Kuwait    | Asia  |              76.1 |   27037.00 |
    +-----------+-------+-------------------+------------+
    ```

6. Tampilkan daftar __10 negara yang bahasa resminya (_official language_) adalah bahasa Inggris, dan memiliki persentase pengguna bahasa Inggris tertinggi di dunia__. Kolom yang diwajibkan ada yaitu __kode negara__, __nama negara__, __bahasa__, __kolom isOfficial__ dan __percentage__. Urutkan dari persentase pengguna bahasa Inggris tertinggi. Output yang diharapkan:

    ```bash
    +-------------+----------------------+----------+------------+------------+
    | countrycode | name                 | language | isOfficial | percentage |
    +-------------+----------------------+----------+------------+------------+
    | BMU         | Bermuda              | English  | T          |      100.0 |
    | IRL         | Ireland              | English  | T          |       98.4 |
    | GBR         | United Kingdom       | English  | T          |       97.3 |
    | GIB         | Gibraltar            | English  | T          |       88.9 |
    | NZL         | New Zealand          | English  | T          |       87.0 |
    | USA         | United States        | English  | T          |       86.2 |
    | VIR         | Virgin Islands, U.S. | English  | T          |       81.7 |
    | AUS         | Australia            | English  | T          |       81.2 |
    | CAN         | Canada               | English  | T          |       60.4 |
    | BLZ         | Belize               | English  | T          |       50.8 |
    +-------------+----------------------+----------+------------+------------+
    ```

7. Tampilkan daftar __negara ASEAN beserta populasi negaranya, Pendapatan Nasional Bruto/GNP (_Gross National Product_), ibukota & populasi ibukota__. ASEAN (_Association of Southeast Asian Nations_) merupakan sebuah organisasi geo-politik dan ekonomi dari negara-negara di kawasan Asia Tenggara, yang didirikan di Bangkok, 8 Agustus 1967 dengan tujuan untuk meningkatkan pertumbuhan ekonomi, kemajuan sosial, pengembangan kebudayaan negara-negara anggotanya, serta memajukan perdamaian dan stabilitas di tingkat regional. Negara Asia Tenggara yang terdaftar sebagai anggota ASEAN adalah: 

    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/9c/Flag_of_Brunei.svg/33px-Flag_of_Brunei.svg.png' alt='lintang' style='height:13px; width:18px'/> Brunei
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Flag_of_Cambodia.svg/33px-Flag_of_Cambodia.svg.png' alt='lintang' style='height:13px; width:18px'/> Cambodia
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/2/26/Flag_of_East_Timor.svg/33px-Flag_of_East_Timor.svg.png' alt='lintang' style='height:13px; width:18px'/> East Timor
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/9f/Flag_of_Indonesia.svg/33px-Flag_of_Indonesia.svg.png' alt='lintang' style='height:13px; width:18px'/> Indonesia
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/5/56/Flag_of_Laos.svg/33px-Flag_of_Laos.svg.png' alt='lintang' style='height:13px; width:18px'/> Laos
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/6/66/Flag_of_Malaysia.svg/33px-Flag_of_Malaysia.svg.png' alt='lintang' style='height:13px; width:18px'/> Malaysia
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/8/8c/Flag_of_Myanmar.svg/33px-Flag_of_Myanmar.svg.png' alt='lintang' style='height:13px; width:18px'/> Myanmar
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Flag_of_the_Philippines.svg/33px-Flag_of_the_Philippines.svg.png' alt='lintang' style='height:13px; width:18px'/> Philippines
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Flag_of_Singapore.svg/33px-Flag_of_Singapore.svg.png' alt='lintang' style='height:13px; width:18px'/> Singapore 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/a/a9/Flag_of_Thailand.svg/33px-Flag_of_Thailand.svg.png' alt='lintang' style='height:13px; width:18px'/> Thailand
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/2/21/Flag_of_Vietnam.svg/33px-Flag_of_Vietnam.svg.png' alt='lintang' style='height:13px; width:18px'/> Vietnam
    
    Tampilkan daftar __negara ASEAN beserta populasi negaranya, Pendapatan Nasional Bruto/GNP (_Gross National Product_), ibukota & populasi ibukota__, dengan kolom yang diwajibkan ada yaitu __nama negara__, __populasi negara__, __pendapatan nasional bruto (GNP)__, __nama ibukota__ dan __populasi ibukota__. Urutkan berdasarkan abjad nama negara. Output yang diharapkan:

    ```bash
    +--------------+-----------------+-----------+---------------------+------------------+
    | Negara_ASEAN | Populasi_Negara | GNP       | Ibukota             | Populasi_Ibukota |
    +--------------+-----------------+-----------+---------------------+------------------+
    | Brunei       |          328000 |  11705.00 | Bandar Seri Begawan |            21484 |
    | Cambodia     |        11168000 |   5121.00 | Phnom Penh          |           570155 |
    | East Timor   |          885000 |      0.00 | Dili                |            47900 |
    | Indonesia    |       212107000 |  84982.00 | Jakarta             |          9604900 |
    | Laos         |         5433000 |   1292.00 | Vientiane           |           531800 |
    | Malaysia     |        22244000 |  69213.00 | Kuala Lumpur        |          1297526 |
    | Myanmar      |        45611000 | 180375.00 | Rangoon (Yangon)    |          3361700 |
    | Philippines  |        75967000 |  65107.00 | Manila              |          1581082 |
    | Singapore    |         3567000 |  86503.00 | Singapore           |          4017733 |
    | Thailand     |        61399000 | 116416.00 | Bangkok             |          6320174 |
    | Vietnam      |        79832000 |  21929.00 | Hanoi               |          1410000 |
    +--------------+-----------------+-----------+---------------------+------------------+
    ```

8. Tampilkan daftar __negara G20 beserta populasi negaranya, Pendapatan Nasional Bruto/GNP (_Gross National Product_), ibukota & populasi ibukota__. G20 merupakan kelompok 19 negara dengan perekonomian besar di dunia, ditambah dengan Uni Eropa, yang dibentuk sejak 1999 sebagai forum untuk mendiskusikan berbagai masalah kunci di bidang ekonomi dunia. Negara yang terdaftar sebagai anggota G20 adalah: 

    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/1/1a/Flag_of_Argentina.svg/35px-Flag_of_Argentina.svg.png' alt='lintang' style='height:13px; width:18px'/> Argentina 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/8/88/Flag_of_Australia_%28converted%29.svg/35px-Flag_of_Australia_%28converted%29.svg.png' alt='lintang' style='height:13px; width:18px'/> Australia 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/0/05/Flag_of_Brazil.svg/33px-Flag_of_Brazil.svg.png' alt='lintang' style='height:13px; width:18px'/> Brazil 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Flag_of_Canada_%28Pantone%29.svg/35px-Flag_of_Canada_%28Pantone%29.svg.png' alt='lintang' style='height:13px; width:18px'/> Canada 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/f/fa/Flag_of_the_People%27s_Republic_of_China.svg/35px-Flag_of_the_People%27s_Republic_of_China.svg.png' alt='lintang' style='height:13px; width:18px'/> China 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/c/c3/Flag_of_France.svg/35px-Flag_of_France.svg.png' alt='lintang' style='height:13px; width:18px'/> France 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/b/ba/Flag_of_Germany.svg/35px-Flag_of_Germany.svg.png' alt='lintang' style='height:13px; width:18px'/> Germany 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/4/41/Flag_of_India.svg/35px-Flag_of_India.svg.png' alt='lintang' style='height:13px; width:18px'/> India 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/9/9f/Flag_of_Indonesia.svg/35px-Flag_of_Indonesia.svg.png' alt='lintang' style='height:13px; width:18px'/> Indonesia 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/0/03/Flag_of_Italy.svg/35px-Flag_of_Italy.svg.png' alt='lintang' style='height:13px; width:18px'/> Italy 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/9/9e/Flag_of_Japan.svg/35px-Flag_of_Japan.svg.png' alt='lintang' style='height:13px; width:18px'/> Japan 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/f/fc/Flag_of_Mexico.svg/35px-Flag_of_Mexico.svg.png' alt='lintang' style='height:13px; width:18px'/> Mexico 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/f/f3/Flag_of_Russia.svg/35px-Flag_of_Russia.svg.png' alt='lintang' style='height:13px; width:18px'/> Russian Federation 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/0/0d/Flag_of_Saudi_Arabia.svg/35px-Flag_of_Saudi_Arabia.svg.png' alt='lintang' style='height:13px; width:18px'/> Saudi Arabia 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Flag_of_South_Africa.svg/35px-Flag_of_South_Africa.svg.png' alt='lintang' style='height:13px; width:18px'/> South Africa 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/0/09/Flag_of_South_Korea.svg/35px-Flag_of_South_Korea.svg.png' alt='lintang' style='height:13px; width:18px'/> South Korea 
    - <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/b/b4/Flag_of_Turkey.svg/35px-Flag_of_Turkey.svg.png' alt='lintang' style='height:13px; width:18px'/> Turkey
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/a/ae/Flag_of_the_United_Kingdom.svg/35px-Flag_of_the_United_Kingdom.svg.png' alt='lintang' style='height:13px; width:18px'/> United Kingdom 
    - <img src='https://upload.wikimedia.org/wikipedia/en/thumb/a/a4/Flag_of_the_United_States.svg/35px-Flag_of_the_United_States.svg.png' alt='lintang' style='height:13px; width:18px'/> United States
    
    Tampilkan daftar __negara G20 beserta populasi negaranya, Pendapatan Nasional Bruto/GNP (_Gross National Product_), ibukota & populasi ibukota__, dengan kolom yang diwajibkan ada yaitu __nama negara__, __populasi negara__, __pendapatan nasional bruto (GNP)__, __nama ibukota__ dan __populasi ibukota__. Urutkan berdasarkan abjad nama negara. Output yang diharapkan:

    ```bash
    +--------------------+-----------------+------------+-------------------+------------------+
    | Negara_G20         | Populasi_Negara | GNP        | Ibukota           | Populasi_Ibukota |
    +--------------------+-----------------+------------+-------------------+------------------+
    | Argentina          |        37032000 |  340238.00 | Buenos Aires      |          2982146 |
    | Australia          |        18886000 |  351182.00 | Canberra          |           322723 |
    | Brazil             |       170115000 |  776739.00 | BrasÃ­lia          |          1969868 |
    | Canada             |        31147000 |  598862.00 | Ottawa            |           335277 |
    | China              |      1277558000 |  982268.00 | Peking            |          7472000 |
    | France             |        59225700 | 1424285.00 | Paris             |          2125246 |
    | Germany            |        82164700 | 2133367.00 | Berlin            |          3386667 |
    | India              |      1013662000 |  447114.00 | New Delhi         |           301297 |
    | Indonesia          |       212107000 |   84982.00 | Jakarta           |          9604900 |
    | Italy              |        57680000 | 1161755.00 | Roma              |          2643581 |
    | Japan              |       126714000 | 3787042.00 | Tokyo             |          7980230 |
    | Mexico             |        98881000 |  414972.00 | Ciudad de MÃ©xico |          8591309 |
    | Russian Federation |       146934000 |  276608.00 | Moscow            |          8389200 |
    | Saudi Arabia       |        21607000 |  137635.00 | Riyadh            |          3324000 |
    | South Africa       |        40377000 |  116729.00 | Pretoria          |           658630 |
    | South Korea        |        46844000 |  320749.00 | Seoul             |          9981619 |
    | Turkey             |        66591000 |  210721.00 | Ankara            |          3038159 |
    | United Kingdom     |        59623400 | 1378330.00 | London            |          7285000 |
    | United States      |       278357000 | 8510700.00 | Washington        |           572059 |
    +--------------------+-----------------+------------+-------------------+------------------+
    ```

    ✅ Lampirkan jawaban berupa daftar __query SQL & Screenshoot hasil query__ dalam bentuk file __.docx atau .pdf__ dan kirimkan via email ke _khumaeni@purwadhika.com_ dan ke _operational_jkt@purwadhika.com_ Subject Email : **Exam_Modul2_JCDS12_Nama**
    
    <hr>



#

### **Soal 2 - Exploratory Data Analysis (EDA) - 70 Points**
    
Berikut ini tersedia __5 Dataset__ Silakan __Pilih salah satu__ , Kemudian lakukan __Exploratory Data Analysis__ terhadap Dataset yang anda pilih.

Dataset|Unduh csv|Info|Keterangan
-----|-----|-----|-----
Employee |[Employee.csv](./employee.csv)|[Info_Emp](./emp.PNG) , Attrition = keluar|Ini merupakan data karyawan keluar pada suatu perusahaan
Sephora |[Sephora.csv](./sephora.csv)|[Info_Sephora](./Sephora.PNG)|Ini adalah data dari ecommerce Sephora
Supermarket |[Supermarket.csv](./Supermarket.csv)|[Info_Supermarket](./Supermarket.PNG)|Ini merupakan data penjualan dari suatu Supermarket
Seluler | [seluler.csv](./seluler.csv) | Churn = pindah | Ini merupakan data pelanggan operator seluler yg pindah provider dan tidak
Bank | [bank.csv](./bank.csv) | 1 = yes, 0 = no | Ini merupakan data nasabah bank yg pindah bank dan tidak

__Sertakan Alasan ataupun Tujuan disetiap langkah yang anda lakukan, jangan hanya coding tanpa alasan atau penjelasan Fokus pada *Problem Solving*, Detail Poin Penilaian Sebagai Berikut :__


- Definisikan Masalah terkait bisnis yang ingin anda selesaikan (Define Business Problem) - __5 point__
- Definisikan Tujuan EDA anda (Define Goals), Goals harus memiliki **Impact** untuk perusahaan - __5 point__
- Analisa Deskriptif & Handling Missing Value serta Outliers - __10 point__
- Analisis Data (Univariate dan Multivariate, Gunakan `Crosstab` atau `Pivot_Table` atau `Group by` ) - __20 point__
- Visualisasi Data (Univariate dan Multivariate, Gunakan plot sesuai dengan fungsi dan tujuannya) - __20 Point__
- Temukan Insight data berdasarkan Analisis dan Visualisasi yang telah anda lakukan - __5 point__
- Kesimpulan dan Saran serta simulasi **Impact** untuk perusahaan yang dapat anda berikan berdasarkan hasil EDA anda - __5 point__

<hr>


__Untuk mendukung setiap hipotesa anda, Silakan Lakukan Riset dari bermacam sumber dari luar terkait business problem yang anda pilih__


** Note : Alternatif Untuk download dataset bisa dengan membuka file sesuai link, klik **raw** dan copas ke text editor kemudian save as **.csv**


✅ Commit dan Push jawaban anda ke Repository Github anda, beri nama repo anda __Exploratory-Data-Analysis-(Dataset yang anda pilih)__ kemudian kirim __Link repo github__ anda  via email ke _khumaeni@purwadhika.com_ dan ke _operational_jkt@purwadhika.com_ Subject Email : **Exam_Modul2_JCDS12_Nama**
    
<hr>




































#

### *__Good Luck & Happy Coding__* 
