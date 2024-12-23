Bu proje Türkiye'de kalıcı olarak engellenmiş **Discord** ve bazı durumlarda engellenen **Instagram**, **Youtube** vb. web sitesi ve uygulamalara VPN kullanmadan ve İnternet hızında bir değişiklik olmadan giriş yapmanızı sağlamak için GoodByeDPI'ın orjinal reposundan çatallanmış ve düzenlenmiş bir sürümüdür.

GoodbyeDPI — Derin Paket İncelemesi Atlatma Aracı
=========================
Bu yazılım, birçok İnternet Servis Sağlayıcısında bulunan ve belirli web sitelerine erişimi engelleyen **Derin Paket İnceleme Sistemleri**ni atlatmak için tasarlanmıştır.

Optik ayırıcı veya port yansıtma (**Pasif DPI**) kullanılarak bağlanan ve herhangi bir veriyi engellemeyen ancak istenen hedeften daha hızlı yanıt veren DPI'ları ve sırayla bağlanan **Aktif DPI**'ları işler.

**Windows 7, 8, 8.1, 10 ve 11** işletim sistemlerinde, yapılandırma dosyalarının **Yönetici** olarak çalıştırılması gerekir.

Virüs, Veri Sızıntısı ve Bitcoin Madenciliği
=========================
Yazılım açık kaynak kodlu olduğundan tüm kodları gözatıp inceleyebilirsiniz. WinDivert.dll ve WinDivert64.sys dosyaları fonksiyonlarından dolayı bazı antivirüs programlarında virüs olarak algılanabilir. Ancak Bu DLL ve SYS dosyaları da açık kaynak kodludur ve istendiğinde herhangi bir **Not Defteri**, **NotePad++** vb. uygulama ile düzenle diyerek incelenebilir. Yazılımı kullanmak ya da kullanmamak tamamen sizin kendi insiyatifinizdedir.

Bu dosya virüslü, bilgilerim çalındı vb. yalan yanlış ithamlara kulak asmayın. Dilerseniz indirmeden önce bağlantı adresini kullanarak [buradan](https://www.virustotal.com/gui/home/upload) veya dosyayı indirdikten sonra dosyayı yükleyerek [buradan](https://www.virustotal.com/gui/home/url) virüs taraması yapabilirsiniz.

Teknolojinin geldiği bu noktada yazılım kodlarının ne işe yaradığını ve ne amaçla yazıldığını bile öğrenmek mümkün, hem de tek bir satır kod bilgisi olmadan.

Kodların ne işe yaradığını ve hangi amaçla yazıldığını öğrenmek için [buraya](https://chatgpt.com/) tıklayın ardından **Bu kodlarda virüs var mı? Hangi amaçla yazılmış? Ne işe yarıyor? Bilgilerim çalınır mı? Bitcoin madenciği yapıyor mu?** sorununu yazdıktan sonra **SHIFT + ENTER** tuşlarına basarak 2 satır aşağı inin ve ilgili kodu da yapıştırıp gönderin :)

# Hızlı Başlangıç

* **Türkiye** için [son sürümler sayfasından](https://github.com/delidolu1adam/GoodbyeDPI_Turkiye/releases) ZIP dosyasını indirin, ZIP dosyasını ayıklayın ve içindeki **01 - CloudFlare DNS Yönlendirmeli.cmd** yapılandırma dosyasına sağ tıklayarak **Yönetici Olarak** çalıştırın.

* **Rusya** için [son sürümler sayfasından](https://github.com/delidolu1adam/GoodbyeDPI_Turkiye/releases) ZIP dosyasını indirin, ZIP dosyasını ayıklayın ve içindeki **07 - Yandex DNS Yönlendirmeli.cmd** yapılandırma dosyasına sağ tıklayarak **Yönetici Olarak** çalıştırın.

* **Diğer Ülkeler** için [son sürümler sayfasından](https://github.com/delidolu1adam/GoodbyeDPI_Turkiye/releases) ZIP dosyasını indirin, ZIP dosyasını ayıklayın ve içindeki **01 - CloudFlare DNS Yönlendirmeli.cmd** yapılandırma dosyasına sağ tıklayarak **Yönetici Olarak** çalıştırın.

Bu yapılandırma dosyaları, GoodbyeDPI'ı önerilen modda başlatır ve DNS çözücü yönlendirmesini çalıştırdığınız yapılandırma dosyasına göre CloudFlare, Google, Quad9, OpenDNS, AdGuard, Yandex ve Comodo DNS adreslerine (DNS zehirlenmesini engellemek için) standart olmayan bir port üzerinden yapar. Eğer çalıştıysa — tebrikler! Şu anda olduğu gibi kullanabilirsiniz veya daha fazla yapılandırma yapabilirsiniz.

# Nasıl Kullanılır?

Download [latest version from Releases page](https://github.com/ValdikSS/GoodbyeDPI/releases) and run.

## Desteklenen Argümanlar
Programınızın sürümü hakkında tüm bilgileri öğrenmek için başlangıçta -h (--help) argümanını kullanın.
```ansi
Örnek Kullanım: goodbyedpi.exe -5 **veya** goodbyedpi.exe -5 --dns-addr 1.1.1.1 --dns-port 53 --dnsv6-addr 2606:4700:4700::1111 --dnsv6-port 53

-p: Pasif DPI'yi engelle
-q: QUIC/HTTP3'ü engelle
-r: Host başlığını "hoSt" olarak değiştir
-s: Host başlığı ile değeri arasındaki boşluğu kaldır
-m: Host başlığındaki harfleri karıştır (test.com -> tEsT.cOm)
-f <değer>: HTTP parçalama (fragmentation) değerini ayarla
-k <değer>: HTTP kalıcı (keep-alive) bağlantı parçalamayı etkinleştir ve değeri ayarla
-n: -k etkinleştirildiğinde ilk segmentin ACK'ını bekleme
-e <değer>: HTTPS parçalama değerini ayarla
-a: Yöntem (Method) ile İstek URI'sı (Request-URI) arasında ekstra boşluk (bu, -s'yi etkinleştirir ve bazı siteleri bozabilir)
-w: İşlenen tüm portlarda HTTP trafiğini bulmayı ve çözümlemeyi dene (yalnızca port 80'de değil)
--port <değer>: Parçalama yapacak ek bir TCP portu (ve -w ile HTTP hileleri)
--ip-id <değer>: Ekstra bir IP kimliğini (decimal) yönet, bu kimlik ile yönlendirmeleri ve TCP RST'leri engelle. Bu seçenek birden fazla kez kullanılabilir.
--dns-addr <değer>: UDP DNS isteklerini sağlanan IP adresine yönlendir (deneysel)
--dns-port <değer>: UDP DNS isteklerini sağlanan porta yönlendir (varsayılan 53)
--dnsv6-addr <değer>: UDPv6 DNS isteklerini sağlanan IPv6 adresine yönlendir (deneysel)
--dnsv6-port <değer>: UDPv6 DNS isteklerini sağlanan porta yönlendir (varsayılan 53)
--dns-verb: Ayrıntılı DNS yönlendirme mesajları yazdır
--blacklist <txtfile>: Yalnızca verilen metin dosyasındaki host adları ve alt alan adları için engelleme hilelerini uygula (HTTP Host/TLS SNI). Bu seçenek birden fazla kez verilebilir.
--allow-no-sni: TLS SNI tespit edilemezse, --blacklist etkinleştirildiğinde engelleme işlemini uygula.
--frag-by-sni: Eğer TLS paketinde SNI tespit edilirse, paketi SNI değeri öncesinde parçala.
--set-ttl <değer>: Sahte İstek Modunu etkinleştir ve sağlanan TTL değeri ile gönder. DİKKATLİ KULLANIN! Web sitelerini beklenmedik şekillerde bozabilir. Dikkatli kullanın (veya --blacklist ile).
--auto-ttl [a1-a2-m]: Sahte İstek Modunu etkinleştir, TTL'yi otomatik olarak tespit et ve mesafeye göre azalt. Eğer mesafe a2'den kısa ise TTL a2 kadar azalır. Daha uzunsa, (a1; a2) ölçeği kullanılarak mesafe ağırlık olarak kabul edilir. Eğer sonuç TTL m’den büyükse, TTL'yi m olarak ayarla. Varsayılan: --auto-ttl 1-4-10. Ayrıca --min-ttl 3'ü ayarlar. DİKKATLİ KULLANIN! Web sitelerini beklenmedik şekilde bozabilir. Dikkatli kullanın (veya --blacklist ile).
--min-ttl <değer>: Sahte İstek Modunda --set-ttl ve --auto-ttl modlarında gönderilecek Sahte İstek için minimum TTL mesafesi (128/64 - TTL).
--wrong-chksum: Sahte İstek Modunu etkinleştir ve yanlış TCP checksum ile gönder. Sanal makinelerde veya bazı yönlendiricilerle çalışmayabilir, ancak set-ttl’den daha güvenlidir.
--wrong-seq: Sahte İstek Modunu etkinleştir ve TCP SEQ/ACK geçmişteki bir değeriyle gönder.
--native-frag: Paketleri daha küçük parçalara ayırarak, pencere boyutunu küçültmeden gönder. Daha hızlı çalışır (bağlantıyı yavaşlatmaz) ve daha iyi sonuç verir.
--reverse-frag: --native-frag gibi paketleri parçalara ayır, ancak ters sırayla gönder. HTTPS TLS ClientHello segmentlerini işleyemeyen web siteleriyle çalışır (çünkü TCP akışını "birleştirilmiş" alırlar).
--fake-from-hex <değer>: Sahte İstek Modunda HEX değerlerinden (örneğin, 1234abcDEF) sahte paketler yükle. Bu seçenek birden fazla kez verilebilir, bu durumda her sahte paket komut satırı argüman sırasına göre her istekte gönderilir.
--fake-with-sni <değer>: Sahte İstek Modunda verilen SNI alan adı ile sahte paketler üret. Bu paketler Mozilla Firefox 130 TLS ClientHello paketini taklit eder (rastgele üretilmiş sahte SessionID, anahtar paylaşımları ve ECH grease ile).
--fake-gen <değer>: Sahte İstek Modu için rastgele doldurulmuş sahte paketler üret, değer kadar (30'a kadar).
--fake-resend <değer>: Her sahte paketi belirtilen sayı kadar yeniden gönder. Varsayılan: 1 (her paketi bir kez gönder).
--max-payload [değer]: TCP yük verisi [değer]’den büyük olan paketler işlenmeyecektir. Bu seçenek, zaten kurulmuş oturumlarda büyük miktarda veriyi atlayarak CPU kullanımını azaltmak için kullanılabilir. Büyük HTTP isteklerinin işlenmesini engelleyebilir. Varsayılan: --max-payload 1200.
Eski Mod Ayarları:
-1: -p -r -s -f 2 -k 2 -n -e 2 (en uyumlu mod)
-2: -p -r -s -f 2 -k 2 -n -e 40 (HTTPS için daha iyi hız, yine de uyumlu)
-3: -p -r -s -e 40 (HTTP ve HTTPS için daha iyi hız)
-4: -p -r -s (en iyi hız)
Modern Mod Ayarları (daha stabil, daha uyumlu, daha hızlı):
-5: -f 2 -e 2 --auto-ttl --reverse-frag --max-payload
-6: -f 2 -e 2 --wrong-seq --reverse-frag --max-payload
-7: -f 2 -e 2 --wrong-chksum --reverse-frag --max-payload
-8: -f 2 -e 2 --wrong-seq --wrong-chksum --reverse-frag --max-payload
-9: -f 2 -e 2 --wrong-seq --wrong-chksum --reverse-frag --max-payload -q (varsayılan ayar)

Not: Bu argümanlar, çeşitli internet trafiği manipülasyonları ve güvenlik ayarları yaparak, kullanıcıların sansürü aşmalarını ve internet trafiği üzerinde daha fazla kontrol sahibi olmalarını sağlar. **--wrong-seq** ve **--wrong-chksum** kombinasyonu iki farklı sahte paket üretir.
```
## Nasıl Kontrol Edilir?
İnternet servis sağlayıcınızın DPI'sinin aşılabileceğini kontrol etmek için öncelikle tarayıcınızda "Güvenli DNS (HTTPS üzerinden DNS)" seçeneğini etkinleştirerek sağlayıcınızın DNS yanıtlarını zehirlemediğinden emin olun.

* **Google Chrome**: [Ayarlar](chrome://settings/) → [Gizlilik ve güvenlik](chrome://settings/privacy) → [Güvenlik](chrome://settings/security) → Güvenli DNS kullan → DNS sağlayıcısı seç: CloudFlare
* **Mozilla Firefox**: [Ayarlar](about:preferences) → Ağ Ayarları → HTTPS üzerinde DNS'yi etkinleştir → DNS sağlayıcısı seç: CloudFlare

Daha sonra Türkiye ve diğer Ülkeler için **08 - DNS Yönlendirmesiz v1.cmd** veya Rusya için **08 - DNS Yönlendirmesiz v2.cmd** dosyasını herhangi bir argüman olmadan çalıştırın. Eğer çalışırsa — tebrikler! Olduğu gibi kullanabilir veya örneğin ülkeniz için engellenen web sitelerinin listesi biliniyorsa ve kullanılabilirse `--blacklist` argümanını kullanarak daha fazla yapılandırabilirsiniz.

Sağlayıcınız DNS isteklerini engelliyorsa, standart olmayan bir portta (örneğin Yandex DNS `77.88.8.8:1253`) çalışan genel bir DNS çözücüsüne `--dns-addr` seçeneğini kullanmak veya üçüncü taraf uygulamaları kullanarak HTTPS/TLS üzerinden DNS yapılandırmak isteyebilirsiniz.

.cmd betiklerini kontrol edin ve tercihinize ve ağ koşullarınıza göre değiştirin.

# How does it work

### Passive DPI

Most Passive DPI send HTTP 302 Redirect if you try to access blocked website over HTTP and TCP Reset in case of HTTPS, faster than destination website. Packets sent by DPI usually have IP Identification field equal to `0x0000` or `0x0001`, as seen with Russian providers. These packets, if they redirect you to another website (censorship page), are blocked by GoodbyeDPI.

### Active DPI

Active DPI is more tricky to fool. Currently the software uses 7 methods to circumvent Active DPI:

* TCP-level fragmentation for first data packet
* TCP-level fragmentation for persistent (keep-alive) HTTP sessions
* Replacing `Host` header with `hoSt`
* Removing space between header name and value in `Host` header
* Adding additional space between HTTP Method (GET, POST etc) and URI
* Mixing case of Host header value
* Sending fake HTTP/HTTPS packets with low Time-To-Live value, incorrect checksum or incorrect TCP Sequence/Acknowledgement numbers to fool DPI and prevent delivering them to the destination

These methods should not break any website as they're fully compatible with TCP and HTTP standards, yet it's sufficient to prevent DPI data classification and to circumvent censorship. Additional space may break some websites, although it's acceptable by HTTP/1.1 specification (see 19.3 Tolerant Applications).

The program loads WinDivert driver which uses Windows Filtering Platform to set filters and redirect packets to the userspace. It's running as long as console window is visible and terminates when you close the window.

# How to build from source

This project can be build using **GNU Make** and [**mingw**](https://mingw-w64.org). The only dependency is [WinDivert](https://github.com/basil00/Divert).

To build x86 exe run:

`make CPREFIX=i686-w64-mingw32- WINDIVERTHEADERS=/path/to/windivert/include WINDIVERTLIBS=/path/to/windivert/x86`

And for x86_64:

`make CPREFIX=x86_64-w64-mingw32- BIT64=1 WINDIVERTHEADERS=/path/to/windivert/include WINDIVERTLIBS=/path/to/windivert/amd64`

# How to install as Windows Service

Check examples in `service_install_russia_blacklist.cmd`, `service_install_russia_blacklist_dnsredir.cmd` and `service_remove.cmd` scripts.

Modify them according to your own needs.

# Known issues

* Horribly outdated Windows 7 installations are not able to load WinDivert driver due to missing support for SHA256 digital signatures. Install KB3033929 [x86](https://www.microsoft.com/en-us/download/details.aspx?id=46078)/[x64](https://www.microsoft.com/en-us/download/details.aspx?id=46148), or better, update the whole system using Windows Update.
* Intel/Qualcomm Killer network cards: `Advanced Stream Detect` in Killer Control Center is incompatible with GoodbyeDPI, [disable it](https://github.com/ValdikSS/GoodbyeDPI/issues/541#issuecomment-2296038239).
* QUIK trading software [may interfere with GoodbyeDPI](https://github.com/ValdikSS/GoodbyeDPI/issues/677#issuecomment-2390595606). First start QUIK, then GoodbyeDPI.
* ~~Some SSL/TLS stacks unable to process fragmented ClientHello packets, and HTTPS websites won't open. Bug: [#4](https://github.com/ValdikSS/GoodbyeDPI/issues/4), [#64](https://github.com/ValdikSS/GoodbyeDPI/issues/64).~~ Fragmentation issues are fixed in v0.1.7.
* ~~ESET Antivirus is incompatible with WinDivert driver [#91](https://github.com/ValdikSS/GoodbyeDPI/issues/91). This is most probably antivirus bug, not WinDivert.~~


# Similar projects

- **[zapret](https://github.com/bol-van/zapret)** by @bol-van (for MacOS, Linux and Windows)
- **[Green Tunnel](https://github.com/SadeghHayeri/GreenTunnel)** by @SadeghHayeri (for MacOS, Linux and Windows)
- **[DPI Tunnel CLI](https://github.com/nomoresat/DPITunnel-cli)** by @zhenyolka (for Linux and routers)
- **[DPI Tunnel for Android](https://github.com/nomoresat/DPITunnel-android)** by @zhenyolka (for Android)
- **[PowerTunnel](https://github.com/krlvm/PowerTunnel)** by @krlvm (for Windows, MacOS and Linux)
- **[PowerTunnel for Android](https://github.com/krlvm/PowerTunnel-Android)** by @krlvm (for Android)
- **[SpoofDPI](https://github.com/xvzc/SpoofDPI)** by @xvzc (for macOS and Linux)
- **[SpoofDPI-Platform](https://github.com/r3pr3ss10n/SpoofDPI-Platform)** by @r3pr3ss10n (for Android, macOS, Windows)
- **[GhosTCP](https://github.com/macronut/ghostcp)** by @macronut (for Windows)
- **[ByeDPI](https://github.com/hufrea/byedpi)** for Linux/Windows + **[ByeDPIAndroid](https://github.com/dovecoteescapee/ByeDPIAndroid/)** for Android (no root)
- **[youtubeUnblock](https://github.com/Waujito/youtubeUnblock/)** by @Waujito (for OpenWRT/Entware routers and Linux)

# Kudos

Thanks @basil00 for [WinDivert](https://github.com/basil00/Divert). That's the main part of this program.

Thanks for every [BlockCheck](https://github.com/ValdikSS/blockcheck) contributor. It would be impossible to understand DPI behaviour without this utility.
