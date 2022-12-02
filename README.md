# wiki
Address ve Deiğer Endpointler için endpointler
## COUNTRY
~~~
GET - {{SERVER}}/address/country
GET - {{SERVER}}/address/country/{id}
GET - GET - {{SERVER}}/address/countries
POST - {{SERVER}}/address/country/{id}
PUT - {{SERVER}}/address/country/{id}
DELETE - {{SERVER}}/address/country/{id}

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
    "count": 0,
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
    "count": 0,
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
GET - GET - {{SERVER}}/address/cities/{country_id}
POST - {{SERVER}}/address/city/{id}
PUT - {{SERVER}}/address/city/{id}
DELETE - {{SERVER}}/address/city/{id}
~~~
## CITY
~~~
GET - {{SERVER}}/address/district
GET - {{SERVER}}/address/district/{id}
GET - GET - {{SERVER}}/address/districts/{city_id}
POST - {{SERVER}}/address/district/{id}
PUT - {{SERVER}}/address/district/{id}
DELETE - {{SERVER}}/address/district/{id}
~~~
