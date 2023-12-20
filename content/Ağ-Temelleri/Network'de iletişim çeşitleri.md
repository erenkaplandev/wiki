 [[Ağ Temelleri]]
## 1 - Unicast (Tek noktaya yayın)
A ---> B 
Bir cihazdan bir cihaza veri aktarımı, iletişime geçilmesi.
![[unicast1.png]]
Bilgisayarar 4'ten Bilgisayar 5'e Unicast yayın yapılabilir. Unicast yayın. En yaygın kullanılan iletişim çeşitlerinden birisidir. 

## 2 - Broadcast (Genel yayın)
A ---> B, C, D, E ve F'ye yayın yapabilir(alt ağ maskeleri)

Bir cihazdan aynı subnet'deki(aynı alt ağdaki) veya aynı network'deki diğer tüm cihazlar ile iletişime geçmesi, veri aktarması. Alıcı pozisyonundaki cihazlar gönderilen veri ile ilgili olsa da olmasa da veri tüm cihazlara iletilir. Broadcast normalde bizim networkde istediğimiz iletişim şekli değildir. Güvenlik ve performans açısından birçok probleme neden olabilir. Bu nedenle router gibi L3 Switch(Yönlendirme özelliği olan switch türü.) gibi cihazlar tarafından Broadcast trafiği kısıtlanır veya bloklanır. Yani broadcast trafiği networkler arasında her yere gidemez. IPv4'ten bilimnen bu problemler nedeniyle IPv6'da da broadcast trafiği desteklenmez. Temelde broadcast mantığı aynı alt ağ içerisinde bir cihazdan gönderilen veri diğer tüm cihazlar tarafından alınır. 

### Nerde kullanılır?
Örneğin ARP protokolü ile. ARP protokolü broadcast yaparak MAC adreslerini öğreniyor. Veya başka bir örnek, Network'de kullanıcılara IP parametrelerine dinamik olarak atayan DHCP protokolüne keşif paketlerini broadcast olarak tüm cihazlara gönderiyor. 

![[broadcast1.png]]
## 3 - Multicast (Çoklu yayın)
A ---> B, D, F 

Bir cihaz birden çok cihaz ile iletişime geçiyor. Fakat broadcastden farklı olarak gönderilen veri ilgili cihazlara iletiliyor. Yani hangi cihazlar bu veri ile ilgiliyse veri onlara veri iletiliyor. Bir grup hedef bilgisayara aynı anda veri iletimi yapılıyor.  


**SORU:** Bir istemci-sunucu sistemi bir uydu ağı kullanmaktadır. Bu ağda uydular dünyadan 37.000km uzaklıktadır. İstemcinin göndermiş olduğu bir istek mesajına en az ne kadar süre sonra istemciye ulaşır.

(4 * ışık hızı) / kilometre