🛡️ Kaspersky Antivirüs Programı Hakkında Önemli Duyuru
=========================
İnternette dolaşan haberlerin aksine; şu ana kadar Kaspersky ile Rus hükümeti arasında, doğrudan "GoodbyeDPI’yi engellemek amacıyla yapılmış özel bir anlaşma" olduğuna dair herhangi bir resmi, teknik ya da sızdırılmış kanıt bulunmamaktadır. Dolayısıyla ne sızdırılmış belgelerde ne de hükümet açıklamalarında GoodbyeDPI’ye özel bir anlaşma veya hedefleme söz konusu değildir.

Kaspersky'nin GoodbyeDPI’yi engellemesi, büyük ihtimalle genel ağ güvenliği politikalarının ve ürün özelliklerinin doğal bir sonucudur.
- HTTP/HTTPS trafiğini analiz eder.
- Paket yapısını bozan uygulamaları "şüpheli" olarak algılar.
- Man-in-the-Middle (MitM) saldırılarına karşı koruma sağlar.

Bu davranış, Rusya özelinde değil; Kaspersky’nin genel ürün tasarımı ile ilgilidir. Yaklaşık 20 yıldır Antivirüs programı kullanmıyorum, gerek de duymuyorum. Bu engelleme ürün ayarlarından ince/gelişmiş bir ayar yaparak bu düzeltilebilir mi emin değilim. Bunu Kaspersky kullanan kullanıcılar ile forumda tartışabilir, fikir alışverişinde bulunabilirsiniz. Şayet bu konuda başarısız olursanız, tek yapmanız gereken Kaspersky bilgisayarınızdan tamamen kaldırmak, zira devre dışı bıraksanız bile büyük olasılıkla GoodBye DPI'ı yine de engelleyecektir.

🇹🇷 GoodbyeDPI Türkiye — Derin Paket İncelemesi Atlatma Aracı
=========================
Bu proje Türkiye'de kalıcı olarak engellenmiş **Discord** ve bazı durumlarda engellenen **Instagram**, **Youtube** vb. web sitesi ve uygulamalara VPN kullanmadan ve İnternet hızında bir değişiklik olmadan giriş yapmanızı sağlamak için GoodByeDPI'ın orjinal deposundan çatallanmış ve düzenlenmiş bir sürümüdür.

Bu uygulama ve yazılım dosyaları, birçok İnternet Servis Sağlayıcısında bulunan ve belirli web sitelerine erişimi engelleyen **Derin Paket İnceleme Sistemleri**'ni atlatmak için tasarlanmıştır.

Optik ayırıcı veya port yansıtma (**Pasif DPI**) kullanılarak bağlanan ve herhangi bir veriyi engellemeyen ancak istenen hedeften daha hızlı yanıt veren DPI'ları ve sırayla bağlanan **Aktif DPI**'ları işler.

Daha fazla bilgi için **GoodBye DPI Türkiye v0.2.3rc3/documents/turkish** klasör içeriğindeki dosyalara göz atabilirsiniz veya [buraya](https://github.com/ValdikSS/GoodbyeDPI) tıklayrak projenin asıl sayfasında tüm detayları inceleyebilirsiniz.

> [!CAUTION]
> **Windows 7, 8, 8.1, 10 ve 11** işletim sistemlerinde, komut dosyalarının **Yönetici** olarak çalıştırılması gerekir.

🦠 Virüs, Veri Sızıntısı ve Bitcoin Madenciliği
=========================
Yazılım açık kaynak kodlu olduğundan tüm kodları inceleyebilirsiniz. WinDivert.dll ve WinDivert64.sys dosyaları fonksiyonlarından dolayı bazı antivirüs programlarında virüs olarak algılanabilir.

Ancak endişe etmenizi gerektirecek bir durum yok. Bu DLL ve SYS dosyaları da açık kaynak kodludur ve istendiğinde [buraya](https://github.com/basil00/WinDivert) tıklayarak inceleyebilirsiniz. Yazılımı kullanmak ya da kullanmamak tamamen sizin kendi insiyatifinizdedir.

Bu dosya da virüs var, bilgilerim çalındı vb. yalan yanlış ithamlarda bulunan kişilere kulak asmayın. Dilerseniz indirmeden önce dosyanın indirme bağlantısını kullanarak [buradan](https://www.virustotal.com/gui/home/upload) veya dosyayı indirdikten sonra dosyayı karşıya yükleyerek [buradan](https://www.virustotal.com/gui/home/url) virüs taraması yapabilirsiniz.

> [!NOTE]
> Kodların ne işe yaradığını ve hangi amaçla yazıldığını öğrenmek için kod bilgisine sahip olmanıza da gerek yok [buraya](https://chatgpt.com/) tıklayın ardından **Bu kodlarda virüs var mı? Hangi amaçla yazılmış? Ne işe yarıyor? Bilgilerim çalınır mı? Bitcoin madenciği yapıyor mu?** sorununu yazdıktan sonra **SHIFT + ENTER** tuşlarına basarak 2 satır aşağı inin ve merak ettiğiniz kodu da yapıştırıp gönderin. :)

👣 Kullanım Yöntemi #1 : Elle Başlat
=========================

Bu yöntemi kullanırsanız, bilgisayarınızı her yeniden başlattığınızda istediğiniz herhangi bir komut dosyasını Yönetici olarak elle çalıştırmak zorundasınız. **Türkiye** için en hızlı ve en güvenili olanları `01, 02, 03, 04, 05, 06 ve 07` olarak sıraladım.

* **01 - CloudFlare DNS Yönlendirmeli.cmd** komut dosyasına sağ tıklayın ve **Yönetici Olarak** çalıştırın.
* Açılan pencereyi kapatmadan, istediğiniz uygulamaya veya web sitesine giriş yapabilirsiniz. Hepsi bu kadar!

> [!NOTE]
Bu komut dosyaları, GoodbyeDPI'ı önerilen modda başlatır ve çalıştırdığınız komut dosyasına göre DNS çözücü yönlendirmesini **CloudFlare, Google, Quad9, OpenDNS, AdGuard, Yandex ve Comodo** adreslerine (DNS zehirlenmesini engellemek için) standart olmayan bir port üzerinden gerçekleştirir. Eğer burada anlatıldığı gibi sorunsuz çalışıyorsa, olduğu gibi kullanmaya devam edebilir ya da diğer DNS hizmet sağlayıcıları için oluşturulmuş yapılandırma dosyalarını deneyebilir veya özelleştirebilirsiniz.

👣 Kullanım Yöntemi #2 : Otomatik Olarak Başlat
=========================
Bu yöntemi kullanırsanız, bilgisayarınızı her yeniden başlattığınızda istediğiniz komut dosyasını **Başlangıç Programlarına** ekleyerek otomatik olarak başlatır ve ekstra birşey yapmanıza gerek kalmaz.

* Öncelikle buradaki kullanıcı adını düzenleyin **C:\Users\KULLANICI-ADINIZ\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup**
* Herhangi bir klasör adres çubuğuna düzenlemiş olduğunuz adresi yapıştırın ve ilgili klasörü açın.
* Daha sonra **01 - CloudFlare DNS Yönlendirmeli.cmd** komut dosyasına sağ tıklayın > Daha fazla seçenek göster > Kısayol oluştur
* Oluşturmuş olduğunuz **01 - CloudFlare DNS Yönlendirmeli.cmd - Kısayol** komut dosyasının kısayoluna sağ tıklayıp **kesin** (CTRL + X)
* **C:\Users\KULLANICI-ADINIZ\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup** klasörünün içinde boş bir yere sağ tıklayıp **yapıştırın** (CTRL + V)
* Şimdi herşeyi kapatıp bilgisayarınızı yeniden başlatın, görmüş olduğunuz gibi elle açmanız gereken pencere windows ile otomatik olarak açılıyor.
* Açılan pencereyi kapatmadan, istediğiniz uygulamaya veya web sitesine giriş yapabilirsiniz. Hepsi bu kadar!

> [!WARNING]
> Bu yöntemin çalışması için komut dosyalarına bir kaç kod eklemem gerekiyor - henüz eklemedim!

👣 Kullanım Yöntemi #3 : Windows Hizmeti Olarak Başlat
=========================
Bu yöntemi kullanırsanız, bilgisayarı her yeniden başlattığınızda GoodbyeDPI de bir Windows Hizmeti olarak başlatılır ve ekstra birşey yapmanıza gerek kalmaz.

- İndirmiş olduğunuz **GoodBye DPI Türkiye v0.2.3rc3** klasörününü açın.
- `11 - Windows Hizmeti Olarak Kur - DNS Yönlendirmeli v1.cmd`, komut dosyasına sağ tıklayın ve yönetici olarak çalıştırın.
- Açılan komut penceresinde herhangi bir tuşa basın.
- Eğer bu sizin için çalıştıysa olduğu gibi kullanabilirsiniz.
- Eğer çalışmazsa diğer alternatif olarak hazırladığım `12, 13, 14 ve 15` numaralı `v2.cmd`, `v3.cmd`, `v4.cmd`, ve `v5.cmd` komut dosyalarını sırayla deneyebilirsiniz.

> [!WARNING]
> Diğer `12, 13, 14 ve 15` numaralı `v2.cmd`, `v3.cmd`, `v4.cmd`, ve `v5.cmd` komut dosyalarını çalıştırmadan önce **18 - Hizmetleri Durdur ve Kaldır.cmd** komut dosyası ile herşeyi kaldırmayı ve temizlemeyi unutmayın.

♻️ ## Desteklenen Argümanlar
Programınızın sürümü hakkında ilgili bilgileri almak için başlangıçta -h (--help) komutunu kullanabilirsiniz.
=========================
```
Kullanımı: goodbyedpi.exe [OPTION...]
 -p          block passive DPI
 -q          block QUIC/HTTP3
 -r          replace Host with hoSt
 -s          remove space between host header and its value
 -m          mix Host header case (test.com -> tEsT.cOm)
 -f <value>  set HTTP fragmentation to value
 -k <value>  enable HTTP persistent (keep-alive) fragmentation and set it to value
 -n          do not wait for first segment ACK when -k is enabled
 -e <value>  set HTTPS fragmentation to value
 -a          additional space between Method and Request-URI (enables -s, may break sites)
 -w          try to find and parse HTTP traffic on all processed ports (not only on port 80)
 --port        <value>    additional TCP port to perform fragmentation on (and HTTP tricks with -w)
 --ip-id       <value>    handle additional IP ID (decimal, drop redirects and TCP RSTs with this ID).
                          This option can be supplied multiple times.
 --dns-addr    <value>    redirect UDP DNS requests to the supplied IP address (experimental)
 --dns-port    <value>    redirect UDP DNS requests to the supplied port (53 by default)
 --dnsv6-addr  <value>    redirect UDPv6 DNS requests to the supplied IPv6 address (experimental)
 --dnsv6-port  <value>    redirect UDPv6 DNS requests to the supplied port (53 by default)
 --dns-verb               print verbose DNS redirection messages
 --blacklist   <txtfile>  perform circumvention tricks only to host names and subdomains from
                          supplied text file (HTTP Host/TLS SNI).
                          This option can be supplied multiple times.
 --allow-no-sni           perform circumvention if TLS SNI can't be detected with --blacklist enabled.
 --frag-by-sni            if SNI is detected in TLS packet, fragment the packet right before SNI value.
 --set-ttl     <value>    activate Fake Request Mode and send it with supplied TTL value.
                          DANGEROUS! May break websites in unexpected ways. Use with care (or --blacklist).
 --auto-ttl    [a1-a2-m]  activate Fake Request Mode, automatically detect TTL and decrease
                          it based on a distance. If the distance is shorter than a2, TTL is decreased
                          by a2. If it's longer, (a1; a2) scale is used with the distance as a weight.
                          If the resulting TTL is more than m(ax), set it to m.
                          Default (if set): --auto-ttl 1-4-10. Also sets --min-ttl 3.
                          DANGEROUS! May break websites in unexpected ways. Use with care (or --blacklist).
 --min-ttl     <value>    minimum TTL distance (128/64 - TTL) for which to send Fake Request
                          in --set-ttl and --auto-ttl modes.
 --wrong-chksum           activate Fake Request Mode and send it with incorrect TCP checksum.
                          May not work in a VM or with some routers, but is safer than set-ttl.
 --wrong-seq              activate Fake Request Mode and send it with TCP SEQ/ACK in the past.
 --native-frag            fragment (split) the packets by sending them in smaller packets, without
                          shrinking the Window Size. Works faster (does not slow down the connection)
                          and better.
 --reverse-frag           fragment (split) the packets just as --native-frag, but send them in the
                          reversed order. Works with the websites which could not handle segmented
                          HTTPS TLS ClientHello (because they receive the TCP flow "combined").
 --fake-from-hex <value>  Load fake packets for Fake Request Mode from HEX values (like 1234abcDEF).
                          This option can be supplied multiple times, in this case each fake packet
                          would be sent on every request in the command line argument order.
 --fake-with-sni <value>  Generate fake packets for Fake Request Mode with given SNI domain name.
                          The packets mimic Mozilla Firefox 130 TLS ClientHello packet
                          (with random generated fake SessionID, key shares and ECH grease).
                          Can be supplied multiple times for multiple fake packets.
 --fake-gen <value>       Generate random-filled fake packets for Fake Request Mode, value of them
                          (up to 30).
 --fake-resend <value>    Send each fake packet value number of times.
                          Default: 1 (send each packet once).
 --max-payload [value]    packets with TCP payload data more than [value] won't be processed.
                          Use this option to reduce CPU usage by skipping huge amount of data
                          (like file transfers) in already established sessions.
                          May skip some huge HTTP requests from being processed.
                          Default (if set): --max-payload 1200.

LEGACY Mod Setleri:
 -1          -p -r -s -f 2 -k 2 -n -e 2 (en uyumlu mod)
 -2          -p -r -s -f 2 -k 2 -n -e 40 ((HTTPS için daha iyi hız, yine de uyumlu)
 -3          -p -r -s -e 40 (HTTP ve HTTPS için daha iyi hız)
 -4          -p -r -s (en iyi hız)

Modern Mod Setleri (daha kararlı, daha uyumlu, daha hızlı):
 -5          -f 2 -e 2 --auto-ttl --reverse-frag --max-payload (otomatik TTL, ters parçalama; hızlı ve uyumlu)
 -6          -f 2 -e 2 --wrong-seq --reverse-frag --max-payload (yanlış sıra numarası ile DPI atlatma)
 -7          -f 2 -e 2 --wrong-chksum --reverse-frag --max-payload  (yanlış kontrol toplamı ile DPI atlatma)
 -8          -f 2 -e 2 --wrong-seq --wrong-chksum --reverse-frag --max-payload (sıra + kontrol toplamı kombinasyonu)
 -9          -f 2 -e 2 --wrong-seq --wrong-chksum --reverse-frag --max-payload -q (varsayılan değer, en etkili ve sessiz mod)

NOT: --wrong-seq ve --wrong-chksum kombinasyonu, iki farklı sahte paket üretir.
```

⚠️ Bilinen Sorunlar
=========================
* Eski Windows 7 kurulumlarında, SHA256 dijital imzalarına yönelik desteğin olmaması nedeniyle WinDivert sürücüsünü yükleyemiyor. KB3033929 [x86](https://www.microsoft.com/en-us/download/details.aspx?id=46078)/[x64](https://www.microsoft.com/en-us/download/details.aspx?id=46148) güncelleme paketini yükleyin veya daha iyi seçenek olan Windows Güncelleme'yi kullanarak tüm sisteminizi en yeni sürüme güncelleyin.
* Intel/Qualcomm Killer ağ kartları: Killer Control Center'daki Advanced Stream Detect, GoodbyeDPI ile uyumlu değil, [devre dışı bırakın](https://github.com/ValdikSS/GoodbyeDPI/issues/541#issuecomment-2296038239).
* QUIK ticaret yazılımı [GoodbyeDPI ile çakışabilir](https://github.com/ValdikSS/GoodbyeDPI/issues/677#issuecomment-2390595606). Çözüm için önce QUIK'i daha sonra GoodbyeDPI'ı başlatın.
* ~~Bazı SSL/TLS yığınları parçalanmış ClientHello paketlerini işleyemiyor ve HTTPS web siteleri açılmıyor. Hata: [#4](https://github.com/ValdikSS/GoodbyeDPI/issues/4), [#64](https://github.com/ValdikSS/GoodbyeDPI/issues/64).~~ Parçalanma sorunları v0.1.7'de düzeltildi.
* ~~ESET Antivirus, WinDivert sürücüsüyle uyumsuzdur [#91](https://github.com/ValdikSS/GoodbyeDPI/issues/91). Bu büyük ihtimalle WinDivert değil, antivirüs hatasıdır.~~

👮 Yasal Sorumluluk
=========================
> [!IMPORTANT]
Bu uygulama ve yazılım dosyalarının kullanımı sonucunda doğabilecek her türlü yasal sorumluluk, kullanıcıların kendine aittir. Uygulama ve yazılım dosyaları, açık kaynak kodludur ve yalnızca araştırma, eğitim, bilgi paylaşımı ve kodlama eğitimi amacıyla geliştirilmiştir. Bu şartlar altında kullanılıp, kullanılmaması tamamen kullanıcıların kendi insiyatifine bırakılmıştır. 

❤️ Özel Teşekkürler
=========================
[Goodbye DPI](https://github.com/ValdikSS/GoodbyeDPI) geliştiricisi **@ValdikSS**'e teşekkürler.

[WinDivert](https://github.com/basil00/WinDivert) geliştiricisi **@basil00**'a teşekkürler.

[BlockCheck](https://github.com/ValdikSS/blockcheck)'e katkıda bulunan herkese teşekkürler.

SuperOnline alternatif dosya eki için **@cagritaskn**'a teşekkürler.
