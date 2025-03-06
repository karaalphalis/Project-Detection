# YOLO ile Proje Tespiti (Project Detection) Modeli
Bu proje, YOLOv8 derin öğrenme modeli kullanılarak nesne tespiti gerçekleştiren bir Project-Detection sistemini içermektedir. YOLO (You Only Look Once), gerçek zamanlı nesne tespiti ve sınıflandırma için kullanılan bir derin öğrenme modelidir. Bu projede, özel veri setleri üzerinde eğitim yaparak belirli nesneleri tespit etmek ve sınıflandırmak amaçlanmaktadır.

🚀 Özellikler
YOLOv8 Kullanımı: Ultralytics YOLOv8 modeli ile yüksek doğrulukta nesne tespiti.
Özel Veri Seti Desteği: Farklı projelere uygun özel veri setleriyle eğitim.
Gerçek Zamanlı Tespit: Kamera veya video akışında anlık tespit imkanı.
Kolay Entegrasyon: Python ve OpenCV desteği ile esnek kullanım.
PyTorch Desteği: Model eğitimi ve test işlemleri için PyTorch kullanımı.
🔧 Kurulum ve Kullanım
1️⃣ Gerekli Kütüphaneleri Kurun
bash
Kopyala
Düzenle
pip install ultralytics opencv-python torch torchvision
2️⃣ Modeli Eğitme
Özel veri setiniz varsa, YOLO formatına çevirerek aşağıdaki komutu çalıştırabilirsiniz:

bash
Kopyala
Düzenle
yolo task=detect mode=train model=yolov8n.pt data=dataset.yaml epochs=50
3️⃣ Modeli Test Etme
Eğitilmiş modeli test etmek için:

bash
Kopyala
Düzenle
yolo task=detect mode=val model=runs/train/exp/weights/best.pt data=dataset.yaml
4️⃣ Gerçek Zamanlı Tespit
Web kamerası üzerinden nesne tespiti yapmak için:

bash
Kopyala
Düzenle
yolo task=detect mode=predict model=runs/train/exp/weights/best.pt source=0
📌 Kullanım Alanları
Savunma sanayi ve askeri uygulamalar
Güvenlik sistemleri ve akıllı şehirler
Endüstriyel kalite kontrol
Tarım ve sağlık sektörü
