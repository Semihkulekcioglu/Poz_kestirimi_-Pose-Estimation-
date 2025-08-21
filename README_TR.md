İngilizce dokümantasyon için `README.md` dosyasına bakın.

## Poz Kestirimi (MediaPipe, Python)

Bu depo, MediaPipe ve OpenCV kullanarak gerçek zamanlı insan pozu kestirimi (iskelet noktaları) yapan küçük bir uygulama içerir. Uygulama, hem web kamera hem de yerel video dosyasıyla çalışabilir ve her kare üzerine iskelet bağlantılarını çizer, FPS bilgisini gösterir.

### Özellikler
- Web kamera ile gerçek zamanlı çalıştırma
- Video dosyasıyla çevrimdışı test
- MediaPipe iskelet bağlantılarının çizdirilmesi
- FPS bilgisinin ekrana yazdırılması

### Depo Yapısı
- `Poz_kestirimi(Pose Estimation).py` — ana betik
- `Screenshots/` — örnek çıktı görselleri
- `video*.mp4` — test videoları
- `requirements.txt` — bağımlılıklar
- `.gitignore` — temel Python/IDE dışlamaları

### Gereksinimler
- Python 3.9+
- OpenCV, MediaPipe, NumPy

Kurulum:
```bash
pip install -r requirements.txt
```

### Hızlı Başlangıç
Web kamera ile çalıştır:
```bash
python "Poz_kestirimi(Pose Estimation).py"
```

Video dosyası ile çalıştırmak için kodda giriş kaynağını değiştirin:
```python
#cap = cv2.VideoCapture("video5.mp4")
cap = cv2.VideoCapture(0)
```
Bunu şu şekilde güncelleyin:
```python
cap = cv2.VideoCapture("video5.mp4")
#cap = cv2.VideoCapture(0)
```
Kaydedip betiği yeniden çalıştırın.

### İpuçları
- `0` numaralı kamera çalışmıyorsa `1` deneyin.
- Video yolu bulunamazsa dosyayı betikle aynı klasöre koyun veya tam yol kullanın.
- Programdan çıkmak için görüntü penceresini kapatın.

### Sorun Giderme
- MediaPipe kurulum hataları: `pip` ve `setuptools` güncelleyip tekrar kurun:
  ```bash
  python -m pip install --upgrade pip setuptools
  pip install -r requirements.txt --upgrade --force-reinstall
  ```
- Kamera boş kare dönüyor: Kamerayı kullanan başka bir uygulamayı kapatın.
- Performans düşükse: Giriş çözünürlüğünü düşürün veya `waitKey` süresini artırın.

### Yol Haritası
- Kilit noktalarını CSV/JSON’a aktarma
- Basit açı/aktivite hesaplamaları

