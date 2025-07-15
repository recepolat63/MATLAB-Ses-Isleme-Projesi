# MATLAB-Ses-Tanima-Projesi

Bu proje, MATLAB kullanılarak geliştirilmiş bir ses tanıma sistemidir. Sistem, belirli ses dosyalarına ait özellikleri analiz eder ve hangi sesin hangi dosyaya ait olduğunu tahmin eder. Toplamda 30 adet `.wav` uzantılı ses dosyası kullanılarak sinir ağı eğitilir ve test edilir.

---

## 🚀 Projeyi Çalıştırma Adımları

### 1. Gerekli Dosyaları Hazırlayın
- `ses1.wav` ile `ses30.wav` arasında adlandırılmış ses dosyalarınızı oluşturun.
- Bu ses dosyalarını ve `Ses Tanima Projesi.m` dosyasını **aynı klasöre**, yani MATLAB'in çalışma dizinine yerleştirin.

### 2. Gerekli Toolbox’lar
Bu proje için aşağıdaki MATLAB toolbox'larının kurulu olması gerekir:

- **Signal Processing Toolbox**
- **Neural Network Toolbox**

Toolbox'ların kurulu olup olmadığını kontrol etmek için MATLAB Komut Penceresi’ne şunu yazabilirsiniz:
```matlab
ver
