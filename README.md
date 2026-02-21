# 🏦 Çek Takip Sistemi  

**Çek Takip Sistemi**, çek işlemlerini yönetmek için geliştirilen **ASP.NET Core MVC** tabanlı bir uygulamadır.  
Bu sistem, finansal işlemleri kolaylaştırmak ve kullanıcıların çekleri düzenli bir şekilde takip etmelerini sağlamak için geliştirilmiştir.  

---

## 🚀 Özellikler  

✅ **Çek Yönetimi** – Yeni çek ekleme, düzenleme ve silme işlemleri  
✅ **Gelişmiş Filtreleme** – Şehir, tutar, para birimi gibi kriterlere göre filtreleme  
✅ **Arşiv Yönetimi** – Çekleri **arşive ekleme** veya **arşivden çıkarma**  
✅ **Seçilen Çekleri Yazdırma** – Kullanıcıların belirlediği çekleri tek tıklamayla yazdırma  
✅ **Excel Aktarımı** – Çek listesini **Excel formatında dışa aktarma ve içe aktarma**  
✅ **Çoklu Para Birimi Desteği** – TL, USD, EUR gibi farklı para birimleriyle çalışma  
✅ **Veri Doğrulama** – Kullanıcıların geçerli bilgiler girdiğini kontrol eden formlar  

---

## 📸 Proje Yapısı

### 📌 Çek Listesi  
Çeklerinizi listeleyebilir, filtreleyebilir ve düzenleyebilirsiniz.  

### ✍️ Yeni Çek Oluştur  
Kullanıcılar, yeni çek kayıtlarını ekleyerek işlemlerini yönetebilirler.  

### 🔧 Çek Düzenle  
Mevcut çeklerin bilgilerini güncelleyebilirsiniz.  

---

# PDF Oluşturma ve Çek Basma Modülü

Bu modül, finansal süreçlerde kullanılan **çek** bilgilerini (VKN, şehir, tarih, tutar, gönderen adı vb.) **PDF formatında** oluşturmak için yazılmıştır.  
[jsPDF](https://github.com/parallax/jsPDF) kütüphanesini kullanarak özel boyutlarda PDF dokümanı oluşturur, tutar biçimlendirme ve metin yerleşimi gibi özellikler sunar.

---

## printerEdit.js

### 📌 Sayfa Açıklaması

Bu proje, **JavaScript** ve **jsPDF** kütüphanesini kullanarak çek (cheque) formatında bir PDF belgesi oluşturan bir modüldür. Çek üzerindeki bilgileri doğru konumlara yerleştirmek için özel ayarlamalar içerir. PDF çıktısı, çek formatına uygun olarak dinamik alanlar ve özel font ayarlarıyla oluşturulur.

---

### 🚀 Sayfa Özellikleri

- ✅ **PDF Dokümanı Oluşturma** → `jsPDF` ile özel ölçülerde (200mm x 75mm) PDF çek formatı oluşturur.
- ✅ **Dinamik Alanlar** → Çek üzerindeki **VKN, şehir, tarih, tutar, gönderen adı** gibi bilgileri belirtilen koordinatlara yazdırır.
- ✅ **Tarih Formatlama** → `dd/mm/yyyy` veya `dd-mm-yyyy` formatındaki tarihleri biçimlendirerek çeke uygun hale getirir.
- ✅ **Miktar Formatlama** → Sayıyı **binlik ayırıcılar (.) ve ondalık virgüller (,)** ile düzgün şekilde yazdırır.
- ✅ **Metin Boyutu Otomatik Ayarlama** → Uzun metinlerde yazıyı **küçültme mekanizması** ile sığdırır.
- ✅ **Uyarı Mekanizması** → Hatalı tarih formatı algılandığında konsolda uyarı verir.
- ✅ **Manuel Biçimlendirme** → İlgili alanların koordinatları ve font büyüklüğü gerektiğinde değiştirilebilir.

---

### Manuel Biçimlendirme 

- **function createPdfDoc()** → Bu fonksiyon ile PDF belgesi oluşturabilir boyutunu ayarlayabilir ve kaydedebilirsiniz.
- **getHeaderConfig()** → Vergi Kimlik Numarası, Şehir, Tarih konumlarını ayarlayabilirsiniz.
- **getDetailsConfig()** → Tutar, Satıcı Ünvanı, Tuarın Yazı ile Tam Kısım ve Kuruş Kısmını ayarlayabilirsiniz.

----

### **Miktar Formatlama** 
- **formatAmount(amount)** → Sayıyı **binlik ayırıcılar (.) ve ondalık virgüller (,)** ile düzgün şekilde yazdırır.

----

### **Metin Boyutu Otomatik Ayarlama** 
- **renderCheck(doc, config)** → Uzun metinlerde yazıyı **küçültme mekanizması** ile sığdırır.
