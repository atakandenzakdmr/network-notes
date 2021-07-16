# Classification of Routing Protocols

Yönlendiriciler yönlendirme işlemini statik ve dinamik yönlendirme olarak iki farklı şekilde yapmaktadır.

Statik yönlendirme: Yönlendirme tablosu girişi el ile yapılandırılmış ve ağ topolojisindeki değişiklerden etkilenmeyen yönlendirmeye statik yönlendirme denir. Statik yönlendirme küçük ağlar için iyi çalışabilmektedir.

Dinamik yönlendirme: Ağ topolojisindeki değişiklilerde yönlendirme tablosu girişleri otomatik olarak güncellenebilen yönlendirmeye dinamik yönlendirme denir. Dinamik yönlendirme geniş ağlarda daha iyi sonuç verebilmekte ve ağ hataları daha kolay bulunabilmektedir.


Dinamik yönlendirmede kullanılan yönlendirme protokolleri, -iki ana gurupta- sınıflandırılabilir.

1- Dış Yönlendirme Protokolleri: Yönlendirme işlemi bütün ağ ve geniş internet ağı arasında gerçekleşmektedir. Dış yönlendirme protokolleri, yönlendiricilerin durum ve bağlantıları hakkındaki değişiklikleri hızlı ve verimli bir şekilde haberleşen yönlendiricilere iletmek zorundadır.
Bu protokoller EGP (Exterior Gateway Protocol – Harici Geçit Protokol) olarak da adlandırılır ve temel olarak kullanılan EGP protokolüdür. EGP protokollerinin IPv6 versiyonları aşağıdaki gibi listelenebilir.

  • BGPv6

2- İç Yönlendirme Protokolleri: Yönlendirme işlemi bütün ağ içerisinde kendi aralarında gerçekleşir. İç yönlendirme protokolleri küçük internet içerisindeki yönlendiricilere, durum ve bağlantıları hakkında bilgi sağlar ve genellikle daha az karmaşık yönlendirme mimarisini destekler.
Bu protokoller IGP (Interior Gateway Protocol – Dahili Geçit Protokol) olarak da adlandırılır. IGP protokollerinin IPv6 versiyonları aşağıdaki gibi listelenebilir.

  • RIPng
  • EIGRPv6
  • OSPFv3
  • IS-ISv6


<img src= "https://github.com/atakandenzakdmr/network-notes/blob/dd4577a73bb989a49e09b5d8f681461c5d29a3e2/images/routing-protocols.PNG"> 
