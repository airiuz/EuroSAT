## Tensorflow datasets: EuroSAT dataseti

<p align="center">
  <img src="https://github.com/MisterFoziljon/EuroSAT/blob/main/rasmlar/Eurosat.jpg" />
</p>

#### 1. ```EuroSAT``` dataseti haqida qisqacha ma'lumot
```EuroSAT``` dataseti Sentinel-2 sun'iy yo'ldoshi yordamida tasvirga olingan yerning turli hududlari va qoplamalaridagi 80x80x3 
o'lchamli rasmlar to'plamidan iborat. Ushbu dataset 13 ta spektral diapazonga ega bo'lib, quyidagi 10 ta sinfni o'z ichiga qamrab oladi:
1. AnnualCrop
2. Pasture
3. River
4. HerbaceousVegetation
5. Highway
6. SeaLake
7. Residential
8. PermanentCrop
9. Industrial
10. Forest

Dataset parametrlari:

* Versiya: 2.0.0 
* Manba: https://www.tensorflow.org/datasets/catalog/eurosat
* Manba kodi: tfds.image_classification.Eurosat
* Dataset hajmi: 89.91 MB 

#### 2. Loyihani yuklab olish uchun quyidagi ketma-ketlikni bajaring:
  * `windows+R` klavishlarini bosing va paydo bo'lgan oynaga `cmd` buyrug'ini yozing OK tugmachasini bosing.
  
  ![cmd](https://github.com/MisterFoziljon/EuroSAT/blob/main/rasmlar/cmd.png)

  * Loyihani quyidagi link yordamida yuklab oling. (Loyiha uchun yaratilgan fayl adresni o'zingiz ko'rsatishingiz mumkin)

        C:\> git clone https://github.com/MisterFoziljon/EuroSAT.git

  * Loyiha joylashgan faylga kiring.
         
        C:\> cd EuroSAT


#### 3. Proyektni ishlatish uchun kerakli modullarni virtual environment yaratib o'rnatib oling.
* O'zingizdagi pip ni so'nggi versiyasiga yangilang.

        C:\EuroSAT> python -m pip install --upgrade pip
        
* virtual environment yaratish uchun virtualenv modulini o'rnating.
        
        C:\EuroSAT> python -m pip install --user virtualenv

* Yangi environment yaratish uchun unga nom bering.
        
        C:\EuroSAT> python -m venv sizning_env
        
* Virtual environmentni ishga tushiring(aktivlashtiring).
        
        C:\EuroSAT> sizning_env\Scripts\activate.bat
        
* Virtual environment ichiga loyiha ishlashi uchun kerakli bo'lgan modullarni o'rnating (requirements.txt faylining ichida barchasi mavjud).
        
        (sizning_env) C:\EuroSAT> pip install -r requirements.txt


#### 4. Proyektni ishlatish uchun jupyter notebook ni ishga tushiring.

        (sizning_env) C:\EuroSAT> jupyter notebook
        
  * ```Eurosat.ipynb``` ni ishga tushiring. 
  * Usbu notebookda [Tensorflow.org](https://www.tensorflow.org/) saytidagi [eurosat](https://www.tensorflow.org/datasets/catalog/eurosat?hl=ru) datasetini o'qib olish, uni train va test datalariga ajratish, datalarni size va shape larini train uchun moslash hamda normallashtirish ko'rsatilgan. 
  * Dataset yordamida Convolutional Neural Network ishlab chiqilgan va u yordamida model train va evaluate qilingan. Model fayl ko'rinishida saqlanadi. 
  * Notebook yordamida saqlangan modelni load qilish va yangi test qilish datalari yordamida bashorat qilish (predict) ko'rsatib o'tilgan. 
  * [Modelni yuklab olish](https://drive.google.com/drive/folders/1xEv6qVREdSjaw07oVx-wjVCKkymufu2g?usp=share_link)
 

#### 5. Proyektni streamlit yordamida deploy qilish.

        (sizning_env) C:\EuroSAT> streamlit run streamlit.py

  * Proyekt ```local server```da ishga tushadi va quyidagicha ko'rinishda bo'ladi:


![streamlit1](https://github.com/MisterFoziljon/EuroSAT/blob/main/rasmlar/streamlit2.png)
  
  * Rasm faylini yuklab oling va ```Predict``` tugmachasini bosing. Model yuklab olingan tasvirni qaysi turkumga tegishli ekanligini bashorat qiladi. Bundan tashqari softmaxdan chiqqan ehtimollik natijasi ham ekranga chiqadi.


![streamlit3](https://github.com/MisterFoziljon/EuroSAT/blob/main/rasmlar/streamlit1.png)
