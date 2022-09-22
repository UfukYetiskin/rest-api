# Rest-API

This repository contains what I learned about the REST API. This document will serve as a future reference.

## API (Application Programming Interface) Nedir? 

API'nin açılımı olan Application Programming Interface, Uygulama Programlama Arabirimi anlamına gelir. API'ler bağlamında Uygulama sözcüğü, ayrı bir işlevi bulunan her türlü yazılımı ifade eder. Arabirim, iki uygulama arasındaki hizmet sözleşmesi gibi düşünülebilir. Bu sözleşme, ikisinin istekler ve yanıtlar kullanarak birbiriyle nasıl iletişim kuracağını tanımlar. İlişkili API belgeleri, geliştiricilerin bu istek ve yanıtları nasıl yapılandırması gerektiğine dair bilgiler içerir.

API'ler, iki yazılım bileşeninin belirli tanımlar ve protokoller aracılığıyla birbiri ile iletişim kurmasına olanak tanıyan mekanizmalardır. Örneğin, meteoroloji müdürlüğünün yazılım sistemi, günlük hava durumu verilerini içerir. Telefonumuzdaki hava durumu uygulaması, API'ler aracılığıyla bu sistemle "konuşur" ve telefonumuzda bizlere günlük hava durumu güncellemeleri gösterir. 

### API'ler Nasıl Çalışır?

API mimarisi genellikle istemci ve sunucu bakımından açıklanır. İsteği gönderen uygulama istemci, yanıtı gönderen uygulamaya ise sunucu adı verilir. Yani hava durumu örneğinde, müdürlüğün hava durumu veritanabı bir sunucu iken, mobil uygulama ise bir istemcidir.

![Api Nedir?](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQZ1tv5OACJZEYaogH8BeHTpj_HCr9ovgJFYw&usqp=CAU)

## HTTP (Hyper Text Transfer Protocol) Nedir?

**HTTP**, bilginin sunucudan kullanıcıya nasıl ve ne şekilde aktarılacağını gösteren protokoldür. Tarayıcılar otomatik olarak bu protokolü aramalarda koyar. 

HTTP, kullanıcının bilgisayarı ve sunucu(server) arasındaki veri alışverişinin kurallarını belirler. Bu protokolü kullanmak için tarayıcı kullanılır. Google Chrome, Mozilla Firefox, Internet Explorer bu web tarayıcılarından bazılarıdır. Bu tarayıcılar yardımı ile herhangi bir istek gönderilir ve sunucu bu isteğe cevap verdiği vakit internet sitesinin verileri bizlere gelir. Yani internet sitesindeki verilere/bilgilere erişmiş oluruz.

### HTTP Nasıl Çalışır?

Kullanıcı girmek istediği sitenin adresini tarayıcı çubuğuna yazmasıyla **HTTP** yardımı ile sitenin sunucusuna bağlantı isteği gider. Sitenin sunucusu bu isteği kabul ederse kullanıcı siteye erişir, eğer kabul etmezse veya yanıt gelmezse kullancıya hata mesajı döner.

## HTTPS (Secure Hyper Text Transfer Protocol) Nedir? 

**HTTPS** aynı HTTP gibi bir protokoldür. Temelde iki protokol de aynı işi yapsa da HTTPS'de güvenlik öne çıkar. HTTP protokolüne **SSL** sertifikası eklenerek oluşur.  Kısacası internet sitelerinin metinlerle kurduğu bağlantının şifrelenmesidir.

HTTP, herhangi bir siteye bağlanmak istediğiniz zaman isteğinizi alıp, sunucuya iletir ve siteye girişinizi sağlar. HTTPS de aynı işlevi görür. Farkı ise HTTPS protokolü ile bir siteye bağlandığınız zaman güvenlik önlemleri daha ağırdır ve bilgileriniz asla başkaları tarafından okunamaz.

### HTTPS Nasıl Çalışır?

Herhangi bir tarayıcının adres çubuğuna girmek istediğiniz internet sitesinin adını yazdığınız zaman bu protokoller sayesinde sunucuya bir istek gider ve bu istek sonucunda siteye erişebiliriz. HTTP ve HTTPS temelde bu işlemi yapar.  **HTTPS** protokolünde SSL sertifikasının bulunduğunu söylemiştik. Bu sertifika **“Secure Socket Layer”** yani “Güvenli Giriş Katmanı” olarak bilinir ve Netscape firması tarafından geliştirilmiştir. Tüm web tarayıcıları ve sunucuları tarafından da tanınır. Bu sertifika sitenin güvenli olduğunu teyit eden bir sertifikadır.

HTTPS, özellikle ödeme alan web siteleri için uygun olan bir protokoldür.  Bu da günümüz teknolojisinde özellikle online alışveriş alışkanlığının artışı ile birlikte oldukça önemli bir konuma geldi. Online dolandırıcılığa karşı güçlü bir önlem olan HTTPS, tüm bankacılık işlemlerinin gerçekleştiği sitelerde ve online alışveriş sitelerinde bulunur ya da bulunması gerekir. HTTPS sertifikası bulunmayan sitelere karşı bilgi paylaşımı yaparken dikkat etmekte fayda vardır!