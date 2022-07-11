# GENEL İŞLEMLER


Pazaryeri modüllerinde
* app.module.ts dosyasında modül için gerekli temel yapılandırmalar yapılır. import edilecek hizmetler ayarlanır
* app.controller.ts dosyasında gateway den gelen istekler karşılanır ve bu istekler servise yönlendirilir
* @param body post işlemi ile gönderilen json datasına karşılık gelmektedir. HTTP Body dir

Her pazaryeri için temel üç servis olacak. Bu servisler isteklerin işlendiği yerdir. bu servis içinde ayrıca ek servisler, dto ve eventslar kullanılabilir.
* a. productService ürün işlemleri
* b. orderService sipariş işlemleri
* c. appService diğer işlemler
* d. utilService tüm serviler için ortak işlevler, metodlar

Tüm pazaryerleri servisleri aynı isimde metodlara sahiptir. hepsine aynı yapıda json ile istek göndeirilir. ve aynı yapıda geri dönüş alınır
## appService Metodları
```
testAccount: Api hesabını test etmek için
postMainCategories: Kök Kategori listesini almak için
postCategories: Kategori listesini almak için
postCategory: Bir kategorinin bilgilerini almak için
postCategorySpecs: Kategoride kullanılabilecek specsler için
postBrands: Markalar listesini almak için
postBrand: Bir Markanın bilgilerini almak için
```

POST "{api_user_id}/{pazaryeri}/test" pazaryeri api hesabını test etme hizmeti.
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}"
}
```
POST "{api_user_id}/{pazaryeri}/brand"
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}",
    "brand_code": "{brand_cod}"
}
```
POST "{api_user_id}/{pazaryeri}/brands"
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}"
}
```
POST "{api_user_id}/{pazaryeri}/maincategories"
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}"
}
```
POST "{api_user_id}/{pazaryeri}/categories"
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}"
}
```
POST "{api_user_id}/{pazaryeri}/category"
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}",
    "brand_code": "{category_code}",
}
```
POST "{api_user_id}/{pazaryeri}/category_specs"
```
{
    "seller_id": "{seller_id}",
    "api_key": "{api_key}",
    "secret_key": "{secret_key}",
    "brand_code": "{category_code}",
}
```
