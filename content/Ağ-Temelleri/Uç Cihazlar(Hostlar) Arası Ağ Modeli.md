[[Ağ Temelleri]]
#ağ #OSI
Kaynak <--> Kanal <---> Alıcı

Uç cihazları, ağ ara cihazları ve medya ile birbirine bağlamak aralarında bir iletişim olması için yeterli değildir. Uç cihazlar aralarında iletişim sağlanması için aynı insanların birbirleri ile iletişim sağlarken kullandıkları kurallar gibi kurallar belirlenmiş olması gereklidir. Tüm iletişim çeşitlerinde üç orta öge bulunur. Mesajı gönderen kaynak, mesajı alan alıcı ve mesajın iletildiği kanal. Bir kanal aralığı ile kaynaktan alıcıya bir mesaj gönderilirken **protokol** denen belirli kurallar kullanılır. Farklı iletişim çeşitlerinde farklı protokoller kullanılabilir. Örneğin, günlük hayatta mektup gönderirken uygulanan kurallar ile sms gönderilirken kullanılanlar farklıdır. Aynı şekilde bilgisayarlar arasında iletişim gerçekleşirken belirli kurallar bütünü yani protokoller kullanılmaktadır. 

# Uç Cihazlar Arası Ağ İletişiminin Temelleri
Öncelleri bilgisayar<->bilgisayar, bilgisayar<->sunucu, bilgisayar<->ağ yazıcısı gibi uç cihazlar arası ağ iletişiminde marka bağımlı modeller kullanılmaktaydı. Örneğin IBM firmasının ürettiği bilgisayar ve ağ cihazları kendilerine özgü ağ iletişim sistemi ve protokoller kullanıyorken, başka bir firmanın cihazı IBM ağında kullanılamıyordu. Yani her üretici kendine özgü çözümler ve protokoller sunuyordu. Bu karmaşıklığın ve sorunun önüne geçebilmek için katmanlı bir ağ standartı geliştirilmeye başlandı. Böylelikle bütün üreticilerin cihazları birbirleriyle sorunsuz bir şekilde anlaşacaktı. OSI ve TCP/IP modelleri bu ihtiyaç sonucunda ortaya çıkmıştır. 

# OSI Referans Modeli 
ISO 1984 yılında OSI ismini verdiği 7 katmanlı (layer) açık standart referans modelini yayınladı. Bu referans modelinin yayınlanmasındaki amaç bir referans modeli oluşturmak ve aynı zamanda internette kullanılacak bir protokol paketi sunmaktı. Fakat çok daha önceleri geliştirilmeye başlanan TCP/IP protokol kümesi daha popüler hale geldi ve internet için OSI referans modeli yerine TCP/IP protokol kümesi tercih edilmeye başlandı.

Ağ protokolleri ve çalışmalarını açıklamak için katmanlı model kullanmanın belirli avantajları vardır:
- Farklı üreticilerin ürünleri birbirleri ile sorunsuz çalışabilir.
- Ağ işlevlerini sağlamak için ortak bir dil sunar.
- Bir katmandaki teknolojik gelişmeler diğer katmanları etkilemez. Örneğin IPv4'den IPv6'ya geçilmesi gibi.
- Belirli bir katmanda çalışan protokoller. Alt ve üst katmanlarla beraber tanımlı olduğu için protokol tasarımlarında yeniliklere yardımcı olur.

OSI referans modeli, her bir katmanda gerçekleşen işlemleri ve bir katmanın alt ve üst katmanlarla olan etkileşimini açıklar.

| 7-Uygulama        | HTTP, SMTP, POP3, IMAP, FTP, TFTP                               | Hostlar, Güvenlik Duvarı                                                 |     |
| ----------------- | --------------------------------------------------------------- | ------------------------------------------------------------------------ | --- |
| 6-Sunum           | ISO 8822, ISO 8823, ISO 8824, ITU-T T.73, ITU-T X.409           | ""                                                                       |     |
| 5-Oturum          | NFS, SMB, ISO 8326, ISO 8327, ITU-T T.6299, ...                 | ""                                                                       |     |
| 4-Taşıma          | TCP, UDP, SCTP, DCCP                                            | ""                                                                       |     |
| 3-Ağ              | IP, IPv4, IPv6, ICMP, ARP, İnternet Grup Yönetim Protokolü, IPX | Yönlendiriciler (Router)                                                 |     |
| 2-Veri bağlantısı | Ethernet, HDLC, Wi-Fi, Token ring, FDDI, PPP, L2Tp              | Anahtarlar(Switch), Kablosuz erişim noktaları, Kablo modem, DSL modemler |     |
| 1-Fiziksel        | ISDN, RS-232, EIA-422, RS-449, EIA-485                          | Dağıtıcılar(HUB), Kablolar                                               |     |

**Katman 7:** uygulama katmanı kullanıcılara bir arayüz sağlar. Kullanıcıların bilgisayar ile etkileşime geçtiği katmandır 

**Katman 6:** sunum katmanı, uygulama katmanına veri sunar ve bunu yaparken verileri beliri biçimlerde kodlamak, sıkıştırmak ve çevirmekten sorumludur. Örneğin verinin **.jpg** formatında biçimlendirilmesi gibi. Ayrıca gönderen bilgisayarın uygulama katmanından aktarılan verinin alıcı bilgisayarların uygulama katmanından okumasını garanti sunar. 

**Katman 5:** oturum katmanı, gönderen ve alıcı bilgisayar sunum katmanları arasındaki oturumları kurmak düzenlemek ve yönetmekten sorumludur. 

**Katman 4:** taşıma katmanı, gönderen ve alan bilgisayar arasında iletilen veriyim **segmentlere**(parçalar) ayırmak, aktarmak ve tekrar birleştirmekten sorumludur. 

**Katman 3:** ağ katmanı, cihazların belirli adreslerle(iplerle) tanımlanmasını, verinin üretilmesi için en iyi yolun belirlenmesine ve farklı ağlar arasında iletilmesine sağlamaktan sorumludur.

**Katman 2:** veri bağlantısı katmanı, veri çerçevelerinin cihazlar arasında fiziksel aktarımını sağlar. Ayrıca ağ katmanından gelen paketleri bir alt katman olan fiziksel katman için bitlere(1'ler ve 0'lar) dönüştürmekten sorumludur.

**Katman 1:** fiziksel katman gönderici ve alıcı cihazlar arasında kullanılan medya(kablolu, kablosuz, fiberoptik, bakır) üst katmanlardan gelen bitleri gönderir veya alır. Ayrıca bitleri gönderip alırken fiziksel bağlantıları etkinleştirmek, korumak veya devredışı bırakmak için gerekli mekanik, elektriksel ve fonksiyonel yolları tanımlamaktan sorumludur.