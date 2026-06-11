# 1/64 Stand Builder — Axle Database

1/64 ölçekli araçların aks ve teker ölçülerini içeren veritabanı. Her araç için MakerWorld'e tek tıkla yapıştırılabilir SCAD parametreleri üretir.

## 🚀 GitHub Pages'e Yayınlama

1. Bu repoyu GitHub'a yükleyin
2. Repo ayarlarına gidin → **Pages**
3. Source: `Deploy from a branch` → `main` → `/ (root)` seçin
4. Kaydedin — birkaç dakika içinde siteniz yayında!

URL: `https://KULLANICIADINIZ.github.io/REPO-ADI/`

## ➕ Yeni Araç Ekleme

`index.html` dosyasını açın, `CARS` dizisini bulun ve şu formatta yeni nesne ekleyin:

```javascript
{
  id: 5,                          // Sıradaki ID numarası
  name: "Ferrari F40",            // Araç adı
  brand: "Hot Wheels",            // Üretici marka
  series: "Mainline",             // Seri
  year: 2025,                     // Yıl
  code: "ABC12",                  // Ürün kodu
  tags: ["Treasure Hunt"],        // Etiketler (opsiyonel)
  image: "images/ferrari-f40.jpg", // Görsel yolu veya URL (opsiyonel)
  measurements: {
    wheelbase: 41.0,                    // Dingil mesafesi (mm)
    front_wheel_diameter: 12.0,         // Ön teker çapı (mm)
    front_wheel_width: 5.0,             // Ön teker genişliği (mm)
    front_wheels_inner_distance: 15.0,  // Ön tekerlerin iç mesafesi (mm)
    rear_wheel_diameter: 12.0,          // Arka teker çapı (mm)
    rear_wheel_width: 5.0,              // Arka teker genişliği (mm)
    rear_wheels_inner_distance: 19.0,   // Arka tekerlerin iç mesafesi (mm)
  }
}
```

## 🖼️ Görsel Ekleme

1. `images/` klasörü oluşturun
2. Görselleri oraya koyun
3. Araç nesnesinde `image: "images/dosya-adi.jpg"` şeklinde belirtin

## 🎨 MakerWorld Kullanımı

1. Sitede aracı bulun
2. **SCAD Kopyala** butonuna tıklayın
3. MakerWorld'deki Axle Plate Creator modelini açın
4. Parametreler paneline gidin → sağ üstte "Paste parameters" veya metin alanına yapıştırın
5. Model otomatik olarak o araca göre şekillenir!

## 🏷️ Tag Renkleri

Yeni tag rengi eklemek için `index.html`'deki `TAG_COLORS` objesini düzenleyin:

```javascript
const TAG_COLORS = {
  "Yeni Tag": "tag-purple",  // tag-blue, tag-amber, tag-green, tag-purple
};
```

## 📬 Katkı Sağlama

Araç ölçülerinizi göndermek için sayfadaki **Ölçü Gönder** butonunu kullanın.
