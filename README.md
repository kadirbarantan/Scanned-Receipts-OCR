# UiPath Fiş & Fatura İşleme Otomasyonu

Bu proje, UiPath Studio kullanılarak geliştirilmiş bir RPA (Robotik Süreç Otomasyonu) iş akışıdır. Bot, bulut üzerindeki fatura/fiş belgelerini otomatik olarak indirir, OCR ile içindeki verileri okur ve hesaplanan sonuçları yerel makineye raporlar.

## Özellikler
* **Google Drive Entegrasyonu:** Google Drive klasöründe bulunan PDF formatındaki fişleri/faturaları otomatik olarak tespit eder ve bilgisayara indirir.
* **OCR ile Veri Çıkartma:** İndirilen PDF dosyaları, UiPath Document OCR API kullanılarak taranır ve içeriklerindeki metinler elde edilir.
* **Veri İşleme ve Hesaplama:** Belgelerden okunan satış tutarları işlenir ve kümülatif olarak toplam satış tutarı hesaplanır.
* **Dinamik Raporlama:** Elde edilen sonuçlar ve fiş ID'leri, her cihazda veya Orchestrator ortamında sorunsuz çalışabilmesi için dinamik dosya yolları kullanılarak `.txt` dosyasına (`Append Line`) yazdırılır.
* **Dosya Yönetimi ve Hata Yakalama:** İndirme işlemleri sırasında oluşabilecek sorunlar `Try Catch` bloğu ile yönetilir. Ayrıca işlem gören dosyalar başarıyla tamamlandıktan sonra başka bir klasöre taşınarak (`Move File`) düzen sağlanır.

## Kullanılan Teknolojiler
* UiPath Studio
* UiPath GSuite (Google Drive) Aktiviteleri
* UiPath Document OCR

## Kurulum ve Kullanım
1. Projeyi bilgisayarınıza klonlayın veya indirin.
2. `Main.xaml` dosyasını UiPath Studio ile açın.
3. Çalıştırmadan önce Google Drive erişimi için gerekli hesap/API izinlerinin tanımlı olduğundan emin olun. 
4. Gerekli bağımlılıklar (paketler) yüklendikten sonra projeyi başlatabilirsiniz.