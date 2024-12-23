Bu proje Türkiye'de kalıcı olarak engellenmiş **Discord** ve bazı durumlarda engellenen **Instagram**, **Youtube** vb. web sitesi ve uygulamalara VPN kullanmadan ve İnternet hızında bir değişiklik olmadan giriş yapmanızı sağlamak için GoodByeDPI'ın orjinal reposundan çatallanmış ve düzenlenmiş bir sürümüdür.

Daha fazla bilgi edinmek isterseniz indirdiğiniz **GoodBye DPI Türkiye v0.2.3rc3/assets/documents** klasör içeriğindeki **_Turkish** etiketli dosyalara göz atın.

GoodbyeDPI — Derin Paket İncelemesi Atlatma Aracı
=========================
Bu yazılım, birçok İnternet Servis Sağlayıcısında bulunan ve belirli web sitelerine erişimi engelleyen **Derin Paket İnceleme Sistemleri**ni atlatmak için tasarlanmıştır.

Optik ayırıcı veya port yansıtma (**Pasif DPI**) kullanılarak bağlanan ve herhangi bir veriyi engellemeyen ancak istenen hedeften daha hızlı yanıt veren DPI'ları ve sırayla bağlanan **Aktif DPI**'ları işler.

**Windows 7, 8, 8.1, 10 ve 11** işletim sistemlerinde, komut dosyalarının **Yönetici** olarak çalıştırılması gerekir.

Virüs, Veri Sızıntısı ve Bitcoin Madenciliği
=========================
Yazılım açık kaynak kodlu olduğundan tüm kodları gözatıp inceleyebilirsiniz. WinDivert.dll ve WinDivert64.sys dosyaları fonksiyonlarından dolayı bazı antivirüs programlarında virüs olarak algılanabilir. Ancak Bu DLL ve SYS dosyaları da açık kaynak kodludur ve istendiğinde herhangi bir **Not Defteri**, **NotePad++** vb. uygulama ile düzenle diyerek incelenebilir. Yazılımı kullanmak ya da kullanmamak tamamen sizin kendi insiyatifinizdedir.

Bu dosya virüslü, bilgilerim çalındı vb. yalan yanlış ithamlara kulak asmayın. Dilerseniz indirmeden önce bağlantı adresini kullanarak [buradan](https://www.virustotal.com/gui/home/upload) veya dosyayı indirdikten sonra dosyayı yükleyerek [buradan](https://www.virustotal.com/gui/home/url) virüs taraması yapabilirsiniz.

Teknolojinin geldiği bu noktada yazılım kodlarının ne işe yaradığını ve ne amaçla yazıldığını bile öğrenmek mümkün, hem de tek bir satır kod bilgisi olmadan.

Kodların ne işe yaradığını ve hangi amaçla yazıldığını öğrenmek için [buraya](https://chatgpt.com/) tıklayın ardından **Bu kodlarda virüs var mı? Hangi amaçla yazılmış? Ne işe yarıyor? Bilgilerim çalınır mı? Bitcoin madenciği yapıyor mu?** sorununu yazdıktan sonra **SHIFT + ENTER** tuşlarına basarak 2 satır aşağı inin ve ilgili kodu da yapıştırıp gönderin :)

# Hızlı Başlangıç

* **Türkiye** için [son sürümler sayfasından](https://github.com/delidolu1adam/GoodbyeDPI_Turkiye/releases) ZIP dosyasını indirin, ZIP dosyasını ayıklayın ve içindeki **01 - CloudFlare DNS Yönlendirmeli.cmd** komut dosyasına sağ tıklayarak **Yönetici Olarak** çalıştırın.

* **Rusya** için [son sürümler sayfasından](https://github.com/delidolu1adam/GoodbyeDPI_Turkiye/releases) ZIP dosyasını indirin, ZIP dosyasını ayıklayın ve içindeki **07 - Yandex DNS Yönlendirmeli.cmd** komut dosyasına sağ tıklayarak **Yönetici Olarak** çalıştırın.

* **Diğer Ülkeler** için [son sürümler sayfasından](https://github.com/delidolu1adam/GoodbyeDPI_Turkiye/releases) ZIP dosyasını indirin, ZIP dosyasını ayıklayın ve içindeki **01 - CloudFlare DNS Yönlendirmeli.cmd** komut dosyasına sağ tıklayarak **Yönetici Olarak** çalıştırın.

Bu komut dosyaları, GoodbyeDPI'ı önerilen modda başlatır ve DNS çözücü yönlendirmesini çalıştırdığınız komut dosyasına göre CloudFlare, Google, Quad9, OpenDNS, AdGuard, Yandex ve Comodo DNS adreslerine (DNS zehirlenmesini engellemek için) standart olmayan bir port üzerinden yapar. Eğer çalıştıysa — tebrikler! Şu anda olduğu gibi kullanabilirsiniz veya daha fazla yapılandırma yapabilirsiniz.

# Nasıl Kullanılır?

Download [latest version from Releases page](https://github.com/ValdikSS/GoodbyeDPI/releases) and run.

## Desteklenen Argümanlar
Programınızın sürümü hakkında tüm bilgileri öğrenmek için başlangıçta -h (--help) argümanını kullanın.
```
Örnek Kullanım: goodbyedpi.exe -5 **veya** goodbyedpi.exe -5 --dns-addr 1.1.1.1 --dns-port 53 --dnsv6-addr 2606:4700:4700::1111 --dnsv6-port 53

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

.cmd komut dosyalarını kontrol edin ve tercihinize ve ağ koşullarınıza göre değiştirin.

# Nasıl Çalışır?

### Pasif DPI

Çoğu Pasif DPI, HTTP üzerinden engellenen web sitesine erişmeye çalışırsanız HTTP 302 Yönlendirmesi gönderir ve HTTPS durumunda TCP Sıfırlama, hedef web sitesinden daha hızlıdır. DPI tarafından gönderilen paketlerin genellikle IP Kimlik alanı `0x0000` veya `0x0001`'e eşittir, Rus sağlayıcılarda görüldüğü gibi. Bu paketler, sizi başka bir web sitesine (sansür sayfası) yönlendirirse, GoodbyeDPI tarafından engellenir.

### Aktif DPI

Aktif DPI'ı kandırmak daha zordur. Şu anda yazılım Aktif DPI'ı atlatmak için 7 yöntem kullanıyor:

* İlk veri paketi için TCP düzeyinde parçalanma
* Kalıcı (canlı tutma) HTTP oturumları için TCP düzeyinde parçalanma
* `Host` başlığını `hoSt` ile değiştirme
* `Host` başlığındaki başlık adı ve değer arasındaki boşluğu kaldırma
* HTTP Yöntemi (GET, POST vb.) ve URI arasına ek boşluk ekleme
* Host başlık değerinin harflerini karıştırma
* DPI'ı kandırmak ve bunların hedefe ulaşmasını engellemek için düşük Yaşam Süresi değerine, yanlış toplam kontrolüne veya yanlış TCP Dizisi/Onay numaralarına sahip sahte HTTP/HTTPS paketleri gönderme

Bu yöntemler TCP ve HTTP standartlarıyla tamamen uyumlu oldukları için hiçbir web sitesini bozmamalıdır, ancak DPI veri sınıflandırmasını önlemek ve sansürü atlatmak için yeterlidir. Ek boşluk bazı web sitelerini bozabilir, ancak HTTP/1.1 spesifikasyonuna göre kabul edilebilirdir (bkz. 19.3 Toleranslı Uygulamalar).

Program, filtreleri ayarlamak ve paketleri kullanıcı alanına yönlendirmek için Windows Filtreleme Platformu kullanan WinDivert sürücüsünü yükler. Konsol penceresi görünür olduğu sürece çalışır ve pencereyi kapattığınızda sonlanır.

# Kaynaktan Nasıl İnşa Edilir?

This project can be build using **GNU Make** and [**mingw**](https://mingw-w64.org). The only dependency is [WinDivert](https://github.com/basil00/Divert).

x86 exe'yi derlemek için şunu çalıştırın:

`make CPREFIX=i686-w64-mingw32- WINDIVERTHEADERS=/path/to/windivert/include WINDIVERTLIBS=/path/to/windivert/x86`

x86_64 exe'yi derlemek için şunu çalıştırın:

`make CPREFIX=x86_64-w64-mingw32- BIT64=1 WINDIVERTHEADERS=/path/to/windivert/include WINDIVERTLIBS=/path/to/windivert/amd64`

# Windows Hizmeti Olarak Nasıl Kurulur?

Bunun için `11 - Windows Hizmeti Olarak Kur - DNS Yönlendirmeli v1.cmd`, `12 - Windows Hizmeti Olarak Kur - DNS Yönlendirmeli v2.cmd`, `13 - Windows Hizmeti Olarak Kur - DNS Yönlendirmeli v3.cmd`, `14 - Windows Hizmeti Olarak Kur - DNS Yönlendirmeli v4.cmd`, `15 - Windows Hizmeti Olarak Kur - DNS Yönlendirmesiz Karaliste.cmd`, `16 - Windows Hizmeti Olarak Kur - DNS Yönlendirmeli Karaliste.cmd` ve `17 - Hizmetleri Durdur ve Kaldır.cmd` komut dosyalarındaki yapılandırma örneklerini kontrol edin. Bunları kendi ihtiyaçlarınıza göre değiştirin.

# Bilinen Sorunlar

* Korkunç derecede eski Windows 7 kurulumları, SHA256 dijital imzalarına yönelik desteğin olmaması nedeniyle WinDivert sürücüsünü yükleyemiyor. KB3033929 [x86](https://www.microsoft.com/en-us/download/details.aspx?id=46078)/[x64](https://www.microsoft.com/en-us/download/details.aspx?id=46148) güncelleme paketini yükleyin veya daha iyi seçenek olan Windows Güncelleme'yi kullanarak tüm sisteminizi en yeni sürüme güncelleyin.
* Intel/Qualcomm Killer ağ kartları: Killer Control Center'daki Advanced Stream Detect, GoodbyeDPI ile uyumlu değil, [devre dışı bırakın](https://github.com/ValdikSS/GoodbyeDPI/issues/541#issuecomment-2296038239).
* QUIK ticaret yazılımı [GoodbyeDPI ile çakışabilir](https://github.com/ValdikSS/GoodbyeDPI/issues/677#issuecomment-2390595606). Çözüm için önce QUIK'i daha sonra GoodbyeDPI'ı başlatın.
* ~~Bazı SSL/TLS yığınları parçalanmış ClientHello paketlerini işleyemiyor ve HTTPS web siteleri açılmıyor. Hata: [#4](https://github.com/ValdikSS/GoodbyeDPI/issues/4), [#64](https://github.com/ValdikSS/GoodbyeDPI/issues/64).~~ Parçalanma sorunları v0.1.7'de düzeltildi.
* ~~ESET Antivirus, WinDivert sürücüsüyle uyumsuzdur [#91](https://github.com/ValdikSS/GoodbyeDPI/issues/91). Bu büyük ihtimalle WinDivert değil, antivirüs hatasıdır.~~

# Benzer Projeler

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

# Özel Teşekkür

[WinDivert](https://github.com/basil00/Divert) için @basil00'a teşekkürler.

Her [BlockCheck](https://github.com/ValdikSS/blockcheck) katılımcısına teşekkürler.
