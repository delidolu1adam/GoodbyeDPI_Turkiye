GoodbyeDPI Türkiye — Derin Paket İncelemesi Atlatma Aracı
=========================
Bu proje Türkiye'de kalıcı olarak engellenmiş **Discord** ve bazı durumlarda engellenen **Instagram**, **Youtube** vb. web sitesi ve uygulamalara VPN kullanmadan ve İnternet hızında bir değişiklik olmadan giriş yapmanızı sağlamak için GoodByeDPI'ın orjinal reposundan çatallanmış ve düzenlenmiş bir sürümüdür.

Daha fazla bilgi edinmek isterseniz indirdiğiniz **GoodBye DPI Türkiye v0.2.3rc3/documents/turkish** klasör içeriğindeki dosyalara göz atın.

Bu uygulama ve yazılım dosyaları, birçok İnternet Servis Sağlayıcısında bulunan ve belirli web sitelerine erişimi engelleyen **Derin Paket İnceleme Sistemleri**ni atlatmak için tasarlanmıştır.

Optik ayırıcı veya port yansıtma (**Pasif DPI**) kullanılarak bağlanan ve herhangi bir veriyi engellemeyen ancak istenen hedeften daha hızlı yanıt veren DPI'ları ve sırayla bağlanan **Aktif DPI**'ları işler.

> [!CAUTION]
> **Windows 7, 8, 8.1, 10 ve 11** işletim sistemlerinde, komut dosyalarının **Yönetici** olarak çalıştırılması gerekir.

Virüs, Veri Sızıntısı ve Bitcoin Madenciliği
=========================
Yazılım açık kaynak kodlu olduğundan tüm kodları inceleyebilirsiniz. WinDivert.dll ve WinDivert64.sys dosyaları fonksiyonlarından dolayı bazı antivirüs programlarında virüs olarak algılanabilir.

Ancak endişe etmenizi gerektirecek bir durum yok. Bu DLL ve SYS dosyaları da açık kaynak kodludur ve istendiğinde [buraya](https://github.com/basil00/WinDivert) tıklayarak inceleyebilirsiniz. Yazılımı kullanmak ya da kullanmamak tamamen sizin kendi insiyatifinizdedir.

Bu dosya da virüs var, bilgilerim çalındı vb. yalan yanlış ithamlarda bulunan kişilere kulak asmayın. Dilerseniz indirmeden önce dosyanın indirme bağlantısını kullanarak [buradan](https://www.virustotal.com/gui/home/upload) veya dosyayı indirdikten sonra dosyayı karşıya yükleyerek [buradan](https://www.virustotal.com/gui/home/url) virüs taraması yapabilirsiniz.

> [!NOTE]
> Kodların ne işe yaradığını ve hangi amaçla yazıldığını öğrenmek için kod bilgisine sahip olmanıza da gerek yok [buraya](https://chatgpt.com/) tıklayın ardından **Bu kodlarda virüs var mı? Hangi amaçla yazılmış? Ne işe yarıyor? Bilgilerim çalınır mı? Bitcoin madenciği yapıyor mu?** sorununu yazdıktan sonra **SHIFT + ENTER** tuşlarına basarak 2 satır aşağı inin ve merak ettiğiniz kodu da yapıştırıp gönderin. :)

Kullanım Yöntemi #1 : Elle Başlat
=========================

Bu yöntemi kullanırsanız, bilgisayarınızı her yeniden başlattığınızda istediğiniz herhangi bir komut dosyasını Yönetici olarak elle çalıştırmak zorundasınız. **Türkiye** için en hızlı ve en güvenili olanları `01, 02, 03, 04, 05, 06 ve 07` olarak sıraladım.

* **01 - CloudFlare DNS Yönlendirmeli.cmd** komut dosyasına sağ tıklayın ve **Yönetici Olarak** çalıştırın.
* Açılan pencereyi kapatmadan, istediğiniz uygulamaya veya web sitesine giriş yapabilirsiniz. Hepsi bu kadar!

> [!NOTE]
Bu komut dosyaları, GoodbyeDPI'ı önerilen modda başlatır ve çalıştırdığınız komut dosyasına göre DNS çözücü yönlendirmesini **CloudFlare, Google, Quad9, OpenDNS, AdGuard, Yandex ve Comodo** adreslerine (DNS zehirlenmesini engellemek için) standart olmayan bir port üzerinden gerçekleştirir. Eğer burada anlatıldığı gibi sorunsuz çalışıyorsa, olduğu gibi kullanmaya devam edebilir ya da diğer DNS hizmet sağlayıcıları için oluşturulmuş yapılandırma dosyalarını deneyebilir veya özelleştirebilirsiniz.

Kullanım Yöntemi #2 : Otomatik Olarak Başlat
=========================
Bu yöntemi kullanırsanız, bilgisayarınızı her yeniden başlattığınızda istediğiniz komut dosyasını **Başlangıç Programlarına** ekleyerek otomatik olarak başlatır ve ekstra birşey yapmanıza gerek kalmaz.

* Öncelikle buradaki kullanıcı adını düzenleyin **C:\Users\KULLANICI-ADINIZ\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup**
* Herhangi bir klasör adres çubuğuna düzenlemiş olduğunuz adresi yapıştırın ve ilgili klasörü açın.
* Daha sonra **01 - CloudFlare DNS Yönlendirmeli.cmd** komut dosyasına sağ tıklayın > Daha fazla seçenek göster > Kısayol oluştur
* Oluşturmuş olduğunuz **01 - CloudFlare DNS Yönlendirmeli.cmd - Kısayol** komut dosyasının kısayoluna sağ tıklayıp **kesin** (CTRL + X)
* **C:\Users\KULLANICI-ADINIZ\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup** klasörünün içinde boş bir yere sağ tıklayıp **yapıştırın** (CTRL + V)
* Şimdi herşeyi kapatıp bilgisayarınızı yeniden başlatın, görmüş olduğunuz gibi elle açmanız gereken pencere windows ile otomatik olarak açılıyor.
* Açılan pencereyi kapatmadan, istediğiniz uygulamaya veya web sitesine giriş yapabilirsiniz. Hepsi bu kadar!

Kullanım Yöntemi #3 : Windows Hizmeti Olarak Başlat
=========================
Bu yöntemi kullanırsanız, bilgisayarı her yeniden başlattığınızda GoodbyeDPI de bir Windows Hizmeti olarak başlatılır ve ekstra birşey yapmanıza gerek kalmaz.

- İndirmiş olduğunuz **GoodBye DPI Türkiye v0.2.3rc3** klasörününü açın.
- `11 - Windows Hizmeti Olarak Kur - DNS Yönlendirmeli v1.cmd`, komut dosyasına sağ tıklayın ve yönetici olarak çalıştırın.
- Açılan komut penceresinde herhangi bir tuşa basın.
- Eğer bu sizin için çalıştıysa olduğu gibi kullanabilirsiniz.
- Eğer çalışmazsa diğer alternatif olarak hazırladığım `12, 13, 14 ve 15` numaralı `v2.cmd`, `v3.cmd`, `v4.cmd`, ve `v5.cmd` komut dosyalarını sırayla deneyebilirsiniz.

> [!WARNING]
> Diğer `12, 13, 14 ve 15` numaralı `v2.cmd`, `v3.cmd`, `v4.cmd`, ve `v5.cmd` komut dosyalarını çalıştırmadan önce **18 - Hizmetleri Durdur ve Kaldır.cmd** komut dosyası ile herşeyi kaldırmayı ve temizlemeyi unutmayın.

Bilinen Sorunlar
=========================
* Eski Windows 7 kurulumlarında, SHA256 dijital imzalarına yönelik desteğin olmaması nedeniyle WinDivert sürücüsünü yükleyemiyor. KB3033929 [x86](https://www.microsoft.com/en-us/download/details.aspx?id=46078)/[x64](https://www.microsoft.com/en-us/download/details.aspx?id=46148) güncelleme paketini yükleyin veya daha iyi seçenek olan Windows Güncelleme'yi kullanarak tüm sisteminizi en yeni sürüme güncelleyin.
* Intel/Qualcomm Killer ağ kartları: Killer Control Center'daki Advanced Stream Detect, GoodbyeDPI ile uyumlu değil, [devre dışı bırakın](https://github.com/ValdikSS/GoodbyeDPI/issues/541#issuecomment-2296038239).
* QUIK ticaret yazılımı [GoodbyeDPI ile çakışabilir](https://github.com/ValdikSS/GoodbyeDPI/issues/677#issuecomment-2390595606). Çözüm için önce QUIK'i daha sonra GoodbyeDPI'ı başlatın.
* ~~Bazı SSL/TLS yığınları parçalanmış ClientHello paketlerini işleyemiyor ve HTTPS web siteleri açılmıyor. Hata: [#4](https://github.com/ValdikSS/GoodbyeDPI/issues/4), [#64](https://github.com/ValdikSS/GoodbyeDPI/issues/64).~~ Parçalanma sorunları v0.1.7'de düzeltildi.
* ~~ESET Antivirus, WinDivert sürücüsüyle uyumsuzdur [#91](https://github.com/ValdikSS/GoodbyeDPI/issues/91). Bu büyük ihtimalle WinDivert değil, antivirüs hatasıdır.~~

Bilinen Sorunlar
=========================
> [!IMPORTANT]
Bu uygulama ve yazılım dosyalarının kullanımı sonucunda doğabilecek her türlü yasal sorumluluk, kullanıcıların kendi sorumluluğundadır. Uygulama ve yazılım dosyaları, açık kaynak kodludur ve yalnızca araştırma, eğitim, bilgi paylaşımı ve kodlama eğitimi amacıyla geliştirilmiştir. Bu şartlar altında kullanılıp, kullanılmaması tamamen kullanıcıların kendi insiyatifine bırakılmıştır. 

Özel Teşekkürler
=========================
[Goodbye DPI](https://github.com/ValdikSS/GoodbyeDPI) geliştiricisi **@ValdikSS**'e teşekkürler.
[WinDivert](https://github.com/basil00/WinDivert) geliştiricisi **@basil00**'a teşekkürler.
[BlockCheck](https://github.com/ValdikSS/blockcheck)'e katkıda bulunan herkese teşekkürler.
