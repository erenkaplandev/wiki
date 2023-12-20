[[Ağ Temelleri]]
[[Uç Cihazlar(Hostlar) Arası Ağ Modeli]]
#ulaşımkatmanları
TCP/IP'ni ulaşım katmanında **TCP** ve **UDP** olmak üzere iki protokol tanımlıdır. TCP, bağlantılı düzene bağlı protokoldür. İki bilgisayar iletişim kurmadan önce iletişim kurma istek ve onaylarını birbirine yollarlar. Böylece iletişim konusunda anlaşmış olurlar. UDP ise bağlantısız düzenli bir protokoldür. İletişim başlamadan önce gönderici ve alıcı arasında bir amaçla yapılmasına gerek yoktur. Bu katman protokollerinden genelde TCP kullanılır. UDP ise kontrol amaçlı kullanılmaktadır. ==TCP ve UDP protokolleri bir üst katmandan gelen veriyi paketleyip alt katmana gönderirler. Eğer veri tek hamlede gönderilemeyecek kadar uzunsa alt katmana gönderilmeden önce paralara ayrılırlar ve her parçaya bir sıra numarası verilir.== 

### TCP 
TCP protokolü bir üst katmandan gelen veriyi uygun uzunlukta parçalara böler ve bir alt katmana gönderir. Ayrıca her bir parçaya TCP protokolü tarafında, alıcı tarafından **paketlerin sıralı birleşesi maksatıyla** parçalara bir sıra numarası verir. Eğer gönderilen paket alıcı tarafından hatalı olarak alındıysa bu protokol aracılığında hatalı olan paket alıcı tarafından tekrar gönderilir. İki cihaz arasında TCP iletişimi başlamadan önce bir oturum kurulması gerekmektedir.

### UDP 
UDP'nin farkı sorgulama ve sınama amaçlı küçük boyutlu verinin aktarılması için olmasıdır. Veri küçğk boyutlu olduğu için parçalanmaya gerek duymaz. Dolayısıyla UDP segmenti TCP segmentinden farklıdır. Başlık bilgisi daha az alan içermektedir. Gönderici ve alıcı port numaraları TCP bağlığındaki ile aynıdır. Uzunluk alanı veri ve başlığın boyunu gösterir. Kullanılması seçimlik olan hata sınama bitleri ise paketin hatadan arınmış olarak alınıp alınmadığını sınamak için kullanılmaktadır.