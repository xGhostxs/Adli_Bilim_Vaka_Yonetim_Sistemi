# VAKA_AI - Akıllı Vaka Yönetim Sistemi

![Version](https://img.shields.io/badge/version-0.0.0-blue)
![React](https://img.shields.io/badge/React-19.2.0-61DAFB?logo=react)
![Vite](https://img.shields.io/badge/Vite-7.2.4-646CFF?logo=vite)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4.1-38B2AC?logo=tailwindcss)

VAKA_AI, adalet ve güvenlik profesyonelleri için tasarlanmış modern, kapsamlı bir vaka yönetim ve analiz platformudur. Dedektif, savcı, polis ve hukuk müşavirleri için vakaları etkili bir şekilde yönetmeyi, kanıtları organize etmeyi ve raporlar oluşturmayı sağlar.

## 📋 İçindekiler

- [Özellikler](#-özellikler)
- [Teknoloji Stack](#-teknoloji-stack)
- [Kurulum](#-kurulum)
- [Kullanım](#-kullanım)
- [Proje Yapısı](#-proje-yapısı)
- [Modüller](#-modüller)
- [API ve Context](#-api-ve-context)
- [Geliştirme](#-geliştirme)
- [Build ve Deployment](#-build-ve-deployment)
- [Katkıda Bulunma](#-katkıda-bulunma)

## ✨ Özellikler

### Temel Özellikler
- **📊 Dinamik Dashboard**: Tüm vakaların hızlı görünümü ve istatistikleri
- **📁 Vaka Yönetimi**: Yeni vaka oluşturma, düzenleme ve silme
- **🔍 Kanıt Modülü**: Delilleri kategorize etme, etiketleme ve organize etme
- **📅 Zaman Çizelgesi**: Olayların kronolojik sırasını görselleştirme
- **👥 Tanık Yönetimi**: Tanık bilgilerini kayıt etme ve yönetme
- **🔗 Bağlantı Modülü**: Kişiler, yerler ve olaylar arasındaki ilişkileri haritalandırma
- **🗺️ Harita Modülü**: Olay yerlerini ve önemli konumları coğrafi olarak görselleştirme
- **📄 Raporlama**: Profesyonel PDF raporlar oluşturma
- **⚡ Hızlı İşlemler**: Vite ile hot module replacement (HMR) desteği

### Teknik Özellikler
- Modüler ve ölçeklenebilir mimari
- React Context API ile durum yönetimi
- Tailwind CSS ile responsive tasarım
- ESLint ile kod kalitesi kontrolü
- Modern React 19 özellikleri

## 🛠️ Teknoloji Stack

### Frontend Framework
- **React** (^19.2.0) - UI kütüphanesi
- **React DOM** (^19.2.0) - React kütüphanesinin DOM adaptörü

### Build Tools
- **Vite** (^7.2.4) - Hızlı build tool ve dev server
- **@vitejs/plugin-react** (^5.1.1) - React için Vite plugin

### Styling
- **Tailwind CSS** (^3.4.1) - Utility-first CSS framework
- **PostCSS** (^8.5.6) - CSS dönüştürme
- **AutoPrefixer** (^10.4.23) - CSS prefixleri otomatik ekleme

### Utilities
- **Lucide React** (^0.562.0) - Modern SVG ikonları
- **jsPDF** (^4.0.0) - PDF oluşturma kütüphanesi
- **jsPDF AutoTable** (^5.0.7) - PDF tablolar oluşturma

### Development Tools
- **ESLint** (^9.39.1) - JavaScript linter
- **eslint-plugin-react-hooks** (^7.0.1) - React Hooks ESLint kuralları
- **eslint-plugin-react-refresh** (^0.4.24) - React refresh ESLint kuralları

## 📦 Kurulum

### Ön Gereksinimler
- Node.js (14.0.0 veya üzeri)
- npm veya yarn

### Adımlar

1. **Depoyu Klonlayın**
```bash
git clone <repository-url>
cd vaka_ai
```

2. **Bağımlılıkları Yükleyin**
```bash
npm install
```

3. **Geliştirme Sunucusunu Başlatın**
```bash
npm run dev
```

Uygulama `http://localhost:5173` adresinde açılacaktır.

4. **Kodu Lint'leyin**
```bash
npm run lint
```

## 🚀 Kullanım

### Hızlı Başlangıç

Uygulama açıldığında otomatik olarak örnek bir vaka yüklenecektir. Ardından şunları yapabilirsiniz:

1. **Dashboard'dan Başlayın**: Tüm vakaları görüntüleyin
2. **Yeni Vaka Oluşturun**: "Yeni Vaka" düğmesine tıklayın
3. **Vaka Detaylarını Açın**: Bir vaka seçerek detaylarını görüntüleyin
4. **Kanıtlar Ekleyin**: Evidence modülünde kanıtları ekleyin
5. **Raporlar Oluşturun**: Reports modülünde PDF raporlar oluşturun

### Komut Satırı

| Komut | Açıklama |
|-------|----------|
| `npm run dev` | Geliştirme sunucusunu başlat (HMR ile) |
| `npm run build` | Üretim için build oluştur |
| `npm run lint` | ESLint ile kodu kontrol et |
| `npm run preview` | Build edilmiş uygulamayı önizleme sunucusunda çalıştır |

## 📁 Proje Yapısı

```
vaka_ai/
├── public/                          # Statik dosyalar
├── src/
│   ├── assets/                      # Resimler, fontlar vb.
│   ├── components/                  # React bileşenleri
│   │   ├── layout/
│   │   │   └── Header.jsx          # Üst navigasyon çubuğu
│   │   ├── Dashboard.jsx           # Ana sayfa
│   │   ├── CaseDetail.jsx          # Vaka detay sayfası
│   │   ├── EvidenceModule.jsx      # Kanıt yönetimi
│   │   ├── TimelineModule.jsx      # Zaman çizelgesi
│   │   ├── WitnessModule.jsx       # Tanık yönetimi
│   │   ├── ConnectionsModule.jsx   # Bağlantılar haritası
│   │   ├── MapModule.jsx           # Coğrafi harita
│   │   └── ReportsModule.jsx       # Raporlama
│   ├── context/
│   │   └── CaseContext.jsx         # Global durum yönetimi
│   ├── App.jsx                     # Ana uygulama bileşeni
│   ├── App.css                     # Uygulamaya özel stiller
│   ├── index.css                   # Global stiller
│   └── main.jsx                    # Uygulama giriş noktası
├── eslint.config.js                # ESLint konfigürasyonu
├── tailwind.config.js              # Tailwind CSS konfigürasyonu
├── postcss.config.js               # PostCSS konfigürasyonu
├── vite.config.js                  # Vite konfigürasyonu
└── package.json                    # Proje bağımlılıkları ve scripts
```

## 🔧 Modüller

### 📊 Dashboard (`Dashboard.jsx`)
Ana kontrol merkezi. Tüm vakaları listeler, istatistikler gösterir ve hızlı erişim sağlar.

**İşlevler:**
- Vaka listesi görüntüleme
- Vaka durumuna göre filtreleme
- Yeni vaka oluşturma
- Vaka seçme

### 📄 Vaka Detayı (`CaseDetail.jsx`)
Seçilen vakanın tüm bilgilerini gösterir ve düzenlemeyi sağlar.

**İşlevler:**
- Vaka temel bilgilerini görüntüleme
- Vaka bilgilerini güncelleme
- Tüm modüllere hızlı erişim
- Vaka silme

### 🔍 Kanıt Modülü (`EvidenceModule.jsx`)
Delilleri organize etme ve yönetme.

**İşlevler:**
- Kanıt ekleme
- Kanıt kategorilendirme
- Kanıt arama ve filtreleme
- Kanıt detaylarını görüntüleme

### 📅 Zaman Çizelgesi (`TimelineModule.jsx`)
Olayları kronolojik sırada görselleştirme.

**İşlevler:**
- Zaman çizelgesi oluşturma
- Olayları tarih sırasına göre gösterme
- Olay detaylarını görüntüleme
- İnteraktif zaman çizelgesi

### 👥 Tanık Modülü (`WitnessModule.jsx`)
Tanık bilgilerini kayıt etme ve yönetme.

**İşlevler:**
- Tanık ekleme
- Tanık bilgilerini düzenleme
- Tanık sorguları kayıt etme
- Tanık listesi

### 🔗 Bağlantılar (`ConnectionsModule.jsx`)
Kişiler, yerler ve olaylar arasındaki ilişkileri gösterme.

**İşlevler:**
- Bağlantı haritası oluşturma
- İlişkileri görselleştirme
- Bağlantı analizi
- Ağ grafiği

### 🗺️ Harita Modülü (`MapModule.jsx`)
Coğrafi lokasyonları gösterme.

**İşlevler:**
- Olay yerlerini işaretleme
- Önemli konumları gösterme
- Rota planlama
- Harita filtreleme

### 📊 Raporlama (`ReportsModule.jsx`)
Profesyonel PDF raporlar oluşturma.

**İşlevler:**
- Vaka özeti raporu
- Kanıt raporu
- Tam vaka raporu
- PDF indirme

## 🌍 API ve Context

### CaseContext (`CaseContext.jsx`)

Global durum yönetimi için React Context API'si kullanılır.

**State Değişkenleri:**
```javascript
- cases: Case[] - Tüm vakaların listesi
- selectedCase: Case | null - Seçilen vaka
```

**İşlevler:**

#### `useCases()`
Context'e erişmek için custom hook.

```javascript
const { cases, selectedCase, createCase, updateCase, deleteCase } = useCases();
```

#### `createCase(caseData)`
Yeni vaka oluşturur.

```javascript
const newCase = createCase({
  title: 'Yeni Vaka',
  description: 'Vaka açıklaması'
});
```

#### `updateCase(updatedCase)`
Mevcut vaka bilgilerini günceller.

```javascript
updateCase({
  ...selectedCase,
  status: 'Kapalı'
});
```

#### `deleteCase(caseId)`
Vaka siler.

```javascript
deleteCase(caseId);
```

### Vaka Yapısı

```javascript
{
  id: string,              // Benzersiz vaka kimliği
  caseNumber: string,      // Vaka numarası (VK-2026-001 formatında)
  title: string,           // Vaka başlığı
  description: string,     // Vaka açıklaması
  date: string,            // Vaka oluşturma tarihi
  status: string,          // Vaka durumu (Aktif, Kapalı, vb.)
  evidence: Evidence[],    // Delillerin listesi
  timeline: Event[],       // Olayların zaman çizelgesi
  witnesses: Witness[],    // Tanıkların listesi
  reports: Report[]        // Raporların listesi
}
```

## 💻 Geliştirme

### React Bileşen Yapısı

Her bileşen fonksiyonel bileşen olarak yazılmıştır ve React Hooks kullanır:

```javascript
import React, { useState } from 'react';
import { useCases } from '../context/CaseContext';

export default function ComponentName() {
  const { cases, selectedCase } = useCases();
  const [state, setState] = useState('');

  return (
    <div>
      {/* JSX content */}
    </div>
  );
}
```

### Styling

Tailwind CSS utility sınıfları kullanılır:

```jsx
<div className="bg-gray-100 p-4 rounded-lg shadow-md">
  <h1 className="text-2xl font-bold text-gray-800">Başlık</h1>
</div>
```

### State Yönetimi

Global state için CaseContext kullanılır:

```javascript
import { useCases } from '../context/CaseContext';

function MyComponent() {
  const { cases, createCase } = useCases();
  // ...
}
```

### Linting

Kodunuzu lint'lemek için:

```bash
npm run lint
```

ESLint kuralları `eslint.config.js` dosyasında tanımlanmıştır.

## 🏗️ Build ve Deployment

### Üretim Build'i Oluşturma

```bash
npm run build
```

Build dosyaları `dist/` klasöründe oluşturulacaktır.

### Build'i Önizleme

```bash
npm run preview
```

Optimized build'i `http://localhost:4173` adresinde önizleyebilirsiniz.

### Deployment

Built dosyaları herhangi bir statik hosting servisi (Netlify, Vercel, GitHub Pages vb.) üzerinde deploy edilebilir:

```bash
# dist/ klasörünü yükleyin
```

## 🤝 Katkıda Bulunma

Katkılara açığız! Lütfen aşağıdaki adımları izleyin:

1. Fork edin
2. Özellik branşı oluşturun (`git checkout -b feature/AmazingFeature`)
3. Değişiklikleri commit edin (`git commit -m 'Add some AmazingFeature'`)
4. Branşa push edin (`git push origin feature/AmazingFeature`)
5. Pull Request oluşturun

## 📝 Lisans

Bu proje MIT Lisansı altında lisanslanmıştır. Daha fazla bilgi için `LICENSE` dosyasına bakın.

## 📧 İletişim

Sorular veya öneriler için e.cankat.sumer@gmail.com adresi ile iletişime geçin.

---

**Son Güncelleme**: 2026
**Versiyon**: 0.0.0
