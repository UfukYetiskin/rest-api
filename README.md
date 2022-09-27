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

![HTTP vs HTTPS](https://www.edhotels.com/wp-content/uploads/2020/04/Difference-Between-HTTP-and-HTTPS.png)

## Rest API Nedir?

Rest (Representational State Transfer), Server (Sunucu) ve Client (İstemci) arasında veri alışverişini sağlayan bir mimari modeldir. Rest API de Rest mimarisinin kullanımıyla web hizmetleri arasında veri alışverişini sağlayan uygulama ara birimidir.

### Rest API Nasıl Çalışır?

Rest, HTTP protokolünü kullanarak, URL adresleri üzerinden veri ve dosya alışverişi sağlayan yapıdır. Rest API ise Rest işlemini yapabilmek için kurgulanmış modüle verilen isimdir. Bu API(Modül) yardımıyla Rest işlemleri ve veri alışverişi yapılıyor.

Rest ile oluşturulan Server – Client bağlantısı sonucunda veri alışverişi belirli istekler sayesinde gerçekleşir. Rest sırasında kullanılan HTTP istekleri ve işlevleri aşağıdaki gibidir;

GET, veri listelemek ve görüntülemek için kullanılır.
POST, veri eklemek için kullanılan bir istektir.
DELETE, veri silmek için kullanılır.
PATCH, verinin bir kısmının güncellenmesi için kullanılan bir istektir.
PUT, belirli bir kaynaktaki verinin tamamının değiştirilmesi için kullanılan metodtur.


CONNECT - TRACE - OPTIONS - HEAD

SAFE Metotlar
GET – HEAD – OPTIONS : Sunucu “state” tarafında değişiklik oluşturmazlar. “Read-only” yapısındadırlar.

IDEMPOTENT Metotlar
GET – HEAD - OPTIONS – DELETE – PUT – TRACE : Tekrar durumunda sunucu state yapısında herhangi bir yan etki bırakmazlar. Safe metodlar, idempotent'tır.

Endpoint (Sorgu Adresi)
REST API kullanımında gönderilen istek ile verilen cevap için belirlenen buluşma noktasıdır.

Root(Base) /Path yapısından oluşur, isimler kullanılır, fiil ilgili HTTP metodu ile belirtilir. Dökümantasyon tarafından belirtilir.

![Rest API](https://cdn.hosting.com.tr/bilgi-bankasi/wp-content/uploads/2022/01/rest-api-nedir-nasil-calisir.jpg)


### Rest API Prensipleri

- İstemci - Sunucu : (Client - Server): İstemci isteği gönderen, sunucu da ilgili cevabı veren durumundadır. Birbirlerinin sorumluluk alanlarına girmezler. Birbirinden bağımsız programlama dilleri ve teknolojileri kullanılabilir.
- Tek Tip Arayüz : (Uniform Interface) : Aynı kaynağa yönelik olan tüm istekler, isteğin nereden geldiğinden bağımsız olarak aynı şekilde görünmelidir. Bu aynı zamanda istemci - sunucu bağımsızlığını da destekler. 4 temel zeölliği bulunmaktadır.
  - Kaynakların tanımlanması, bir kaynak için sunucuya yapılan istek benzersiz bir URI adresi ile tanımlanmalıdır.
    - http://example.com/users (GET)
    - http://example.com/users/11//posts (GET)
    - http://example.com//users//11//posts/5/comments (GET)
  - İstemci tarafında kaynağın değiştirilmesi.
  - İstemci ve sunucu birbirlerinin ihtiyaç duyduğu bilgilerin tamamını göndermelidir.
    - Sunucu > Content/Type (JSON, XML..) İstemci (doğru parser seçimi)
    - İstemci > Aynı URI farklı metodlar ve farklı sonuçlar (GET/ users ve POST/users)
  - Sunucu tarafından gönderilen cevap istenilen verininyanında bazı ek aksiyonlar da içerebilir.
- Durumsuzluk : (Statelessness)
    - State: Söz konusu veriyi- durumu belirtir, örneğin bir veritabanı için düşünürsek veritabanında o an için bulunan veridir. Bir React uygulamasını düşünürsek herhangi bir component'in o an ki durumu. Modal'ın açık veya kapalı olması, kullanıcının giriş, çıkış durumu gibi
    - Stateful (Durum bilgisi olan ) vs Stateless (Durum bilgisi olmayan)
  - İstemci tarafından gerçekleştirilen her istek birbirinden bağımsızdır ve sunucu bu isteklerin her birini bağımsız olarak değerlendirilir. Sunucu istemci tarafından kendisine gönderilen bilgileri tuutmamalıdır. Örneğin, bir isteğimiz kimlik doğrulama (Authentication) işlemi gerektiriyorsa ilgili tüm bilgiler (token vs...) istemci tarafından sunucuya devamlı olarak gönderilmelidir. 
- Önbelleklenebilir : (Cacheable) : Sunucu gelen isteklere verilen cevapların önbelleklenebilir olup olmadığını belirtmelidir. Örneğin "Cache-Control", "Expires" gibi HTTP başlıkları önbellek ile ilgili bilgiler taşır. 
- Katmanlı Sistem: (Layered System) : İstemci - sunucu arasındaki ilişki katmanlara ayrılabilir, ve bileşenler sadece ilişkili oldukları katmanlara karşı sorumlu olurlar. 
- İsteğe Bağlı Kod : (Code On Demand- Optional) : Sunucu, istemci tarafında istemcinin işlevini genişletecek ek kodlar gönderebilir. Bu özellik istemci tarafında yapılması gereken işlemleri hafifletir.


### Rest API'de Dönen HTTP Durum Kodları

1. HTTP 200 (OK), verilisteleme sonuçları 200 durum koduyla yanıtlanır.
2. HTTP 201 (Creates), veri eklendiği zaman 201 ile yanıt verilir.
3. HTTP 204 (No Content), veri silindiği zaman verilen yanıt 204'tür.
4. HTTP 400 (Bad Request), kayıt ekleme ve güncelleme talebinde gönderilen veri doğrulamadan geçemezse ve sorun yaşanırsa 400 yanıtı gönderilir.
5. HTTP 401 (Unauthorized), API yardımıyla yapılan Client-Server bağlantısı için bir login işlemi yapılması gerekirken login yapılmadıysa 401 yanıtı verilir.
6. HTTP 403 (Forbidden), 401'deki gibi Authorization işlemi gerekn yerde yetkisiz giriş yapılmaya çalışılırsa 403 yanıtı verilir.
7. HTTP 404 (Not Found), verinin talep edildiği URL adresi yok veya bahsedilen URL adresindeki veri geçersiz bir veri ise 404 yanıtı verilir.
8. HTTP 429 (Too Many Request), sunucunun belirli sayıda yapılacak iste sayısı kısıtlıdır ve bu kapasitenin üstünde bir istek geldiği zaman 429 yanıtı verilerek reddedilir.

## JSON Nedir?

Veri, en önemli varlıklardan biridir. Ancak çeşitli verilerle nasıl çalışılacağını bilmek artık daha da önemli hale geldi. Programcılar, geliştiriciler ve BT uzmanlarının doldurulmuş veri yapılarını herhangi bir dilden diğer diller ve platformlar tarafından tanınabilen formatlara aktarmaları gerekir. JavaScript Nesne Notasyonu (JSON), bunu mümkün kılan veri değişim biçimidir.

JSON; insanların okuyabileceği türde metin içermesi nedeniyle geliştiriciler arasında popüler bir veri formatı hale geldi. Bu format hafif, daha az kodlama gerektiriyor ve daha hızlı işleniyor.

*Veri depolamak veya veri iletmek için kullanılan metin tabanlı bir söz dizimi yapısıdır. Genellikle bir sunucu ve istemci arasında veri alışverişi için veya yazılımların genel ayarları için kullanılan bir formattır.*

### JSON Veri Tipleri

- String  : "Sample String", "test1234", "A"
- Number : 7, 3.2, -97.238
- Boolean : true, false
- Null : null
- Array : [2,3,4], , ["İstanbul", "Ankara", "İzmir"] Array içerisinde kullanılan değerler sıralı olarak
- Object : { "name": "İris", "age":23 } JSON nesneleri verileri key-value çiftleri olarak tanımlar.

Yukarıda görmüş olduğunuz veri tiplerinin tamamı tekil olarak uygun bir JSON formatı işlevini görür. Ancak tek bir 3, string veya true gibi ifadeler için ayrı bir .json uzantılı dosya oluşturmak mantıklı değildir. Bu nedenle JSON doayaları bir array, nesne ve/veya bunların içiçe geçmiş formlarından oluşur.

```
{
  "id":1,
  "title": "Matrix",
  "actors": ["Keanu Reeves", "Carrie Anne Moss"],
  "published_year": 1999,
  "genre": {
    "id": 6,
    "name": "Action"
  },
  isMarried : false,
  "rating": 7.9
}   
```

## XML Nedir?

XML (Genişletilebilir İşaretleme Dili), hem insanlar hem de bilgisayar sistemleri tarafından kolayca okunabilen belgeler oluşturmak için kullanılan bir işaretleme dilidir. W3C tarafından tanımlanan bir standarttır. Veri depolamanın yanında farklı sistemler arasında veri alışverişi yapmak amacıyla ara format görevi görmekte. SGML’nin basitleştirilmiş bir alt kümesidir.

```
<breakfast_menu>
  <food>
    <name>Belgian Waffles</name>
    <price>$5.95</price>
    <description>Two of our famous Belgian Waffles with plenty of real maple syrup</description>
    <calories>650</calories>
  </food>
</breakfast_menu>
```

Genel olarak ağaç yapısına (tree structure) sahiptir. Veriler açılış ve kapanış etiketlerinin içerisinde bulunur. Dıştaki etiket, içtekinin "parent"ı, içteki etiket ise dıştakinin "child"ı şeklinde düşünülür.

**JSON** formatının **XML** formatına göre en büyük avantajı, doğalında bir nesne modeline sahip olmasıdır. Bu özellik sayesinde birçok programlama dili JSON verileri daha kolay bir şekilde işleyebilir.

## Rest API Pratik

### Star Wars API (SWAPI)

SWAPI, Star Wars ekosistemine ait olan filmlerin, kahramanların, gezegenlerin vb bilgilerin sunulduğu ücretsiz bir API ortamıdır. İlk pratik çalışma olarak SWAPI seçmekteki yaklaşımın:

- API istekleri yapma alışkanlığı kazanmak
- Hazır bir API kullanımı ve ilgili dökümantasyonu incelemek
- Resource, EndPoint, Status Code gibi teorik olarak konuştuğumuz konuları pratik yapmak
- Postman kullanım alışkanlığı kazanmak

#### Yapılan İstekler

```
GET POPULAR MOVIES - GET : https://api.themoviedb.org/3/movie/popular
GET A MOVIE DETAIL - GET : https://api.themoviedb.org/3/movie/:movie_id
SEARCH FILM - GET : https://swapi.dev/api/films/?search="value"
```

##### Query Params

**?** karakteri api isteğinde sorgu karakteridir.. Buarada *value* değerine sahip veriyi api'dan almamızı sağlar. *seacrh* ise api'ın bize sağladığı bir erişim yoludur.

##### API KEY

API isteği yapacağımız sunucu için istemciye özel key isteniyor olabilir. İsteğin doğru dönmesi için bizlere bu api key oluşturulur ve url kısmına değil edilerek istek atılır.
