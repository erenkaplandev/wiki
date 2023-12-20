[[Ağ Temelleri]]
## IPv4 Adress Yapısı
A. 0.0.0.0 - 127.255.255.255
B. 128.0.0.0 - 191.255.255.255
C. 192.0.0.0 - 223.255.255.255
D. 124.0.0.0 - 239.255.255.255
E. 240.0.0.0 - 255.255.255.255

* A class'ı son derece büyük ağları desteklenmek üzere tasarlanmıştır.
* B class'ı orta ve büyük boyutlu ağların ihtiyaçlarını desteklemek için tasarlanmıştır.
* C class'ı küçük ağları desteklemek için tasarlanmıştır.
* D class'ı özel kullanım için tasarlanmıştır.
* E class'ı bilimsel araşıtrmalar ve deneyler için ayrılmıştır.

## Private IP

İnternete bağlı olmayan ip'ler ya da internet bağlantısını **proxy server** veya **NAT** aracılıyla sağlayan makinelerde kullanılır. Yani bu adresler internete direkt bağlı makinelerde kullanılmaz, A, B ve C class'larında bulunurlar.

### Örneğin
* 10.0.0.0 - 10.255.255.255.255
* 172.16.0.0 - 172.31.255.255
* 192.168.0.0 - 192.168.255.255

## NAT (Network Adress Translation)

NAT kavramını bir döngü olarak anlayabiliriz. Bir ip adress'inin başka bir ip adresine dönüşümüne NAT denmektedir. İnternette her geçen gün artan kullanıcı sayısı belli başlı sorunlar meydana getirmektedir ve bu sorunların en başı ise **ip adresi atamalarıdır**. Her bir kullanıcı için bir ip adress'i atamak zorundadır ve bu ip adress atamaları sınırlıdır. Günümüzde IPv4 sürümünü kullanmaktayız. VE bu sürüm sınırlı olduğu için, internette de her geçen gün kullanıcı sayısı arttığı için IPv4 ihtiyaçı karşılayamıyor. Bu nedenle BT uzmanları IPv6 teknolojisini geliştirmişler. Bu teknoloji sayesinde sınırları aşarak IPv4'ün iki katı olarak bir ip adress'i kullanabileceğiz. İşte NAT burada devreye girer. Modemi her açıp kapatmamızda ip adressimizin yenilendiğini öğreniriz. Bu ip adress'imiz NAT sayesinde olmaktadır. NAT sayesinde her kullanıcı dönüşümlü olarak ip adress'i alabilmektedir.

## NAT Çeşitleri

