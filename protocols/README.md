# Classification of Routing Protocols

Yönlendiriciler yönlendirme işlemini statik ve dinamik yönlendirme olarak iki farklı şekilde yapmaktadır. </br>

#### Statik yönlendirme: Yönlendirme tablosu girişi el ile yapılandırılmış ve ağ topolojisindeki değişiklerden etkilenmeyen yönlendirmeye statik yönlendirme denir. Statik yönlendirme küçük ağlar için iyi çalışabilmektedir. </br>

#### Dinamik yönlendirme: Ağ topolojisindeki değişiklilerde yönlendirme tablosu girişleri otomatik olarak güncellenebilen yönlendirmeye dinamik yönlendirme denir. Dinamik yönlendirme geniş ağlarda daha iyi sonuç verebilmekte ve ağ hataları daha kolay bulunabilmektedir. </br>


Dinamik yönlendirmede kullanılan yönlendirme protokolleri, -iki ana gurupta- sınıflandırılabilir. </br>

##### 1- Dış Yönlendirme Protokolleri: Yönlendirme işlemi bütün ağ ve geniş internet ağı arasında gerçekleşmektedir. Dış yönlendirme protokolleri, yönlendiricilerin durum ve bağlantıları hakkındaki değişiklikleri hızlı ve verimli bir şekilde haberleşen yönlendiricilere iletmek zorundadır.</br> 
##### Bu protokoller EGP (Exterior Gateway Protocol – Harici Geçit Protokol) olarak da adlandırılır ve temel olarak kullanılan EGP protokolüdür. EGP protokollerinin IPv6 versiyonları aşağıdaki gibi listelenebilir. </br>

  • BGPv6

##### 2- İç Yönlendirme Protokolleri: Yönlendirme işlemi bütün ağ içerisinde kendi aralarında gerçekleşir. İç yönlendirme protokolleri küçük internet içerisindeki yönlendiricilere, durum ve bağlantıları hakkında bilgi sağlar ve genellikle daha az karmaşık yönlendirme mimarisini destekler. </br>
##### Bu protokoller IGP (Interior Gateway Protocol – Dahili Geçit Protokol) olarak da adlandırılır. IGP protokollerinin IPv6 versiyonları aşağıdaki gibi listelenebilir.
</br>
  <summary> <a href="https://github.com/atakandenzakdmr/network-notes/blob/4be186ff3a107ca5bbd08bf63482ef02611df0fc/protocols/RIPng/README.md" > RIPng </a> </summary> 
• EIGRPv6 </br>
• OSPFv3 </br>
• IS-ISv6


<img src= "https://github.com/atakandenzakdmr/network-notes/blob/dd4577a73bb989a49e09b5d8f681461c5d29a3e2/images/routing-protocols.PNG"> 
