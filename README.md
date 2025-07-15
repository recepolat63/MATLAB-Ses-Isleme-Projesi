## -TR-
# MATLAB Ses Tanıma Projesi

Bu proje, MATLAB ortamında geliştirilmiş bir ses tanıma sistemidir. Sistem, `.wav` formatında toplam 30 farklı ses dosyasını analiz ederek hangi sesin hangi sınıfa ait olduğunu tahmin etmeyi amaçlar. Analiz sürecinde FFT (Fast Fourier Transform), istatistiksel öznitelikler ve çok katmanlı yapay sinir ağı (patternnet) kullanılmıştır.

## 📋 Proje Özeti

30 adet ses dosyası (ses1.wav – ses30.wav) projeye dahil edilir. FFT ve zaman temelli yöntemlerle her ses dosyasından öznitelikler çıkarılır. Çıkarılan öznitelikler normalize edilir. Veri çoğaltma (data augmentation) tekniğiyle eğitim verisi genişletilir. Sinir ağı eğitilir ve test verisi üzerinden tahminler yapılır. Sistem hem doğruluk oranını hesaplar hem de sonuçları grafiklerle gösterir.

## 🧰 Gerekli Toolbox’lar

Bu proje için MATLAB ortamında Signal Processing Toolbox ve Neural Network Toolbox kurulu olmalıdır. Bu toolbox'ların kurulu olup olmadığını kontrol etmek için MATLAB komut penceresine `ver` yazılabilir. Eksik olanlar MATLAB Add-On Explorer üzerinden kurulabilir.

## ▶️ Projeyi Çalıştırma

Proje klasörü içine `ses_dosyalari` adında bir klasör oluşturulmalı ve içine sırasıyla ses1.wav, ses2.wav ... ses30.wav dosyaları eklenmelidir. Proje klasörünün yapısı aşağıdaki gibi olmalıdır:

proje_klasoru/  
├── Ses_Tanima_Projesi.m  
├── README.md  
└── ses_dosyalari/  
  ├── ses1.wav  
  ├── ses2.wav  
  └── ...  

Ses_Tanima_Projesi.m dosyasında ses okuma işlemi şu şekilde yazılmış olmalıdır:  
`[y, fs] = audioread(sprintf('ses_dosyalari/ses%d.wav', i));`

MATLAB açılır ve çalışma dizini proje klasörüne ayarlanır. Daha sonra Ses_Tanima_Projesi.m dosyası açılır ve Run butonuna basılarak veya komut penceresine `run('Ses_Tanima_Projesi.m')` komutu yazılarak proje çalıştırılır. Kod çalıştırıldığında sistem ses dosyalarını yükler, öznitelikleri çıkarır, sinir ağını eğitir, tahmin yapar ve doğruluk oranını hesaplayarak komut penceresinde gösterir. Ayrıca confusionchart ile sınıflandırma matrisi ve FFT spektrumlarını içeren grafikler oluşturur.

## 📂 Dosya Açıklamaları

Ses_Tanima_Projesi.m – Ana MATLAB kod dosyası  
ses_dosyalari/ – Ses dosyalarının yer aldığı klasör (kullanıcı tarafından oluşturulmalı)  
README.md – Bilgilendirme ve kullanım kılavuzu

## 👤 Geliştirici

Recep Polat  
GitHub: [@recepolat63](https://github.com/recepolat63)

## 📝 Lisans

Bu proje açık kaynaklıdır ve kişisel, akademik amaçlarla serbestçe kullanılabilir. Ticari kullanım için geliştiriciyle iletişime geçilmesi tavsiye edilir.




## -EN-

# MATLAB Speech Recognition Project
This project is a speech recognition system developed in the MATLAB environment. The system analyzes a total of 30 different .wav audio files to predict which class each sound belongs to. The analysis process uses FFT (Fast Fourier Transform), statistical features, and a multilayer artificial neural network (patternnet).

## 📋 Project Overview
30 audio files (ses1.wav – ses30.wav) are included in the project. Features are extracted from each audio file using FFT and time-domain methods. Extracted features are normalized. The training data is expanded using data augmentation techniques. The neural network is trained and predictions are made on the test data. The system calculates accuracy and displays the results with graphs.

## 🧰 Required Toolboxes
Signal Processing Toolbox and Neural Network Toolbox must be installed in the MATLAB environment for this project. To check if these toolboxes are installed, type ver in the MATLAB command window. Missing toolboxes can be installed via the MATLAB Add-On Explorer.

## ▶️ How to Run the Project
Create a folder named ses_dosyalari inside the project directory and add audio files named ses1.wav, ses2.wav ... ses30.wav into it. The project folder structure should be as follows:

project_folder/
├── Speech_Recognition_Project.m
├── README.md
└── ses_dosyalari/
  ├── ses1.wav
  ├── ses2.wav
  └── ...

The audio reading code in Speech_Recognition_Project.m should be written as:
[y, fs] = audioread(sprintf('ses_dosyalari/ses%d.wav', i));

Open MATLAB and set the current folder to the project directory. Then open Speech_Recognition_Project.m and either click the Run button or type run('Speech_Recognition_Project.m') in the command window to execute the project. When run, the system loads the audio files, extracts features, trains the neural network, makes predictions, calculates accuracy, and displays it in the command window. It also generates graphs including the confusion matrix and FFT spectra.

## 📂 File Descriptions
Speech_Recognition_Project.m – Main MATLAB code file
ses_dosyalari/ – Folder containing the audio files (to be created by the user)
README.md – Information and user guide

## 👤 Developer
Recep Polat
GitHub: @recepolat63

## 📝 License
This project is open source and free to use for personal and academic purposes. For commercial use, please contact the developer.
