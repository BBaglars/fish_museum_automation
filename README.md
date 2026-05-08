# 🐟 AR Balık Müzesi

**AR Balık Müzesi**, Unity 6 ile geliştirilen, artırılmış gerçeklik destekli interaktif bir balık müzesi prototipidir.  
Projenin amacı, balık türlerini AR ortamında kullanıcıya göstermek ve ilerleyen aşamalarda quiz, puanlama ve oyunlaştırılmış öğrenme mekanikleriyle desteklemektir.

---

## 🎯 Proje Amacı

Bu proje, müze ziyaretçileri ve öğrenciler için daha etkileşimli bir öğrenme deneyimi sunmayı hedefler.

Kullanıcılar:

- AR ortamında balık modellerini görüntüleyebilir.
- Algılanan yüzeylere balık modeli yerleştirebilir.
- İlerleyen aşamalarda balıklar hakkında bilgi kartları görebilir.
- Quiz sistemiyle öğrendiklerini test edebilir.
- Doğru cevaplarla puan kazanabilir.

---

## 🚀 Mevcut Durum

Bu repo şu anda projenin ilk AR prototipini içerir.

Tamamlanan temel özellikler:

- Unity projesi oluşturuldu.
- Android platformuna geçildi.
- AR Foundation kuruldu.
- ARCore XR Plugin aktif edildi.
- XR Simulation ile editör içinde test ortamı hazırlandı.
- AR Session ve XR Origin sahnesi kuruldu.
- Plane Detection için `AR Plane Manager` eklendi.
- Yüzeye tıklama algısı için `AR Raycast Manager` eklendi.
- Test amaçlı `TestFish` prefabı oluşturuldu.
- Mouse ve mobil dokunma destekli AR yerleştirme scripti yazıldı.
- Unity Editor içinde XR Simulation ile yüzeye balık yerleştirme başarıyla test edildi.

---

## 🛠️ Kullanılan Teknolojiler

| Teknoloji | Açıklama |
|---|---|
| Unity 6.3 LTS | Ana oyun motoru |
| Unity 6000.3.11f1 | Kullanılan Unity sürümü |
| AR Foundation | Platform bağımsız AR altyapısı |
| ARCore XR Plugin | Android AR desteği |
| XR Simulation | Telefonsuz editör içi AR testi |
| Universal Render Pipeline | Mobil uyumlu render altyapısı |
| C# | Script geliştirme dili |

---

## 📁 Proje Klasör Yapısı

```text
Assets/
└── _Project/
    ├── Art/
    ├── Prefabs/
    │   └── Fish/
    │       └── TestFish.prefab
    ├── Scenes/
    │   └── 01_AR_Museum.unity
    ├── ScriptableObjects/
    └── Scripts/
        ├── AR/
        │   └── FishPlacementController.cs
        ├── Core/
        ├── Data/
        ├── Gamification/
        ├── Quiz/
        ├── UI/
        └── Utilities/
```

---

## 🧩 Önemli Scriptler

### `FishPlacementController.cs`

Bu script, AR ortamında yüzeye tıklanınca balık prefabını yerleştirir.

Desteklenen girişler:

- Mouse sol tık
- Mobil dokunma

Temel görevleri:

- Ekran pozisyonunu alır.
- AR Raycast ile yüzey kontrolü yapar.
- İlk tıklamada balık prefabını oluşturur.
- Sonraki tıklamalarda balığı yeni konuma taşır.

---

## 🧪 Test Durumu

Şu anda proje Android telefon olmadan **XR Simulation** ile test edilmiştir.

Başarıyla test edilen akış:

```text
Unity Editor açılır.
Play Mode başlatılır.
XR Simulation sahnesi yüklenir.
Kullanıcı zemine tıklar.
TestFish prefabı yüzeye yerleşir.
```

---

## 📌 MVP Hedefi

Projenin ilk MVP hedefi:

```text
Balığı AR ortamında göster,
kullanıcıya bilgi ver,
soru sor,
doğru cevapta besleme animasyonu oynat,
puanı kaydet.
```

---

## 🗺️ Geliştirme Yol Haritası

### Faz 1 — AR Temel Deneyim

- [x] Unity projesi oluşturma
- [x] Android platform ayarı
- [x] AR Foundation kurulumu
- [x] ARCore ayarı
- [x] XR Simulation kurulumu
- [x] AR sahnesi oluşturma
- [x] Plane Detection ekleme
- [x] Raycast ile yüzeye obje yerleştirme
- [x] TestFish prefabı oluşturma

### Faz 2 — Balık Model Sistemi

- [ ] Gerçek balık modeli import etme
- [ ] Model scale ve pivot ayarlarını düzenleme
- [ ] Balık prefab standardı oluşturma
- [ ] Material ve texture optimizasyonu
- [ ] FishProfile ScriptableObject sistemi kurma

### Faz 3 — Bilgi Kartı ve UI

- [ ] Balık bilgi paneli oluşturma
- [ ] Balık adı, açıklama ve tür bilgisi gösterme
- [ ] Mobil uyumlu UI tasarımı
- [ ] Basit HUD sistemi

### Faz 4 — Quiz Sistemi

- [ ] Soru veri modeli oluşturma
- [ ] Quiz paneli hazırlama
- [ ] Çoktan seçmeli cevap sistemi
- [ ] Doğru / yanlış cevap kontrolü
- [ ] Açıklama metni gösterme

### Faz 5 — Oyunlaştırma

- [ ] Puan sistemi
- [ ] Doğru cevap sonrası besleme animasyonu
- [ ] Basit ödül sistemi
- [ ] Kullanıcı ilerleme takibi

### Faz 6 — Firebase Entegrasyonu

- [ ] Firebase Realtime Database bağlantısı
- [ ] Firebase Storage bağlantısı
- [ ] Soru verilerini Firebase’den çekme
- [ ] Skor kaydetme
- [ ] Öğretmen/admin veri yönetimi altyapısı

### Faz 7 — Android Cihaz Testi

- [ ] Gerçek Android cihazda ARCore testi
- [ ] Kamera izni kontrolü
- [ ] Yüzey algılama testi
- [ ] Performans testi
- [ ] APK/AAB build hazırlığı

---

## 📱 Hedef Platform

İlk hedef platform:

```text
Android / ARCore
```

İlerleyen aşamalarda proje mimarisi uygun hale getirilirse iOS desteği de eklenebilir.

---

## ⚙️ Kurulum

Projeyi klonla:

```bash
git clone https://github.com/BBaglars/fish_museum_automation.git
```

Proje klasörüne gir:

```bash
cd fish_museum_automation
```

Unity Hub üzerinden projeyi aç:

```text
Unity Version: 6000.3.11f1
```

Gerekli paketler Unity tarafından `Packages/manifest.json` üzerinden yüklenecektir.

---

## ▶️ Çalıştırma

Unity içinde şu sahneyi aç:

```text
Assets/_Project/Scenes/01_AR_Museum.unity
```

Sonra:

```text
Play
```

butonuna bas.

XR Simulation ortamında sol tık ile yüzeye balık yerleştirme test edilebilir.

---

## 🧠 Teknik Notlar

- Gerçek ARCore testi için Android cihaz gereklidir.
- Laptop kamerası ARCore yerine geçmez.
- Telefonsuz geliştirme için XR Simulation kullanılmaktadır.
- Unity `Library`, `Temp`, `Obj`, `Build` gibi klasörler repoya dahil edilmemelidir.
- Büyük model dosyaları ileride Git LFS ile yönetilebilir.

---

## 🧱 Gelecek Planları

- Gerçek balık modelleri eklemek
- Marker-based tracking desteği eklemek
- Balık bilgi kartları oluşturmak
- Quiz sistemi geliştirmek
- Besleme animasyonu eklemek
- Firebase üzerinden dinamik içerik yönetimi sağlamak
- Öğretmen paneli geliştirmek
- Offline mod ve 2D fallback sistemi eklemek

---

## 👥 Geliştiriciler

Berkay BAĞLARS - 245541020
Aziz BOLAT - 225541123
Yunus GÜÇLÜ - 225541089
Mert Kaan KİNDAR - 225541039

---

## 📄 Lisans

Bu proje geliştirme aşamasındadır.  
Lisans bilgisi ilerleyen sürümlerde netleştirilecektir.