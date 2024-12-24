GoodbyeDPI Türkiye — Derin Paket İncelemesi Atlatma Aracı
=========================
Bu proje Türkiye'de kalıcı olarak engellenmiş **Discord** ve bazı durumlarda engellenen **Instagram**, **Youtube** vb. web sitesi ve uygulamalara VPN kullanmadan ve İnternet hızında bir değişiklik olmadan giriş yapmanızı sağlamak için GoodByeDPI'ın orjinal reposundan çatallanmış ve düzenlenmiş bir sürümüdür.

Daha fazla bilgi edinmek isterseniz indirdiğiniz **GoodBye DPI Türkiye v0.2.3rc3/assets/documents** klasör içeriğindeki **_Turkish** etiketli dosyalara göz atın.

Bu yazılım, birçok İnternet Servis Sağlayıcısında bulunan ve belirli web sitelerine erişimi engelleyen **Derin Paket İnceleme Sistemleri**ni atlatmak için tasarlanmıştır.

Optik ayırıcı veya port yansıtma (**Pasif DPI**) kullanılarak bağlanan ve herhangi bir veriyi engellemeyen ancak istenen hedeften daha hızlı yanıt veren DPI'ları ve sırayla bağlanan **Aktif DPI**'ları işler.

> [!CAUTION]
> **Windows 7, 8, 8.1, 10 ve 11** işletim sistemlerinde, komut dosyalarının **Yönetici** olarak çalıştırılması gerekir.

Virüs, Veri Sızıntısı ve Bitcoin Madenciliği
=========================
Yazılım açık kaynak kodlu olduğundan tüm kodları inceleyebilirsiniz. WinDivert.dll ve WinDivert64.sys dosyaları fonksiyonlarından dolayı bazı antivirüs programlarında virüs olarak algılanabilir.

Ancak endişe etmenizi gerektirecek bir durum yok. Bu DLL ve SYS dosyaları da açık kaynak kodludur ve istendiğinde [buradan](https://github.com/basil00/WinDivert) inceleyebilirsiniz. Yazılımı kullanmak ya da kullanmamak tamamen sizin kendi insiyatifinizdedir.

Bu dosya da virüs var, bilgilerim çalındı vb. yalan yanlış ithamlarda bulunan kişilere kulak asmayın. Dilerseniz indirmeden önce dosyanın indirme bağlantısını kullanarak [buradan](https://www.virustotal.com/gui/home/upload) veya dosyayı indirdikten sonra dosyayı yükleyerek [buradan](https://www.virustotal.com/gui/home/url) virüs taraması yapabilirsiniz.

> [!NOTE]
> Kodların ne işe yaradığını ve hangi amaçla yazıldığını öğrenmek için kod bilgisine sahip olmanıza da gerek yok [buraya](https://chatgpt.com/) tıklayın ardından **Bu kodlarda virüs var mı? Hangi amaçla yazılmış? Ne işe yarıyor? Bilgilerim çalınır mı? Bitcoin madenciği yapıyor mu?** sorununu yazdıktan sonra **SHIFT + ENTER** tuşlarına basarak 2 satır aşağı inin ve merak ettiğiniz kodu da yapıştırıp gönderin. :)

Elle Başlatarak Kullanma
=========================

Bilgisayarı açtığınızda bu işlemi her zaman tekrarlamanız gerekir.

* **Türkiye** için **01 - CloudFlare DNS Yönlendirmeli.cmd** komut dosyasına sağ tıklayın ve **Yönetici Olarak** çalıştırın.

* **Türkiye** için **07 - Yandex DNS Yönlendirmeli.cmd** komut dosyasına sağ tıklayın ve **Yönetici Olarak** çalıştırın.

* **Diğer Ülkeler** için **01 - CloudFlare DNS Yönlendirmeli.cmd** komut dosyasına sağ tıklayın ve **Yönetici Olarak** çalıştırın.

> [!NOTE]
Bu komut dosyaları, GoodbyeDPI'ı önerilen modda başlatır ve çalıştırdığınız komut dosyasına göre DNS çözücü yönlendirmesini **CloudFlare, Google, Quad9, OpenDNS, AdGuard, Yandex ve Comodo** adreslerine (DNS zehirlenmesini engellemek için) standart olmayan bir port üzerinden gerçekleştirir. Eğer burada anlatıldığı gibi sorunsuz çalışıyorsa, olduğu gibi kullanmaya devam edebilir ya da diğer DNS hizmet sağlayıcıları için oluşturulmuş yapılandırma dosyalarını deneyebilir veya özelleştirebilirsiniz.

Komut Dosyasını Otomatik Olarak Başlatma
=========================
Her bilgisayarı açtığınızda bu dosyaları yönetici olarak çalıştırmak istemiyorsanız, iki farklı yöntem deneyebilirsiniz.

...

Windows Hizmeti Olarak Kurma
=========================
Bilgisayarı açtığınızda hizmetin otomatik olarak başlamasını istiyorsanız, aşağıdaki adımları sırasıyla uygulayabilirsiniz.

- İndirmiş olduğunuz **GoodBye DPI Türkiye v0.2.3rc3** klasörününü açın.
- `11 - Windows Hizmeti Olarak Kur - DNS Yönlendirmeli v1.cmd`, komut dosyasına sağ tıklayın ve yönetici olarak çalıştırın.
- Açılan komut penceresinde herhangi bir tuşa basın.
- Eğer bu sizin için çalıştıysa olduğu gibi kullanabilirsiniz.
- Eğer çalışmazsa diğer alternatif `12 - Windows Hizmeti Olarak Kur - DNS Yönlendirmeli v2.cmd`, `13 - Windows Hizmeti Olarak Kur - DNS Yönlendirmeli v3.cmd`, `14 - Windows Hizmeti Olarak Kur - DNS Yönlendirmeli v4.cmd`, `15 - Windows Hizmeti Olarak Kur - DNS Yönlendirmeli v5.cmd`, komut dosyalarını sırayla deneyebilirsiniz.

> [!WARNING]
> Diğer komut dosyalarını denemeden önce **18 - Hizmetleri Durdur ve Kaldır.cmd** komut dosyası ile herşeyi kaldırmayı ve temizlemeyi unutmayın.

Bilinen Sorunlar
=========================
* Eski Windows 7 kurulumlarında, SHA256 dijital imzalarına yönelik desteğin olmaması nedeniyle WinDivert sürücüsünü yükleyemiyor. KB3033929 [x86](https://www.microsoft.com/en-us/download/details.aspx?id=46078)/[x64](https://www.microsoft.com/en-us/download/details.aspx?id=46148) güncelleme paketini yükleyin veya daha iyi seçenek olan Windows Güncelleme'yi kullanarak tüm sisteminizi en yeni sürüme güncelleyin.
* Intel/Qualcomm Killer ağ kartları: Killer Control Center'daki Advanced Stream Detect, GoodbyeDPI ile uyumlu değil, [devre dışı bırakın](https://github.com/ValdikSS/GoodbyeDPI/issues/541#issuecomment-2296038239).
* QUIK ticaret yazılımı [GoodbyeDPI ile çakışabilir](https://github.com/ValdikSS/GoodbyeDPI/issues/677#issuecomment-2390595606). Çözüm için önce QUIK'i daha sonra GoodbyeDPI'ı başlatın.
* ~~Bazı SSL/TLS yığınları parçalanmış ClientHello paketlerini işleyemiyor ve HTTPS web siteleri açılmıyor. Hata: [#4](https://github.com/ValdikSS/GoodbyeDPI/issues/4), [#64](https://github.com/ValdikSS/GoodbyeDPI/issues/64).~~ Parçalanma sorunları v0.1.7'de düzeltildi.
* ~~ESET Antivirus, WinDivert sürücüsüyle uyumsuzdur [#91](https://github.com/ValdikSS/GoodbyeDPI/issues/91). Bu büyük ihtimalle WinDivert değil, antivirüs hatasıdır.~~
