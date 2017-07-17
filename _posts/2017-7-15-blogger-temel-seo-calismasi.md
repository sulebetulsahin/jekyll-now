---
layout: post
title:  "Blogger İçin Temel Seo Çalışması"
date:   2017-7-15 15:48:00
categories: deneme
---

Google'un blog servisi olan blogger altyapısını kullanan bloglar için temel seo ayarları.

{::options parse_block_html="true" /}


### [Arama Sonuçlarında Görünürlük Sağlama](#aramasonuclari)
### [Search Console'a Ekleme](#search)
### [Başlık ve Açıklama Ekleme](#baslikaciklama)
### [Meta Açıklama ve Anahtar Kelime Ekleme](#metaaciklama)
### [Aramalarda "Yazı başlığı: Blog ismi" Olarak Çıkması](#yazibasligi)
### [Site Haritası Ekleme](#siteharitasi)
### [Robots.txt ve Özel Robot Etiketleri Düzenleme](#robots)
### [Google Analytics'e Ekleme](#googleanalytics)
### [Mobil Uyumluluk](#mobiluyumluluk)

<br>
<br>

<p align="center" style="font-size:30px;  font-weight:bold;"> 
[Arama Sonuçlarında Görünürlük Sağlama](){:name='aramasonuclari'}
</p>

Blogun hem blogger listesinde hem de arama motorlarında görünür olması için 
Ayarlar->Temel->Gizlilik sekmesine giderek gerekli ayarları “Evet” olarak işaretliyoruz. 
Ayarlar->Temel->Blog Okuyucuları sekmesini “Herkese Açık” olarak işaretliyoruz.


<p align="center" style="font-size:30px;  font-weight:bold;">
[Search Console'a Ekleme](){:name='search'}
</p>
Blogunuzu, Google Search Console'a ekleyerek Google arama sonuçlarında sitenizin nasıl göründüğünü, herhangi bir sorun olup olmadığını izleyebilirsiniz. Blogunuzu eklemek için Google hesabınızla oturum açtıktan sonra Google Search Console sayfasına gidin. Açılan sayfada sağ üst köşede yer alan “Özellik Ekle” bağlantısına tıklayarak gelen pencereye sitenizin domain adresini girip “Ekle” bağlantısına tıklayın. Ardından açılacak olan site doğrulama sayfasında uygun olan yöntemlerden biriyle doğrulama yapabilirsiniz. Blogger için “Alternatif Yöntemler” sekmesinde yer alan meta tag doğrulaması daha pratik olacaktır.


<p align="center" style="font-size:30px;  font-weight:bold;">
[Başlık ve Açıklama Ekleme](){:name='baslikaciklama'}
</p>
Google aramalarında görünecek olan başlık ve açıklama kısmını Ayarlar->Temel sekmesindenki ilgili alanlardan düzenliyoruz. Burada yazacağınız başlık ve açıklama aramalarda çıkacağı için ziyaretçiye blogunuzun içeriğiyle ilgili bilgi vermelidir. Başlık en fazla 70 karakter, açıklama ise en fazla 160 karakter olmalıdır. 


<p align="center" style="font-size:30px;  font-weight:bold;">
[Meta Açıklama ve Anahtar Kelime Ekleme](){:name='metaaciklama'}
</p>
Google aramalarında görünecek olan meta açıklamayı Ayarlar->Arama Tercihleri->Açıklama sekmesinden ekleyebilirsiniz. Buraya yazacağınız açıklama aramalarda çıkacağı için ziyaretçiye blogunuzun içeriğiyle ilgili bilgi vermelidir. En fazla 160 karakter olmalıdır. Meta açıklamayı aktif hale getirmek için Tema->HTML'yi düzenle sekmesinde <head></head> etiketleri arasına <b:include data='blog' name='all-head-content'/> kodunu ekliyoruz. Ardından sitenizin içeriğiyle ilgili 2 veya 3 anahtar kelime belirleyerek aynı şekilde <head></head> tagları arasına 
<meta content='anahtar kelime1, anahtar kelime2, anahtar kelime3' name='keywords'/> kodunu ekliyoruz. 

Yaptığınız değişiklikler aramalarda hemen çıkmayabilir. Blogunuzun aramalarda nasıl görüneceğine Meta Tag Analyzer aracını kullanarak bakabilirsiniz.


<p align="center" style="font-size:30px;  font-weight:bold;">
[Aramalarda "Yazı başlığı: Blog ismi" Olarak Çıkması](){:name='yazibasligi'}
</p>
Google aramalarda yazı başlığının ilk 66 karakterinin görüntülenmesine izin vermektedir. Bu yüzden aramalarda ziyaretçilerin odağını yazıya çevirmek için önce yazı başlığı sonra blog isminin görünmesi önemlidir. Aksi takdirde ziyaretçi yazı başlığını göremeyebilir. Arama sonuçlarında “Yazı başlığı: Blog ismi” şeklinde görünüm sağlamak için Tema->HTML'yi düzenle sekmesine giderek <title>...</title> kodunu bulup bu kodun yerine aşağıdaki kodları yapıştırıyoruz.

<b:if cond='data:blog.pageType == &quot;item&quot;'> 
<title><data:blog.pageName/> | <data:blog.title/></title> 
<b:else/> 
<title><data:blog.pageTitle/></title> 
</b:if> 


<p align="center" style="font-size:30px;  font-weight:bold;">
[Site Haritası Ekleme](){:name='siteharitasi'}
</p>
Site haritası yani sitemap, bir XML dosyası olup blogunuzda bulunan linkleri içerir. Google botlarının sitenizi bulmasını sağlar. Blogunuza sitemap eklemek için Google Search Console'a gidin. Sol taraftan daha önce eklemiş olduğunuz blogunuzu seçin. Sol tarafta yer alan 
Tarama->Site Haritaları sekmesine gidin. Sağ üstte yer alan “Site Haritası Ekleme/Test Etme” bağlantısına tıklayın. Açılan penceredeki alana blogunuzdaki yazı sayısına göre aşağıdaki kodları ekleyin ve gönderin.

Eğer sitenizde 500 den daha az yazı varsa : 
         atom.xml?redirect=false&start-index=1&max-results=500
Eğer 500 ile 1000 arasında ise 
atom.xml?redirect=false&start-index=1&max-results=500 
atom.xml?redirect=false&start-index=501&max-results=500
Eğer binden fazla ise : 
atom.xml?redirect=false&start-index=1&max-results=500 
atom.xml?redirect=false&start-index=501&max-results=500 
atom.xml?redirect=false&start-index=1001&max-results=500


<p align="center" style="font-size:30px;  font-weight:bold;">
[Robots.txt ve Özel Robot Etiketleri Düzenleme](){:name='robots'}
</p>
Robots.txt, blogunuzun arama motorlarında indexlenmesini veya indexlenmemesini istediğimiz durumların belirtildiği dosyadır. Dosyayı düzenlemek için Ayarlar->Arama Tercihleri sekmesine gidin. Robots.txt dosyasının yanındaki “Düzenle” bağlantısına tıklayın ve ilgili alana aşağıdaki kodları yapıştırın.

User-agent: Mediapartners-Google
Disallow:
User-agent: *Disallow: /search
Allow: /
Sitemap: http://www.blogisminiz.com/sitemap.xml

Ardından hemen altında yer alan Özel Robot etiketlerini düzenliyoruz. Standart olarak bir çok blog yazarının uyguladığı aşağıdaki seçimleri kullanabilirsiniz. Burada bilmeden farklı ayarlar yapmanız blogunuzun indexlenmemesine neden olabilir. Bu yüzden dikkatli olmalısınız.

“Anasayfa”, “Sayfaları Arşivle ve Arama Yap”, “Yayınlar ve Sayfalar için Varsayılan Ayar” alanlarının her birinde ayrı ayrı “all” ve “noodp” seçeneklerini işaretliyoruz.


<p align="center" style="font-size:30px;  font-weight:bold;">
[Google Analytics'e Ekleme](){:name='googleanalytics'}
</p>
Blogunuzu Google Analytics'e ekleyerek ziyaretçilerinizin tüm hareketlerini ve bilgilerini inceleyebilirsiniz. İlk olarak adres satırından Google Analytics'e giriş yapın. Sağ üst köşede yer alan “Bir Hesap Oluşturun” bağlantısına tıklayıp gelen sayfada “Kaydolun” bağlantısına tıklayın. Açılan sayfada ilgili alanları blogunuza uygun olarak doldurduktan sonra “İzleme Kimliği Edinin” bağlantısına tıklayın. Kullanım koşullarına kabul ettikten sonra karşınıza izleme kimliği sayfası gelecek. Bu sayfada yer alan izleme kodunu <script></script> etiketleri dahil kopyalarak
Tema->HTML'yi düzenle sekmesinde <head></head> etiketleri arasında yapıştırın. Artık blogunuzu kimlerin ziyaret ettiğini yakından izleyebilirsiniz!


<p align="center" style="font-size:30px;  font-weight:bold;">
[Mobil Uyumluluk](){:name='mobiluyumluluk'}
</p>
Blogger sitelerin avantajı default olarak mobil uyumlu bir yapıyla gelmektedir. Blogunuzun mobil uyumluluğunu test etmek için şu sayfayı kullanabilirsiniz.




Kaynaklar:
www.ehliblog.com
www.teknobeyin.com



