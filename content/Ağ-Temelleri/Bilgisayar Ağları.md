#ağ 
[[Ağ Temelleri]]

## Devre Anahtarlamaları Ağlar
Devre anahtarlama yapılırken 3 aşama vardır.
- Devrenin kurulması
- Verinin aktarılması
- Devrenin sonlandırılması
	Örneğin telefon şebekesi
- Devre anahtarlama her bir arama için rezerve edilmiş bir devredir. Devre anahtarlamada yapılan arama için bir uçtan diğerine tüm kaynaklar rezerve edilir. 
**Nedenleri:** 
- Link'in bant genişliği, yani anahtar kapasitesi.
- Paylaşıma açık olmayan kaynaklar.
- Devre benzeri (garanti, performans) ve aramanın da yapılması gereklidir.
- Ağ kaynakları parçalara bölünür. Parçalar aramalarla paylaştırılır. Eğer arama o an için kanalı kullanmıyorsa kaynak parçası boşta bekler, kimse de kullanamaz. 
- Bant genişliği parçalara bölünürken frekans ya da zaman dikkate alınır.

640000 baytlık bir dosyayı A host'undan B hostuna devre anahtarlamalı bir ağ üzerinden göndermek ne kadar sürer.

Soru çözmek için;

1. Bütün linkler 1536 MBPS
2. Her bir link 24 bölmeli TDM kullanır.
3. Uçtan uca devre kurma süresi 500ms

1536/24=64 Her bir bölmenin kapasitesi.
640/64=10 Veri iletimi
10+0,5 = 10,5 sn (Toplam süre)

128.000 baytlık bir dosyayı A host'undan B host'una devre anahtarlamalı bir ağ üzerinden göndermk ne kadar sürer.
## Paket Anahtarlamalı Ağlar 
Paket anahtarlama, veriyi paket adı verilen küçük bloklara böler. Ve alıcıya ait bilgiyi her bir pakete yerleştirir. Ağ boyunca her biri her olası hedefe nasıl ulaşacağına dair bilgi içeren cihazlar yerleştirilmiştir. Bir paket cihazlardan birine ulaştığında paketi göndermek için ilgili cihaz bir yol seçer. Ve paket sonuç olarak doğru hedefe ulaşır. 

