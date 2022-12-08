# wiki
Address ve Deiğer Endpointler için endpointler
## COUNTRY
~~~
GET - {{SERVER}}/address/country //Servis hakkında genel bilgi dönmek için.
GET - {{SERVER}}/address/country/{id}
GET - {{SERVER}}/address/countries
POST - {{SERVER}}/address/country/{id}
PUT - {{SERVER}}/address/country/{id}
DELETE - {{SERVER}}/address/country/{id}

GET ÖRNEĞİ

Başarılı Response:
{
    "status": 1,
    "cached": 0,
    "message": "Ülke Bilgileri",
    "count": 1,
    "data": {
        "id": 4,
        "name": "Türkiye Cumhuriyeti",
        "code": "TR",
        "sort_order": 1,
        "status": 1
    },
    "errors": []
}

Başarısız Response:
{
    "status": 1,
    "cached": 0,
    "message": "Ülke Bulunamadı",
    "count": 1,
    "data": {},
    "errors": [
        "gönderdiğiniz kod bulunmamaktadır"
    ]
}

==============================================================
POST ÖRNEĞİ

Request
{
    "id": 1,
    "name": "TÜRKİYE",
    "code": "TR",
    "sort_order": "1",
    "status": 1
}

Kurallar:
'name'       => 'required|string|max:255',
'code'       => 'required|string|max:32|unique:countries',
'status'     => 'required|boolean'

Başarılı Response:
{
    "status": 1,
    "cached": 0,
    "message": "Ülke Bilgileri",
    "count": 1,
    "data": {
        "id": 4,
        "name": "Türkiye Cumhuriyeti",
        "code": "TR",
        "sort_order": 1,
        "status": 1
    },
    "errors": []
}

Başarısız Response:
{
    "status": 1,
    "cached": 0,
    "message": "Ülke Oluşturulamadı",
    "count": 1,
    "data": {
        "id": 4,
        "name": "Türkiye Cumhuriyeti",
        "code": "TR",
        "sort_order": 1,
        "status": 1
    },
    "errors": [
        "gönderdiğiniz kod kullanılmaktadır"
    ]
}
~~~
## CITY
~~~
GET - {{SERVER}}/address/city
GET - {{SERVER}}/address/city/{id}
GET - {{SERVER}}/address/cities/{country_id}
POST - {{SERVER}}/address/city/{id}
PUT - {{SERVER}}/address/city/{id}
DELETE - {{SERVER}}/address/city/{id}
~~~
## DISTRICT
~~~
GET - {{SERVER}}/address/district
GET - {{SERVER}}/address/district/{id}
GET - {{SERVER}}/address/districts/{city_id}
POST - {{SERVER}}/address/district/{id}
PUT - {{SERVER}}/address/district/{id}
DELETE - {{SERVER}}/address/district/{id}
~~~
## Anasayfa İçin Get Örnekleri
~~~
GET - {{SERVER}}/home/section_carousel1,2,3

section_carousel1,2,3:

'{
    "status": 1,
    "cached": 0,
    "message": "Carousel1 Bilgileri ",
    "count": 1,
    "title": "İndirime Girenler",
    "url": "hakkimizda",
    "product": [
    {
                "image": "assets/images/product-images/1.png",
                "oldPrice":52,
                "newPrice":48,
                "discountRate":50,
                "currency":"₺",
                "inStock":1,
                "brandName":"Baseus",
                "brandImage":"assets/images/brands/1.png"
                
   }, 
       {
                "image": "assets/images/product-images/1.png",
                "oldPrice":52,
                "newPrice":48,
                "discountRate":50,
                "currency":"₺",
                "inStock":1,
                "brandName":"Baseus",
                "brandImage":"assets/images/brands/1.png"
                
   }
     ],
    
    "errors": []
}'

=========================================================

GET - {{SERVER}}/home/section_grid1

section_grid1:

{
        "status": 1,
    "cached": 0,
    "message": "section_grid1 Bilgileri",
    "count": 1,
    "title": "Sonbahar Fırsatı",
    "image": "assets/images/vertical-banner.png",
    "url": "hakkimizda",
    "product": [
    {
                "image": "assets/images/product-images/1.png",
                "oldPrice":52,
                "newPrice":48,
                "discountRate":50,
                "currency":"₺",
                "inStock":1,
                "brandName":"Baseus",
                "brandImage":"assets/images/brands/1.png"
                
   }, 
       {
                "image": "assets/images/product-images/1.png",
                "oldPrice":52,
                "newPrice":48,
                "discountRate":50,
                "currency":"₺",
                "inStock":1,
                "brandName":"Baseus",
                "brandImage":"assets/images/brands/1.png"
               
   }
     ],
    
    "errors": []
}'




~~~
