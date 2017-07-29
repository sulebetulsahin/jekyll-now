---
layout: post
title:  "İç SEO Çalışması"
date:   2017-7-29 15:48:00
categories: deneme
---

Site içi seo çalışması kullanıcılar ve arama motoru botları için yapılmaktadır. Yazılım ve tasarımla ilgili alanları içermekle beraber en önemli bölümü SEO uyumlu içeriktir. Site içi seo çalışmalarındaki amaç içerik kalitesini yükseltmek ve aramalarda üst sıralarda çıkmaktır.

{::options parse_block_html="true" /}


### [Canonical URL](#canonical)
### [W3C Standartlarına Uyumluluk](#w3c)
### [Kırık Link Bağlantılarını Bildirme](#kiriklink)
### [İlgi Çekici 404 Sayfası Hazırlama](#404)
### [Site Hızı](#hiz)
### [Tasarım](#tasarim)
### [Site İçi Bağlantılar](#siteici)
### [Site Dışı Bağlantılar](#sitedisi)
### [URL Yapısı](#url)
### [H Etiketleri Kullanımı](#hetiketi)
### [Başlık Seçimi ve Açıklama](#baslikaciklama)
### [SEO Uyumlu İçerik Hazırlama](#icerik)
### [Anahtar Kelime Kullanımı](#anahtar)
### [LSI](#lsi)
### [Resim Optimizasyonu](#resim)


<br>
<br>

<p align="center" style="font-size:30px; font-weight:bold;">
[Canonical URL](){:name='canonical'}
</p>

Aynı içeriğe birden fazla URL ile ulaşılması sitenin duplicate content yani kopya içerik olarak algılanmasına yol açmaktadır. Canonical URL kullanarak aynı içeriğe ait iki farklı link yapısından hangisinin arama motoru örümcekleri tarafından baz alınacağını belirtiriz. 

Örneğin; Aşağıdaki iki farklı link aynı içeriğe ulaşıyor olsun.
*Blogadi.com/anahtar1*
*Blogadi.com/anahtar2*

İlk linkten ulaşılmasını istiyoruz diyelim. *<head> </head>* etiketleri arasına aşağıdaki gibi Canonical etiketini kullanırız. 
`<link rel=”canonical” href=”blogadi.com/anahtar1” />`

Blogger alt yapılı bloglarda Canonical URL kullanmak için Tema->HTML'yi düzenle sekmesine geldikten sonra `expr:href="data:post.url"` kodunu bulup `expr:href="data:post.canonicalUrl"` olarak değiştirin.

<p align="center" style="font-size:30px; font-weight:bold;">
[W3C Standartlarına Uyumluluk](){:name='w3c'}
</p>

Tim Bernes Lee tarafından kurulan W3C, webin gelişmesinde etkili olmuştur. Bu oluşumla HTML çıktıları belirli bir standart haline gelmiştir. W3C hataları sitenin kalite puanını düşürmekte ve web tarayıcıları tarafından doğru okunmasını güçleştirerek siteyi yavaşlatmaktadır. Bu nedenle sitenizin W3C standartlarını desteklemesi önemlidir. Aynı zamanda Trustrank değerini de etkilemektedir. W3C Validator ile sitenizi test ederek, gelen uyarıları en aza indirip sitenizi W3C uyumlu hale getirebilirsiniz. Uyarıları düzeltmek için temel CSS bilgisine sahip olmanız yeterlidir.

Sık karşılaşılan bazı W3C hata çözümlerini aşağıda bulabilirsiniz.

Etiketleri iç içe kapatma: Etiketleri sırasıyla kapatmalısınız. 
Hatalı Kod: `<b><i> Etiketleri İç İçe Kapatmak </b></i>` 
Doğru Kod: `<b><i> Etiketleri İç İçe Kapatmak </i></b>`

XHTML etiketlerini kapatma: Bu etiketleri mutlaka kapatmalısınız.
Hatalı Kod: `<img src="resim.gif" alt="açıklama">` 
Doğru Kod: `<img src="resim.gif" alt="açıklama" />`

DOCTYPE'ı büyük harfle yazma: Bu tanımlamayı büyük harfle yazmalısınız.
Hatalı Kod: `<!doctype html public "-//w3c//dtd xhtml 1.0 strict//en" "http://www.w3.org/tr/xhtml1/dtd/xhtml1-strict.dtd" >`
Doğru Kod: `<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">`

Özellik değerlerini tırnak içerisinde girme: HTML ile bazı özellik değerlerini tırnaksız girebiliyorduk ancak XHTML ile mutlaka tırnak kullanmalıyız.
Hatalı Kod: `<td height=100%>` 
Doğru Kod: `<td height="100%">`

<p align="center" style="font-size:30px; font-weight:bold;">
[Kırık Link Bağlantılarını Bildirme](){:name='kiriklink'}
</p>
Websitenizde daha önce yer alan ve sonradan kaldırılan linklere, kırık link denilmektedir. 404 hatasıyla karşılaşılan sayfalar gibi. Kırık linklerin az olması veya hiç olmaması Google tarafından olumlu karşılanmaktadır. Websitenizde bulunan kırık linkleri Webmaster Tools panelinden “Sitenize Bağlantılar” sekmesinden öğrenebilirsiniz. Çalışmayan kırık linkler sitenizde buton, resim gibi herhangi bir bağlantıda bulunuyorsa kaldırın. Bu linkleri ilgili sayfalara(404 sayfası, kategori, yazı vb.) yönlendirin.

<p align="center" style="font-size:30px; font-weight:bold;">
[İlgi Çekici 404 Sayfası Hazırlama](){:name='404'}
</p>
Genelde website sahiplerinin çok fazla önemsemediği bu sayfaların kullanıcıya eğlenceli şekilde sunulması hemen çıkma oranını düşürecektir.

<p align="center" style="font-size:30px; font-weight:bold;">
[Site Hızı](){:name='hiz'}
</p>
Web site hızı geçmişte doğrudan SEO çalışmasını etkileyen bir unsur değilken artık Google tarafından içerik sıralamalarına etki eden kriterler arasında değerlendiriliyor. Bununla beraber ziyaretçiler hızlı açılan web sitelerinde daha uzun süre kalmaktadır. Site hızı ortalama 3 saniyenin altında olmalı. Web sitenizin hızlı yüklenmesi için gerekli çalışmalara Gtmetrix veya Google sayfa hızı aracını kullanarak başlayabilirsiniz. Gelen uyarıları dikkate alarak yüklenme hızınızı arttırabilirsiniz.

<p align="center" style="font-size:30px; font-weight:bold;">
[Tasarım](){:name='tasarim'}
</p>
Kullanıcı dostu, aranan içeriğe kolayca ulaşılan, hızlı navigasyon sunan web siteleri hem ziyaretçiler hem de arama motorları açısından önemlidir. Ayrıca sitenizin mobil uyumlu responsive tasarım desteklemesi son yıllarda Google'un önem verdiği ayrıntılardan birisi. Arama motorları eski kodları zararlı olarak görmektedir. Bu yüzden web sitenizin son teknolojiye göre kodlanmış olması avantaj sağlayacaktır. Örneğin güncel web standartlarıyla hazırlanmış olması, sitede yer alan şema, efekt, tablo gibi unsurların javascript yerine css ile kodlanmış olması. 

<p align="center" style="font-size:30px; font-weight:bold;">
[Site İçi Bağlantılar](){:name='siteici'}
</p>
Ziyaretçilerinizin sitenizde daha fazla zaman geçirmesi için site içi bağlantılar önemseyin. Birbiriyle alakalı olan yazılarda iç bağlantılar ile okuyucunun sitede kalma süresini arttırabilirsiniz. İç bağlantılar mutlaka yazının konusuyla alakalı olmalı. Her içerik için 2 ila 5 arasında bağlantı verebilirsiniz. 

<p align="center" style="font-size:30px; font-weight:bold;">
[Site Dışı Bağlantılar](){:name='sitedisi'}
</p>
Backlink almak site dışı SEO çalışmaları için önemliyken backlink vermek site içi SEO çalışmaları için önemlidir. Wikipedia gibi kaliteli ve otoriter sitelere dış bağlantılar vermek Google'un içeriğinizin neyle alakalı olduğunu anlamasını ve içeriğinizi değerli görmesini sağlar.

<p align="center" style="font-size:30px; font-weight:bold;">
[URL Yapısı](){:name='url'}
</p>
Google tarafından içerikler incelenirken yazı linklerinizdeki ilk 3-5 kelimeye önem verilmektedir. URL yapınızın ilk 5 kelimesini SEO uyumlu belirlemek için şunlara dikkat etmelisiniz:

URL yapınız çok fazla uzun olmamalı ve ilk 5 kelimesinde sıralamada çıkmak istediğiniz anahtar kelimeyi içermeli.
URL yapınızda tarih, rakam gibi ögeler yer almamalı. Örneğin; Blogadi.com/p=212 veya Blogadi.com/4/12/kategori/yazi-basligi

Örnek SEO uyumlu URL yapısı:
Blogadi.com/site-ici-seo veya Blogadi.com/seo/site-ici-seo

<p align="center" style="font-size:30px; font-weight:bold;">
[H Etiketleri Kullanımı](){:name='hetiketi'}
</p>
Site içi SEO'nun olmazsa olmazları arasında H etiketleri kullanımı yer alıyor. H etiketleri(h1,h2,h3..) başlıkları kodlamak için kullanılmaktadır. Bu etiketleri kullanılırken hiyerarşik sıralamaya özen gösterilmelidir. Örneğin h1 etiketinden önce h2 etiketi kullanılmamalıdır.
Her sayfada 1 tane h1 etiketi kullanılmalıdır. H1 etiketinde mutlaka anahtar kelimeniz yer almalı. Özellikle başlığın ilk bölümünde yer alması önemlidir. Genel olarak bir sayfada 1 tane h1, 4 tane h2 ve h3, 6 tane h5 etiketi bulunmalıdır.

<p align="center" style="font-size:30px; font-weight:bold;">
[Başlık Seçimi ve Açıklama](){:name='baslikaciklama'}
</p>
Ziyaretçilerinize ve arama motorlarına sitenizi tanıtan, neyle alakalı olduğunu anlamalarına yardımcı olan bölümdür. Anahtar kelimenize bu bölümde doğal bir biçimde yer verin. Başlık seçiminde kendinizi okuyucunun yerine koyun ve tıklanabilecek bir başlık seçin. Başlık uzunluğu en fazla 55 karakter olmalı. Açıklama seçiminiz sitenizi en iyi şekilde pazarlayacak cümleler içermeli. Açıklama uzunluğu 140-160 karakter arası olmalı. 

<p align="center" style="font-size:30px; font-weight:bold;">
[SEO Uyumlu İçerik Hazırlama](){:name='icerik'}
</p>
Ziyaretçilerin sitede kalmasını sağlayan en önemli unsur içeriktir. İçeriğiniz okuyucuyu sıkmayan, uzun, konuyu tümüyle anlatan ve bilgi verici nitelikte olmalıdır. İçerik uzunluğu en az 300 kelime olmalıdır. İçeriklerinizi konuyla alakalı resim ve videolar ile zenginleştirin. İç ve dış bağlantılar ile ziyaretçilerinizin daha uzun süre sitede kalmasını garantileyin. Uzun yazılar sıralamada çıkmak için avantaj sağlamaktadır. Ancak uzun yazayım derken okuyucunun dikkatini dağıtacak ve kısa sürede sıkılıp siteden çıkacağı nitelikte olmamalı. İçeriğinizin kaliteli olup olmadığını anlamak için aşağıdaki kriterleri dikkate alabilirsiniz;

Daha önce ziyaret edenlerin tekrar sitenize dönüş sağlaması
Sık kullanılanlara eklenme
Ziyaretçilerin sitede kalma süresi
Hemen çıkma oranı
Doğrudan aramalardan gelen ziyaretçi sayısı

<p align="center" style="font-size:30px; font-weight:bold;">
[Anahtar Kelime Kullanımı](){:name='anahtar'}
</p>
Bildiğiniz gibi arama motorlarından çeşitli kelimeler ile arama yaparak içeriklere ulaşıyoruz.  Yapılan araştırmalar kişilerin %75'inin konuyla ilgili cümle yerine kelimelerle arama yaptıklarını gösteriyor. Okuyucuların hangi kelimeleri aratarak içeriğinize ulaşmasını istiyorsanız içeriğinizde bu kelimeleri geçirmelisiniz. Anahtar kelime analizi için Google Keyword Tools'u kullanabilirsiniz. Aşırıya kaçmadan doğal olarak cümlenin akışı içerisinde anahtar kelimelerinizi kullanın. Anahtar kelimenizi içeriğinizdeki h2 etiketlerinde kullanın. İçeriğinizin ilk paragrafında mutlaka bir kere geçirin. Anahtar kelime dağılımı rekabeti yüksek kelimelerde içerik uzunluğuna göre %2-3 arasında rekabeti düşük kelimelerde içerik uzunluğuna göre %7-8 arasında olmalıdır.

<p align="center" style="font-size:30px; font-weight:bold;">
[LSI](){:name='lsi'}
</p>
Anahtar kelimenizle eş anlamlı, alakalı veya benzer diğer kelimelerdir. Gizli anlamsal indexleme olarak bilinmektedir. Bu kelimeleri belirlemek için odak anahtar kelimenizi Google'da aratın,  sayfanın en altında benzer kelimeler çıkacaktır. Buradaki kelimelerden alakalı olanları LSI olarak belirleyebilirsiniz. 

<p align="center" style="font-size:30px; font-weight:bold;">
[Resim Optimizasyonu](){:name='resim'}
</p>
Görsel aramalarda çıkmak için içeriklerinizdeki resimlerin optimizasyonunu yapmalısınız. Resimlere anahtar kelimenizin geçtiği isim, başlık ve alt etiketi ekleyerek neyle alakalı olduğunu arama motoru böceklerine anlatmalısınız. İsimlendirirken Türkçe karakter kullanmayın, boşluk yerine '-' işareti kullanın. İçeriğin okunma kısmının genişliğinden daha büyük boyutta resim yüklemeyin. Resimleri yüklemeden önce Photoshop benzeri programlar ile optimize edin. Bunları yapmanız page speed skorunuz ve site hızınız için önemlidir. 

Kaynaklar:
1.https://www.seoteknikleri.com
2.http://www.crmmedya.com
3.https://peakment.com
4.http://blog.112dijital.com
5.http://wpmavi.com
6.https://www.seocu.com
7.http://www.ehliblog.com
8.http://www.teknobeyin.com
9.https://www.seohocasi.com/



