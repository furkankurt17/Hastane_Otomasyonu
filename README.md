# 🏥 Hastane Otomasyon Sistemi V2

<div align="center">
  <img src="https://img.shields.io/badge/C%23-.NET%204.7.2-239120?style=for-the-badge&logo=c-sharp&logoColor=white" alt="C# .NET 4.7.2">
  <img src="https://img.shields.io/badge/Windows%20Forms-Desktop%20App-0078D6?style=for-the-badge&logo=windows&logoColor=white" alt="Windows Forms">
  <img src="https://img.shields.io/badge/SQL%20Server-Database-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white" alt="SQL Server">
</div>

## 📋 İçindekiler
- [Hakkında](#hakkında)
- [Özellikler](#özellikler)
- [Teknolojiler](#teknolojiler)
- [Kurulum](#kurulum)
- [Kullanım](#kullanım)
- [Proje Yapısı](#proje-yapısı)
- [Ekran Görüntüleri](#ekran-görüntüleri)
- [Katkıda Bulunma](#katkıda-bulunma)
- [Lisans](#lisans)

## 🎯 Hakkında

Bu proje, hastaneler için geliştirilmiş kapsamlı bir otomasyon sistemidir. Sistem, hasta, doktor ve sekreter rolleri için farklı paneller sunarak hastane yönetimini dijitalleştirmeyi amaçlamaktadır.

### Ana Amaçlar
- ✅ Hasta kayıt ve yönetim süreçlerini kolaylaştırmak
- ✅ Doktor randevu ve hasta takip sistemini otomatikleştirmek
- ✅ Sekreter işlemlerini hızlandırmak
- ✅ Branş ve duyuru yönetimini merkezi hale getirmek

## ✨ Özellikler

### 👤 Hasta Modülü
- [x] Hasta kayıt sistemi
- [x] Hasta giriş paneli
- [x] Randevu alma sistemi
- [x] Randevu geçmişi görüntüleme
- [x] Duyuruları görüntüleme
- [x] Profil güncelleme

### 👨‍⚕️ Doktor Modülü
- [x] Doktor giriş paneli
- [x] Randevu listesi görüntüleme
- [x] Hasta bilgilerini görüntüleme
- [x] Duyuru oluşturma
- [x] Profil güncelleme
- [x] Hasta değerlendirme sistemi

### 📋 Sekreter Modülü
- [x] Sekreter giriş paneli
- [x] Randevu oluşturma ve yönetme
- [x] Randevu listesi görüntüleme
- [x] Hasta kayıt ve güncelleme
- [x] Doktor kayıt ve güncelleme
- [x] Branş yönetimi
- [x] Duyuru yönetimi

### 🔧 Sistem Özellikleri
- [x] Güvenli giriş sistemi
- [x] Rol bazlı erişim kontrolü
- [x] Veritabanı yedekleme desteği
- [x] Kullanıcı dostu arayüz

## 🛠️ Teknolojiler

| Teknoloji | Versiyon | Açıklama |
|-----------|----------|----------|
| **C#** | .NET Framework 4.7.2 | Programlama dili |
| **Windows Forms** | - | Kullanıcı arayüzü |
| **SQL Server** | - | Veritabanı |
| **ADO.NET** | - | Veritabanı erişimi |
| **Entity Framework** | - | ORM (opsiyonel) |

## 📦 Kurulum

### Gereksinimler
- Visual Studio 2017 veya üzeri
- .NET Framework 4.7.2 veya üzeri
- SQL Server 2014 veya üzeri
- Windows 7 veya üzeri

### Adım 1: Projeyi İndirin
```bash
git clone https://github.com/furkankurt17/Hastane_Otomasyonu.git
cd Hastane_Otomasyonu
```

### Adım 2: Veritabanını Oluşturun
1. SQL Server Management Studio'yu açın
2. Aşağıdaki komutu çalıştırarak veritabanını oluşturun:
```sql
CREATE DATABASE HastaneProje;
```

### Adım 3: Bağlantı Ayarlarını Yapılandırın
`sqlbaglanti.cs` dosyasını açın ve bağlantı string'ini kendi SQL Server ayarlarınıza göre düzenleyin:

```csharp
SqlConnection baglan = new SqlConnection("Data Source=SUNUCU_ADI\\SQLEXPRESS;Initial Catalog=HastaneProje;Integrated Security=True");
```

### Adım 4: Projeyi Derleyin
1. Visual Studio'da `Hastane_OtomasyonV2.sln` dosyasını açın
2. `Build > Build Solution` menüsünden projeyi derleyin
3. `Debug > Start Debugging` ile çalıştırın

## 🚀 Kullanım

### İlk Çalıştırma
1. Uygulamayı başlattığınızda ana giriş ekranı açılır
2. Hasta, Doktor veya Sekreter butonlarından birine tıklayın
3. İlgili giriş formuna kullanıcı adı ve şifrenizi girin

### Hasta İşlemleri
- Randevu almak için doktor seçin
- Randevu geçmişinizi görüntüleyin
- Duyuruları okuyun
- Profil bilgilerinizi güncelleyin

### Doktor İşlemleri
- Randevu listesini görüntüleyin
- Hastaları değerlendirin
- Duyuru oluşturun
- Profil bilgilerinizi güncelleyin

### Sekreter İşlemleri
- Yeni randevu oluşturun
- Hasta ve doktor kayıtlarını yönetin
- Branş ekleyin/düzenleyin
- Sistem duyuruları yayınlayın

## 📁 Proje Yapısı

```
Hastane_OtomasyonV2/
│
├── 📄 Form1.cs                    # CAPTCHA doğrulama formu
├── 📄 FrmGiris.cs                # Ana giriş ekranı
│
├── 👤 Hasta Modülü
│   ├── FrmHastaKayıt.cs          # Hasta kayıt formu
│   ├── FrmHastaGiris.cs          # Hasta giriş formu
│   ├── FrmHastaDetay.cs          # Hasta detay formu
│   ├── FrmHastaPanel.cs          # Hasta paneli
│   └── FrmHastaGuncelle.cs       # Hasta güncelleme formu
│
├── 👨‍⚕️ Doktor Modülü
│   ├── FrmDoktorGiris.cs         # Doktor giriş formu
│   ├── FrmDoktorDetay.cs         # Doktor detay formu
│   ├── FrmDoktorPanel.cs         # Doktor paneli
│   ├── FrmDoktorGuncelle.cs      # Doktor güncelleme formu
│   └── FrmDoktorDuyuru.cs        # Doktor duyuru formu
│
├── 📋 Sekreter Modülü
│   ├── FrmSekreterGiris.cs       # Sekreter giriş formu
│   ├── FrmSekreterDetay.cs       # Sekreter detay formu
│   └── FrmRandevuListe.cs        # Randevu listesi
│
├── 🔧 Sistem Modülleri
│   ├── FrmBransPanel.cs          # Branş yönetim paneli
│   ├── FrmDuyurular.cs           # Duyuru formu
│   ├── FrmDegerlendirme.cs       # Değerlendirme formu
│   └── sqlbaglanti.cs            # Veritabanı bağlantı sınıfı
│
├── ⚙️ Yapılandırma
│   ├── App.config                # Uygulama ayarları
│   ├── Program.cs                # Program giriş noktası
│   └── Properties/               # Proje özellikleri
│
└── 📸 Resimler/                  # Uygulama görselleri
    ├── gizligöz1.2.png
    └── göz1.2.png
```

## 🖼️ Ekran Görüntüleri

> 📸 Ekran görüntüleri eklenecek...

## 📝 Lisans

Bu proje eğitim amaçlı geliştirilmiştir. Ticari kullanım için lisans gereklidir.

## 👨‍💻 Geliştirici

**Celil Furkan KURT**
- GitHub: [@furkankurt17](https://github.com/furkankurt17)
- Proje Linki: [Hastane_Otomasyonu](https://github.com/furkankurt17/Hastane_Otomasyonu)

---

<div align="center">
  ⭐ Bu projeyi beğendiyseniz yıldız vermeyi unutmayın! ⭐
</div>
