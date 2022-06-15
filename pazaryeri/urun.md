
# Ürün işlemleri
### POST "{pazaryeri}/product" postProduct bir ürün bilgisi çekme
```
{
    "seller_id": "108498",
    "api_key": "OtttIGZPJFwCqonagh2v",
    "secret_key": "8D5OhXAwAE1JxU1uJNIq",
    "prodcut_code": "35168-955",
}
```
### POST "{pazaryeri}/products" postProducts ürün listesi çekme
```
{
    "seller_id": "108498",
    "api_key": "OtttIGZPJFwCqonagh2v",
    "secret_key": "8D5OhXAwAE1JxU1uJNIq",
    "page": "1",
    "size": "50"
}
```
### postProductSave
```
{
    "seller_id": "",
    "api_key": "",
    "secret_key": "",
    "products": [
        {
            "product_seller_id": "",
            "product_markeplace_id": "",
            "product_sku": "",
            "barcode": "",
            "brand": "",
            "category": "",
            "name": "",
            "sub_title": "",
            "description": "",
            "prices": {
                "sale_price": "",
                "market_price": ""
            },
            "discount": {
                "discount_type": "",
                "discounted_price": "",
                "expired_date": ""
            },
            "shipping": {
                "shipping_type": "",
                "cargo_company": "",
                "dispatch_day": ""
            },
            "specs": [
                {
                    "spec_id": "",
                    "spec_name": "",
                    "spec_value_id": "",
                    "spec_value_name": ""
                }
            ],
            "variants": {
                "variant_markeplace_id": "",
                "variant_seller_sku": "",
                "variant_barcode": "",
                "variant_price": "",
                "variant_specs": [
                    {
                        "spec_id": "",
                        "spec_name": "",
                        "spec_value_id": "",
                        "spec_value_name": ""
                    }
                ]
            },
            "_n11_catalog_id": "",
            "_n11_category": ""
        }
    ]
}
```
