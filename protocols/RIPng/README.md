# RIPng


RIP, uzaklık vektör algoritması temelli 1988 yılında IETF tarafından standartlaştırılmış IPv4 ağları arasında yönlendirmeyi sağlamak amacıyla geliştirilmiş bir yönlendirme protokolüdür.
Bu protokol, atlama sayısına (hop count) bakarak hedef ve kaynak arasında en az kaç yönlendiriciden atlanacaksa o yolu yönlendirme yolu olarak tercih etmektedir.


RIP’in en büyük dezavantajı, diğer yollar arasındaki bant genişliği ve gecikme gibi faktörleri göz önünde bulundurmamasıdır. <br/>
#### RIP’in IPv6 yönlendirmede kullanılmak için RIPv2’nin geliştirilmiş versiyonu RIPng’dir. <br/>
RIPng, Ocak 1997’de RFC 2080 standardında tanımlanan ve uzaklık vektörü algoritması temelli yönlendirme algoritmasıdır.
Bu protokol, RIPv1 ve RIPv2’den IPv6 yönlendirmeyi desteklemek için geliştirilmiştir.
RIPng mesajlarını IPv6 adresi olan alıcı adresinin FF02::9 olduğu çoklu yayın adresine gönderir. 

#### Temel olarak bu protokolün nasıl çalıştığı aşağıda açıklanmıştır;

• Yönlendirici, yönlendirme bilgisini ve direk bağlı olduğu yönlendiricileri belirli zaman aralıklarında güncelleme mesajlarıyla göndermekte ve almaktadır. <br/>
• Yönlendirici direkt bağlı olduğu yönlendiriciden güncelleme mesajı aldığında, bu bilgiler doğrultusunda yönlendirme tablosunu güncellemektedir.

### RIPng özellikleri;
• IPv6 destekler, <br/> 
• Kimlik denetimi için Ipsec protokolünü kullanır, <br/>
• Yönlendiricinin her arayüzünde ayrı ayrı etkinleştirilir, <br/>
• Güncellemelerini FF02::9 ile gerçekleştirir.


### RIPng yönlendirme tablosunda, ulaşılabilir hedefler için her bir giriş en azından aşağıdaki bilgileri içermelidir
• Hedefin IPv6 öneki,<br/>
• Metrik değer: Hedef ile kayak yönlendirici arasındaki maliyet bilgisi, <br/>
• Sonraki yönlendiricinin IPv6 adres bilgisi (sonraki atlama vb.). Eğer kaynak yönlendirici direk bağlı ise bu bilgiye gerek yoktur, <br/>
• Yol değişim bayrağı: İzlenecek yolun değiştiğini gösteren bilgi, <br/>
• Zamanlayıcı: Yol bilgisinin gönderildiğini ve zaman aşımına uğramadığını gösteren bilgidir.

### RIPng yapılandırması aşağıdaki gibidir;
Router(config)#ipv6 unicast-routing  <br/>
Router(config)#interface [?] [?] <br/>
Router(config-if)#ipv6 rip [isim] enable <br/>
Router(config)#ipv6 unicast-routing <br/>
Router(config)#interface fa0/0 <br/>
Router(config-if)#ipv6 rip [isim] enable <br/> 
Router(config-if)#ip address 10.0.0.1 255.0.0.0 <br/>
Router(config-if)#no shutdown <br/>
Router(config-if)#exit  <br/>
Router(config)# <br/>

### Buradaki kodlar; <br/>
"ipv6 unicast-routing" IPv6 paketlerinin iletilmesini sağlar, <br/>
"interface fa0/0" Fast Ethernet port 0/0 tanımlanır, <br/>
"ipv6 rip msku enable" IPv6 yönlendirme işlemlerini msku işlem ismi ile etkinleştir. <br/> 
“no shutdown” hiçbir kapatma komutu arayüzü açmaz.  <br/>
“exit” genel yapılandırma moduna dönmek için çıkış komutu kullanılır. <br/>

#### RIPng, 
tıpkı eski RIP versiyonları gibi bir ortam için max 15 router desteklemektedir ancak yeni versiyonla birlikte farklı cihazları farklı domain ortamlarında tutarak max 15 hop durumundan siyrilmak mumkun. <br/> 
(Örnek senaryoda cihazların hepsi MSKU domaininde bulunacak).
