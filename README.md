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
