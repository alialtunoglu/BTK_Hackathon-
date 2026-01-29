# BTK Hackathon 2024 - Yapay Zeka Destekli Matematik Çözücü

## 📋 Proje Özeti

Bu proje, **BTK Hackathon 2024** için geliştirilmiş, Gemini yapay zeka destekli bir matematik problemi çözücü web uygulamasıdır. Uygulama, kullanıcıların matematik problemlerini **metin**, **dosya**, **ses kaydı** veya **fotoğraf** yoluyla girip anında çözüm alabildikleri, eğitim odaklı bir platformdur.

### 🎯 Temel Özellikler
- ✍️ **Çoklu Girdi Desteği**: Metin, PDF, ses kaydı ve fotoğraf ile problem girişi
- 🤖 **Gemini AI Entegrasyonu**: Google Gemini API ile güçlendirilmiş çözüm motoru
- 📚 **Adım Adım Açıklama**: Her problemin detaylı, eğitici çözüm adımları
- 🎥 **Video ve Doküman Önerileri**: Konu ile ilgili YouTube videoları ve öğrenme kaynakları
- 📱 **Responsive Tasarım**: Mobil, tablet ve masaüstü uyumlu arayüz
- 🔊 **OCR ve Ses Tanıma**: EasyOCR ve Google Speech Recognition ile görüntü ve ses işleme

### 🛠️ Teknoloji Stack
- **Backend**: Flask (Python)
- **AI/ML**: Google Gemini API, EasyOCR, SpeechRecognition
- **Frontend**: HTML5, CSS3, JavaScript
- **Görüntü İşleme**: OpenCV, Pillow
- **Diğer**: Markdown, NumPy

### 👥 Takım ve Geliştirme Süreci
3 kişilik bir ekip tarafından Git versiyon kontrolü kullanılarak işbirlikçi bir şekilde geliştirilmiştir.

### 🚀 Kurulum ve Çalıştırma
```bash
# 1. Sanal ortam oluştur (önerilen)
python -m venv venv

# 2. Sanal ortamı aktifleştir
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate

# 3. Bağımlılıkları yükle
pip install -r requirements.txt

# 4. Google Gemini API anahtarını ayarla
# app.py ve gemini_question.py dosyalarındaki API_KEY değerini kendi Gemini API anahtarınızla değiştirin

# 5. Uygulamayı çalıştır
python app.py
```

**Not:** Uygulama için Google Gemini API anahtarı gereklidir. [Google AI Studio](https://makersuite.google.com/app/apikey) üzerinden ücretsiz API anahtarı alabilirsiniz.

---

## 📖 English Summary

This is an **AI-powered math problem solver** web application developed for **BTK Hackathon 2024**. The application uses **Google's Gemini AI** to help users solve math problems through multiple input methods: text, file upload, voice recording, or photo capture. It provides step-by-step solutions with explanations, related educational videos, and learning resources.

**Key Features:**
- Multi-modal input support (text, file, voice, photo)
- Powered by Google Gemini API
- Step-by-step explanations
- Educational video and document recommendations
- Responsive design for all devices
- OCR and speech recognition capabilities

**Tech Stack:** Flask, Google Gemini API, EasyOCR, SpeechRecognition, OpenCV

**Installation:**
```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Set up Google Gemini API key in app.py and gemini_question.py

# Run the application
python app.py
```

**Note:** You need a Google Gemini API key to run this application. Get your free API key at [Google AI Studio](https://makersuite.google.com/app/apikey).

---

## 📝 Detaylı Dokümantasyon

**1. Giriş:**

`   `- Hackathon 2024, Türkiye'de yazılım geliştirmeye ve yapay zekâ alanına ilgi duyan herkese teorik bilgilerini pratikte uygulama imkânı sunan bir etkinlik olarak tasarlanmıştır. Bu hackathonun amacı, katılımcıların veri bilimi ve yapay zekâ konusundaki bilgilerini gerçek dünyadaki problemlere uygulayarak deneyim kazanmalarını sağlamaktır. Bu doğrultuda, biz de yarışmanın şartlarına uygun olarak Gemini destekli bir uygulama geliştirdik. Uygulamamız, yapay zekâ kullanarak belirli bir problemi çözmek için veri bilimi becerilerimizi ortaya koymamız açısından bize önemli bir pratik alan sundu.

`   `- Geliştirdiğimiz uygulamanın temel amacı, kullanıcıların matematik problemlerini çözmelerine yardımcı olmaktır. Bu uygulama, hem kullanıcıların yazılı olarak girdiği hem de dosya yoluyla yükledikleri matematiksel soruları analiz etmekte ve çözmektedir. Bu süreçte, problemleri çözmek için Gemini yapay zekâ teknolojisinden faydalanıyoruz. Gemini, problem çözme sürecinde yapay zekâ tabanlı analiz ve işlem yapma yeteneklerini kullanarak kullanıcılara doğru ve detaylı çözümler sunuyor. Böylece uygulamamız, özellikle matematik problemleriyle uğraşan öğrenciler ve profesyoneller için etkin bir çözüm platformu sağlıyor.

**2. Ürün Tanımı:**

`   `- Uygulamamız, kullanıcıların matematik problemlerini çözmelerine yardımcı olmak için çeşitli özellikler ve işlevler sunmaktadır. Bu özellikler, kullanıcının matematiksel soruları farklı yollarla uygulamaya yüklemesini ve çözümleri detaylı olarak anlamasını sağlamaktadır:

![Aspose Words d5b6856e-cb97-4cfe-bc0e-68bc693bca15 001](https://github.com/user-attachments/assets/daf004b0-37f7-4711-8968-5257068cc57b)


`     `- **Girdi Seçenekleri**: Uygulama, kullanıcılara esneklik sağlayarak matematik problemlerini dört farklı yolla yükleme imkânı tanır:

`       `- **Metin Girişi**: Kullanıcılar, problemlerini doğrudan metin olarak yazabilir.

`       `- Dosya Yükleme: Kullanıcılar, PDF veya metin dosyaları yoluyla birden fazla problemi toplu olarak yükleyebilir.

`       `- **Sesli Giriş:** Kullanıcılar, matematik problemlerini sesli olarak söyleyebilir ve uygulama bu sesi işleyerek problemi algılar.

`       `- **Fotoğraf Çekme:** Kullanıcılar, problem içeren bir fotoğraf çekerek uygulamaya yükleyebilir. Bu özellik, özellikle el yazısıyla yazılmış problemleri kolayca uygulamaya eklemek isteyenler için idealdir.

`       `Bu farklı girdi seçenekleri sayesinde kullanıcılar, uygulamayı kendi tercih ettikleri yöntemle kullanabilmekte ve daha esnek bir deneyim yaşamaktadır.

`     `- **Gemini Desteği:** Uygulama, matematik problemlerini çözerken ileri düzey bir yapay zekâ olan Gemini API’sinden yararlanmaktadır. Gemini, karmaşık matematiksel işlemleri hızlı bir şekilde analiz ederek doğru ve güvenilir sonuçlar sunar. Bu sayede, uygulama yalnızca matematik problemlerini doğru çözmekle kalmaz, aynı zamanda hızlı bir şekilde sonuçlara ulaşarak kullanıcı deneyimini optimize eder.

`     `- **Çözüm Sunumu:** Uygulama, kullanıcıya yalnızca problemin çözümünü sunmakla yetinmez. Aynı zamanda, çözüme dair detaylı dokümanlar ve ilgili eğitim videolarını da gösterir. Bu videolar ve dokümanlar, kullanıcıların çözüm sürecini adım adım öğrenmelerine olanak tanır ve matematiksel kavramları daha iyi anlamalarına yardımcı olur. Bu özellik, özellikle öğrenme sürecinde olan bireyler için oldukça faydalıdır.

`     `- **Açıklamalı Çözüm:** Uygulama, her problemi çözüm adımlarıyla birlikte sunar ve kullanıcıya ayrıntılı bir açıklama sağlar. Bu özellik, kullanıcıların yalnızca çözümü görmekle kalmayıp, çözüm sürecini de anlamalarını sağlar. Adım adım açıklamalarla desteklenen bu çözüm sunumu, öğrenciler ve matematik öğrenmeye çalışan kullanıcılar için eğitim odaklı bir deneyim sunar ve problem çözme becerilerini geliştirmelerine yardımcı olur. 

`   `Bu özellikler sayesinde uygulamamız, matematik problemlerini çözmek isteyen kullanıcılara kapsamlı bir çözüm platformu sağlamaktadır.

![Aspose Words d5b6856e-cb97-4cfe-bc0e-68bc693bca15 002](https://github.com/user-attachments/assets/3b825fe7-f9e8-4c5c-8568-8e4a6e99f67c)


**3. Teknik Yapı:**

`   `- Projemizin dosya yapısını dosya gezgininin ekran görüntüsünden faydalanarak detaylı şekilde açıklayalım. Proje, backend, frontend, ve API entegrasyonunun yanı sıra kullanıcı arayüzü gibi temel bileşenleri içermektedir:

`     `**- app.py:** Projenin backend kısmını yöneten ana dosyadır. Bu dosya, Gemini API’si ile iletişimi sağlamak ve matematik problemlerinin çözüm sürecini yönetmek için gerekli olan tüm API çağrılarını içerir. Kullanıcı tarafından gelen girdiler bu dosyada işlenir ve ilgili API'ye gönderilerek çözüm alınır. Aynı zamanda, çözüm sonucu burada işlenerek frontend’e aktarılır.

`     `**- html:** Uygulamanın web sayfalarındaki elementlerin yer aldığı dizindir. Bu dizin, kullanıcı arayüzünün temel yapısını oluşturur ve kullanıcıların girdi almasını, sonuçları görmesini sağlayan sayfa bileşenlerini içerir. Sayfa düzeni, form yapıları, ve çözüm gösterim bölümleri gibi temel HTML elementleri burada bulunur.

`     `**- script.js:** Uygulamanın frontend tarafında etkileşimli işlemleri gerçekleştiren JavaScript dosyasıdır. Bu dosya, kullanıcıdan girdi almayı, dosya yüklemeyi, fotoğraf çekmeyi, ve sesli giriş gibi işlemleri yönetir. Aynı zamanda, Gemini API’den gelen sonuçları alarak kullanıcıya gösterir. Bu sayede, kullanıcı etkileşimleri ve verilerin backend’e gönderilmesi gibi işlevler script.js tarafından yönetilir.

`     `**- css.js:** Uygulamanın stil düzenlemelerini içeren dosyadır. Butonlar, sayfa düzeni, renkler ve diğer görsel unsurlar gibi tüm stil ayarları bu dosyada yapılır. Kullanıcı arayüzünün daha çekici ve kullanımı kolay olmasını sağlar. Bu dosya sayesinde uygulamanın genel görünümü düzenlenir ve kullanıcı dostu bir deneyim sunulur.

`   `Bu dosya yapısı, projenin backend ve frontend arasında net bir ayrım yaparak düzenli bir yapı sağlar. Kullanıcı arayüzünden backend’e kadar her bir bileşen, belirli bir işlevi yerine getirir ve uygulamanın genel işleyişini destekler.



**4. Kullanıcı Deneyimi:**

`   `- Uygulama, kullanıcı dostu ve anlaşılır bir arayüze sahiptir. Hem öğrenciler hem de genel kullanıcılar düşünülerek tasarlanmıştır, böylece her yaş ve seviyeden kullanıcı, uygulamayı rahatlıkla kullanabilir. Arayüzde, matematik problemlerini çözmek için farklı giriş seçenekleri sunularak kullanıcıya esneklik sağlanmıştır. Girdi alımı ve sonuç görüntüleme işlemleri sade ve anlaşılır bir şekilde düzenlenmiştir.

`   `- Uygulama, ayrıca *responsive* bir tasarıma sahiptir; bu sayede telefon, tablet veya bilgisayar gibi farklı ekran boyutlarında uyumlu bir şekilde çalışır. Mobil cihazlarda kullanım için özel olarak optimize edilmiştir ve küçük ekranlarda da rahat bir deneyim sunmaktadır.

`   `**- İnteraktif Çözüm Adımları:** Uygulama, çözüm sürecini kullanıcıya adım adım interaktif bir şekilde sunar. Kullanıcılar, Gemini tarafından çözülen problemin adımlarını detaylıca inceleyebilir. Bu özellik sayesinde özellikle öğrenciler, sadece sonucu görmekle kalmaz, aynı zamanda çözüm sürecini de öğrenir. İlgili dokümanlar ve videolar çözümle birlikte sunularak, kullanıcıların problem çözme süreçlerinde derinlemesine bir anlayış kazanması sağlanır.

`   `- Bu sayede uygulama, öğrenmeyi destekleyen, kullanıcıya yol gösteren ve problemleri kolayca çözmelerine yardımcı olan bir yapıya sahiptir.

5. **Sonuç ve Hackathon Değerlendirmesi:**

   `   `**- Hackathon Süreci ve Zorluklar:** Hackathon 2024 boyunca bu projeyi geliştirirken bazı teknik ve organizasyonel zorluklarla karşılaştık. En büyük zorluklardan biri, Gemini API’si ile entegrasyon sağlarken yaşadığımız uyumluluk ve performans sorunlarıydı. Bu sorunları aşmak için API dokümantasyonunu dikkatlice inceledik ve kodda optimizasyonlar yaparak entegrasyonu sağladık. Ayrıca, uygulamanın farklı cihazlarda uyumlu çalışabilmesi için responsive tasarım konusunda detaylı çalışmalar yaptık. Projeyi 3 kişilik bir ekip olarak yürüttük ve görev dağılımını yaparak planlı bir çalışma gerçekleştirdik. Git versiyon kontrol sistemini kullanarak sürekli etkileşim halinde çalıştık; böylece her bir ekip üyesi projenin belirli bir alanına odaklandı ve projenin farklı bileşenleri üzerinde paralel ilerlememizi sağladı.

   `   `**- Sonuç:** Bu uygulama, öğrenci ve profesyonel kullanıcılar için eğitim amaçlı büyük bir katkı sunmakta olup, yapay zekâ destekli pratik bir çözüm olarak öne çıkmaktadır. Matematik problemlerinin çözümünü hızlı, doğru ve anlaşılır bir şekilde sunarak, hem eğitim alanında hem de günlük hayatta kullanılabilecek bir araç haline gelmiştir.

   `   `**- Eğitimsel Katkı:** Uygulamanın sunduğu çözüm süreci ve ilgili kaynaklar sayesinde kullanıcılar, matematik problemlerini daha iyi anlayabilmektedir. Adım adım açıklamalı çözüm sunma, kullanıcıların sadece sonuca ulaşmasını değil, aynı zamanda çözüm sürecini kavramasını sağlamaktadır. Bu, özellikle öğrenciler için öğretici bir rehber görevi görmektedir. Hem çözümlerle ilgili dokümanlar hem de destekleyici videolar sayesinde, kullanıcılar matematik öğrenme sürecinde derinlemesine bilgi edinebilmekte ve problem çözme becerilerini geliştirebilmektedir.

   Hackathon 2024 gibi etkinlikler, Türkiye’de yazılım ve yapay zekâ alanında genç yazılımcılara teorik bilgilerini pratiğe dökme imkânı sunuyor. Bu yarışma sürecinde, gerçek dünya problemlerini çözme deneyimi kazanırken ekip çalışması ve proje yönetimi becerilerimizi de geliştirdik. Yapay zekâ destekli matematik çözücü uygulamamız, Hackathon’un sunduğu fırsatları değerlendirerek ortaya çıktı ve eğitim odaklı, kullanıcı dostu bir ürün geliştirmemizi sağladı.
