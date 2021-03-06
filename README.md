iPara - Nodejs Kütüphanesi
===================

iPara Nodejs Kütüphanesidir. iPara API'lerine çok hızlı bir şekilde bağlanmanızı sağlayan bu projeyi indirip hızlıca inceleyebilirsiniz.

## Önemli Notlar

* iPara ile ilgili fonksiyonların hepsi ./ipara/index.js dosyasındadır. Sadece index.js yi çekerek tüm fonksiyonlara ulaşabilirsiniz.
* Helpers fonksiyonların tamamı ./helpers/index.js dosyasındadır. Sadece index.js dosyasını çekerek tüm fonksiyonlara ulaşabilirsiniz.
* Router klasöründe api.js dosyasında örnek çalıştırmaları bulabilirsiniz.
* Servisleri kullanabilmek için iPara kurum başvuru aşamalarını tamamlamış olmanız gerekmektedir. Başvuru adımlarını tamamladıktan sonra kurum panelinizden alabileceğiniz public ve private key bilgileri ile servisleri kullanabilirsiniz.
* Entegrasyon işlemlerinde encoding “UTF-8” kullanılması gerekmektedir. Özellikle token parametresinden kaynaklı alınan hataların büyük çoğunluğu encoding problemlerinden kaynaklanmaktadır. Ek olarak XML dili için olan özel karakterlerin gönderiminde hata almamak için yine encoding yapılması gerekmektedir.
* Servis isteği yaparaken göndermiş olduğunuz alanların başında ve sonunda oluşabilecek boşluk alanlarını kaldırmanızı ( trim() ) önemle rica ederiz. Çünkü bu alanlar oluşacak hash sonuçlarını etkilemektedir.
* Entegrasyon dahilinde gönderilen input alanlarında, kart numarası alanı dışında kart numarası bilgisi gönderilmesi halinde işlem reddedilecektir.

## Önemli Uyarı:

iPara örnek projelerinin amacı, yazılım geliştiricilere iPara servislerine entegre olabilecek bir proje örneği sunmak ve entegrasyon adımlarının daha iyi anlaşılmasını sağlamaktır. Projeleri doğrudan canlı ortamınıza alarak kod değişimi yapmadan kullanmanız için desteğimiz bulunmamaktadır. **Projeyi bir eğitsel kaynak (tutorial) olarak kullanınız.**

## Kullanım

iPara servislerini kullanabilmek için [iPara'ya](https://www.ipara.com.tr) üye olmalısınız. Üye olduktan sonra iPara sizinle private ve public keylerinizi paylaşacaktır. Paylaşılan bu anahtarları kendi projenizde ilgili yerlere yazarak saklamanız ve kullanmanız gerekmektedir.

* Projeyi çalıştırmak için gerekli adımlar aşağıdaki gibidir:
  1) Güncel nodejs ve npm sürümünün bilgisayarınızda kurulu olması gerekmektedir. Nodejs v6 ve üstü, npm için ise v5 ve üstü versiyonların kullanıması önerilir.
  2) Dilediğiniz editor ile proje kodlarını okumak veya nodejs destekler IDE yardımı ile projeyi başlatmak mümkündür.
  3) Projenin asıl giriş dosyası "server.js" olarak tanımlanmıştır. Kullanım esnasında eğer IDE kullanmıyorsanız, Console(CLI) üzerinden "to/project/directory> node .\server.js" şeklindeki komut ile projeyi çalıştırabilirsiniz.
  4) Projenin bağlı dosyalarının kurulumu için "npm install" adımını unutmayınız. Bu projenin bağlı .js dosyalarını "node_modules" altında proje directory'ye eklemesini sağlayacaktır.
  5) Konsol içinde çıkan uyarılara göre projeyi ayarlayabilir ve gösterilen URL üzerinden deneyebilirsiniz.
  6) Projeyi doğru şekilde çalıştırmak için, sizlere iPara üyeliğiniz aşamasında verilmiş olan gizli ve açık anahtar bilginizi projenin ".\settings.js" dosyasında eklediğinizden emin olunuz.

Gerekli ortam değişkenleri (**environment variables**)

- IPARA_PRIVATE_KEY
- IPARA_PUBLIC_KEY
- IPARA_BASE_URL
- IPARA_MODE
- IPARA_HASH_STRING

olarak .\settings.js içinde bulunmaktadır.

>- IPARA_PRIVATE_KEY, IPARA_PUBLIC_KEY ve IPARA_BASE_URL bilgilerinin projeji çalıştırmadan önce girilmiş olması gerekmektedir, aksi taktirde program çalışmayacaktır.

## Kurulum

**Dikkat:** Proje dosyasını düzgün bir şekilde çalıştırabilmek için öncelikle cihazınızda Nodejs (v6+) ve Npm (v5+) kurulu olmalıdır. Daha önceki versyonlarda da kullanabilirsiniz ancak sorun yaşama ihtimaliniz olucaktır.

- **git clone https://github.com/ipara/ipara-nodejs.git**
- **cd ipara-nodejs**
- **npm install**
- **npm start**


## Test Kartları

Testleriniz sırasında aşağıdaki kart numaralarını ve diğer bilgileri kullanabilirsiniz.

| Sıra No 	| Kart Numarası    	| SKT   	| CVC 	|
|---------	|------------------	|-------	|-----	|
| 1       	| 4282209004348015 	| 12/22 	| 123 	|
| 2       	| 5571135571135575 	| 12/22 	| 000 	|
| 3       	| 4355084355084358 	| 12/22 	| 000 	|
| 4       	| 4662803300111364 	| 10/25 	| 000 	|
| 5       	| 5166570072166334 	| 10/25 	| 000 	|
| 6       	| 4022774022774026 	| 12/18 	| 000 	|
| 7       	| 5456165456165454 	| 12/18 	| 000 	|
| 8       	| 4531444531442283 	| 12/18 	| 000 	|
| 9       	| 5818775818772285 	| 12/18 	| 000 	|
| 10      	| 4508034508034509 	| 12/18 	| 000 	|
| 11      	| 5406675406675403 	| 12/18 	| 000 	|
| 12      	| 4025903160410013 	| 07/20 	| 123 	|
| 13      	| 5345632006230604 	| 03/19 	| 310 	|
| 14      	| 4282209027132016 	| 05/18 	| 358 	|
| 15      	| 4029400154245816 	| 03/24 	| 373 	|
| 16      	| 4029400184884303 	| 01/23 	| 378 	|

## Hash Hesaplama
iPara servislerine entegre olurken alınan hataların en sık karşılaşılanı hash değerinin doğru hesaplanmasıdır. Hash değeri her servise göre değişen verilerin yanyana eklenmesi ile oluşan değerin bir dizi işleme tabi tutulması ile oluşur.

Aşağıdaki adreste hash hesaplama ile ilgili detaylar yer almaktadır. Yine burada yer alan interaktif fonksiyon ile hesapladığınız hash fonksiyonlarını test edebilirsiniz.

[iPara Hash Hesaplama](https://dev.ipara.com.tr/#hashCalculate)

Her örnek projenin Helper sınıfı içinde hash hesaplama ile alakalı bir fonksiyon bulunmaktadır. Entegrasyon sırasıdna bu hazır fonksiyonları da kullanabilirsiniz.

## Canlı Ortama Geçiş

* Test ortamında kullandığınız statik verilerin canlı ortamda gerçek müşteri datasıyla değiştirildiğinden emin olun.
* Canlı ortamda yanlış, sabit data gönderilmediğinden emin olun. Gönderdiğiniz işlemlere ait verileri mutlaka size özel panelden görüntüleyin.
* Geliştirmeler tamamlandıktan sonra ödeme adımlarını, iPara test kartları ile tüm olası durumlar için test edin ve sonuçlarını görüntüleyin.
* iPara servislerinden dönen ve olabilecek tüm hataları karşılayacak ve müşteriye uygun cevabı gösterecek şekilde kodunuzu düzenleyin ve test edin.
* iPara hata kodları kullanıcı dostu mesajlar olup müşterinize gösterebilirsiniz.
* Hassas olmayan verileri ve servis yanıtlarını, hata çözümü ve olası sorunların çözümünde yardımcı olması açısından loglamaya dikkat edin.
* Canlı ortama geçiş sonrası ilk işlemleri kendi kredi kartlarınız ile deneyerek sonuçlarını size özel Kurum ekranlarından görüntüleyin. Sonuçların ve işlemlerin doğru tamamlandığından emin olun.

Sorularınız olması durumunda bize [Destek](http://dev.ipara.com.tr/Home/Support) üzerinden yazabilirsiniz.
