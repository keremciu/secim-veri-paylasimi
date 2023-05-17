# secim-veri-paylasimi

OyVeÖtesi platformu API'ını kullanırken rate-limit'e takılmamak adına bu repoda bulunan JSON dosyalarını kullanabilirsiniz.

Şehir, İlçe, Mahalle şeklinde veriler sınıflandırılmış durumda.

Şehir = City
İlçe = District
Mahalle = Neighborhood

YSK sistemindeki okulların listesini `unique_school_list.json` dosyasından elde edebilirsiniz.

--

Soru ve öneriler için lütfen issue oluşturunuz.

--

Sıkça sorulan sorular:

1. Okul ID'si bu veri setinde bulunmuyor nasıl elde edebilirim?
- Elinizdeki YSK verisinde Şehir, İlçe, Mahalle ve Okul adı bulunuyor olmalı. unique_school_list.json YSK verisinde oluşturulmuştur. 

```
curl https://api-sonuc.oyveotesi.org/api/v1/cities/{city_id}/districts/{district_id}/neighborhoods/{neighborhood_id}/schools
```

Bu şekilde okul listesini elde edip, okul adı ile eşleştirerek Okul ID'sine erişebilirsiniz.