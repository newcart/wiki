# GENEL İŞLEMLER


Pazaryeri modüllerinde
* app.module.ts dosyasında modül için gerekli temel yapılandırmalar yapılır. import edilecek hizmetler ayarlanır
* app.controller.ts dosyasında gateway den gelen istekler karşılanır ve bu istekler servise yönlendirilir
* @param body post işlemi ile gönderilen json datasına karşılık gelmektedir. HTTP Body dir

Her pazaryeri için üç servis olacak. Bu servisler isteklerin işlendiği yerdir. bu servis içinde ayrıca dto ve eventslar kullanılabilir.
* a. productService ürün işlemleri
* b. orderService sipariş işlemleri
* c. appService diğer işlemler

Tüm pazaryerleri servisleri aynı isimde metodlara sahiptir. hepsine aynı yapıda json ile istek göndeirilir. ve aynı yapıda geri dönüş alınır
## appService Metodları
```
testAccount: Api hesabını test etmek için
getMainCategories: Kök Kategori listesini almak için
getCategories: Kategori listesini almak için
getCategory: Bir kategorinin bilgilerini almak için
getCategorySpecs: Kategoride kullanılabilecek specsler için
```

POST "{pazaryeri}/test" pazaryeri api hesabını test etme hizmeti.
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}"
}
```
POST "{pazaryeri}/brand"
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}",
    "brand_code": "{brand_cod}"
}
```
POST "{pazaryeri}/brands"
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}"
}
```
POST "{pazaryeri}/maincategories"
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}"
}
```
POST "{pazaryeri}/categories"
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}"
}
```
POST "{pazaryeri}/category"
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}",
    "brand_code": "{category_code}",
}
```
POST "{pazaryeri}/category_specs"
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}",
    "brand_code": "{category_code}",
}
```
