## Tentang Dataset

Gastroenteritis akut (AG) adalah penyakit umum, biasanya disebabkan oleh infeksi virus atau bakteri pada saluran pencernaan. Kasus yang parah dari enteritis bakteri mungkin memerlukan agen antimikroba. Membedakan enteritis bakteri dari enteritis virus sangat penting dalam pengobatan gastroenteritis akut pada anak-anak. Terutama di lingkungan yang kurang dilengkapi, penentuan organisme AG pada saat pemeriksaan bergantung pada temuan dari dokter anak, tetapi indikator khusus tidak jelas.

Data RNA-seq menyarankan bahwa profil RNA dalam darah dapat membedakan antara anak-anak yang terkena gastroenteritis dan yang sehat.

255 sampel darah lengkap dari 246 anak termasuk anak-anak dengan diare yang disebabkan oleh rotavirus, E. coli, Salmonella, Shigella, adenovirus, norovirus, dan anak-anak kontrol.

Meta-data berisi 19 fitur, termasuk usia, skor WHO, jenis kelamin, tinggi, berat badan, sel darah putih (WBC), neutrofil, limfosit, monosit, eosinofil, basofil, sel darah merah (RBC), trombosit, suhu tertinggi, durasi hari, hari setelah onset, dan dosis vaksin rotavirus.

## Ringkasan Referensi

Gastroenteritis akut pada anak merupakan kondisi umum dan berpotensi serius, sering disebabkan oleh infeksi virus (Dalby-Payne, 2011; Sturmberg, 1999; Alhammad, 2021). Gejala utamanya meliputi diare, muntah, mual, demam, dan nyeri perut (Dalby-Payne, 2011). Dehidrasi merupakan kekhawatiran yang signifikan, dan reintroduksi makanan biasa secara dini dapat membantu mempersingkat penyakit (Sturmberg, 1999). Rehidrasi, baik secara oral maupun intravena, adalah dasar terapi (Alhammad, 2021).

Penelitian telah menunjukkan bahwa sampel RNA dapat digunakan untuk menentukan penyebab gastroenteritis akut pada anak-anak. Chen (2017) menemukan bahwa anak-anak dengan gastroenteritis virus akut yang parah memiliki keragaman mikroba usus yang signifikan berkurang, terutama mereka yang terinfeksi rotavirus. Takanashi (2009) mendeteksi RNA norovirus dalam darah 15% anak dengan gastroenteritis norovirus, menunjukkan adanya virus dalam aliran darah. Akhter (2014) mengidentifikasi norovirus sebagai virus paling umum pada anak-anak dengan gastroenteritis, diikuti oleh rotavirus. Chen (2006) juga menemukan bahwa norovirus merupakan penyebab utama gastroenteritis akut pada anak-anak. Studi-studi ini secara kolektif menyarankan bahwa sampel RNA dapat digunakan untuk mendeteksi dan membedakan antara penyebab virus dan bakteri dari gastroenteritis akut pada anak-anak.

Penelitian dari (Miyagi, 2023) menggunakan decision tree classifier, memanfaatkan LASSO untuk seleksi fitur. Evaluasinya menggunakan 5 fold cross-validation dengan skor AUC sebesar 0.80. Tiga fitur paling penting antara lain platelet-lymphocyte ratio, eosinophil count, dan leukocyte count.

## Penjelasan dan Relevansi Fitur

Fitur pada GSE69529_metadata.csv
1. `lib_id`: ID sampel darah.
2. `sample_name`: Nama sampel.
3. `infection_group`: Kelompok infeksi yang menyebabkan gastroenteritis akut pada anak-anak, misalnya rotavirus, E. coli, Salmonella, dll.
4. `age: months`: Usia anak dalam bulan.
5. `age_group`: Grup usia anak (binning dari `age`).
6. `who_score`: Skor pertumbuhan [WHO](https://www.who.int/publications/i/item/9789241547635) untuk menilai status gizi dan pertumbuhan anak.
7. `sex`: Jenis kelamin anak (pria atau wanita).
8. `height: m`: Tinggi anak dalam meter.
9. `weight: kg`: Berat badan anak dalam kilogram.
10. `wbc: 10^6/L`: Jumlah sel darah putih (leukosit) per liter darah.
11. `neutrophils, 10^6/L`: Jumlah neutrofil per liter darah.
12. `lymphocytes, 10^6/L`: Jumlah limfosit per liter darah.
13. `monocytes, 10^6/L`: Jumlah monosit per liter darah.
14. `eosinophils, 10^6/L`: Jumlah eosinofil per liter darah.
15. `basophils, 10^6/L`: Jumlah basofil per liter darah.
16. `red blood cell, 10^6/uL`: Jumlah sel darah merah (eritrosit) per mikroliter darah.
17. `platelets, cells/uL`: Jumlah trombosit per mikroliter darah.
18. `highest_temp`: Suhu tubuh tertinggi yang dicatat selama episode gastroenteritis.
19. `duration_days`: Durasi hari dari episode gastroenteritis.
20. `days_past_onset`: Hari sejak awal gejala gastroenteritis.
21. `rotavirus vaccine doses`: Jumlah dosis vaksin rotavirus yang diberikan kepada anak.

Terdapat hampir 15% sampel ada di data RNA namun tidak ada di metadata dan sekitar 20% sampel yang ada di metadata tetapi tidak ada di data RNA. Data RNA yang dimaksud adalah seluruh data TPM (contohnya GSE69529_TPM_genesymbol.csv). Jika ketidak serasian data ini dibuang atau diambil data yang tersedia saja, maka akan menyisakan sekitar 150 sampel saja. Merujuk ke penelitian yang sebelumnya yang diinisiasi oleh (Miyagi, 2023), maka pada penelitian ini akan memanfaatkan data GSE69529_metadata.


## Daftar Pustaka

```
Akhter, S., Türegün, B., Kiyan, M., Gerçeker, D., Güri̇Z, H., & Şahi̇N, F. (2014). Investigation of Seven Different RNA Viruses Associated with Gastroenteritis in Children Under Five Years Old. Mikrobiyoloji Bulteni, 48(2), 233–241. https://doi.org/10.5578/mb.7374

Alhammad, M. A., Alanazi, S. S., Hassan, Z., Almadan, Thiga, G. A., Alabbas, A., Abdulmajid, Z., Almubarak, Hijazi, M., Albalawi, S., Ghurmullah, D., Alzahrani, Almaghrabi, M. A., & Almasri, D. (2021). Acute Gastroenteritis in Children, Overview, Etiology, and Management; Literature Review. https://www.semanticscholar.org/paper/Acute-Gastroenteritis-in-Children%2C-Overview%2C-and-Alhammad-Alanazi/d2911bad6cf29721b7a3da33431bb70e07023564

Chen, S.-M., Ni, Y.-H., Chen, H.-L., & Chang, M.-H. (2006). Microbial Etiology of Acute Gastroenteritis in Hospitalized Children in Taiwan. Journal of the Formosan Medical Association, 105(12), 964–970. https://doi.org/10.1016/S0929-6646(09)60280-1

Chen, S.-Y., Tsai, C.-N., Lee, Y.-S., Lin, C.-Y., Huang, K.-Y., Chao, H.-C., Lai, M.-W., & Chiu, C.-H. (2017). Intestinal microbiome in children with severe and complicated acute viral gastroenteritis. Scientific Reports, 7(1), 46130. https://doi.org/10.1038/srep46130

Dalby-Payne, J., & Elliott, E. (2008). Gastroenteritis in children. BMJ clinical evidence. https://www.semanticscholar.org/paper/Gastroenteritis-in-children.-Dalby-Payne-Elliott/3f5cd38d689da23782f7ae43345eb743e0a5b6ad

Miyagi, Y. (2023). Identification of Pediatric Bacterial Gastroenteritis From Blood Counts and Interviews Based on Machine Learning. Cureus, 15(8). https://doi.org/10.7759/cureus.43644

Sturmberg, J., & Watt, P. (1999). Acute gastroenteritis in children. Australian family physician. https://www.semanticscholar.org/paper/Acute-gastroenteritis-in-children.-Sturmberg-Watt/8ce551861aeae6b81fbe1449c0cfb22ddf06dbf5

Takanashi, S., Hashira, S., Matsunaga, T., Yoshida, A., Shiota, T., Tung, P. G., Khamrin, P., Okitsu, S., Mizuguchi, M., Igarashi, T., & Ushijima, H. (2009). Detection, genetic characterization, and quantification of norovirus RNA from sera of children with gastroenteritis. Journal of Clinical Virology, 44(2), 161–163. https://doi.org/10.1016/j.jcv.2008.11.011
```
