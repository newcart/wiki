# Wiki

## Yeni Bir Mikroservis Açma
### Mikroservis Oluşturma
1. Öncelikle tamamen boş bir reposity oluşturunuz
2. Boş Repositiyi çalışma oratmınıza klonlayınız
3. ```$ nest new {mikroservis}``` komutunu çalıştırınız
4. ```$ cd {mikroservis}```{mikroservis} klasörüne gidiniz
5. ```$ nest generate resource db``` ile dto ları oluşturunuz
### Mikroservis Sınıfı Bileşenleri
* app.module.ts dosyasında mikroservis için gerekli temel yapılandırmalar yapılır. import edilecek hizmetler ayarlanır
* app.controller.ts dosyasında gateway den gelen istekler karşılanır ve bu istekler servise yönlendirilir
* @param body post işlemi ile gönderilen json datasına karşılık gelmektedir. HTTP Body dir
### Mikroservis Db Resource Bileşenleri
*  ./db/entity/db.entity.ts içerisinde servise ait veri tablosu yapılandırılır
```
import { Entity, Column, PrimaryGeneratedColumn, BeforeInsert, OneToMany, JoinColumn, OneToOne } from 'typeorm';

@Entity({ name: 'user', schema: 'public' })
export class UserEntity {
    @PrimaryGeneratedColumn()
    id: number;
    @Column()
    name: string;
    @Column()
    age: number;
    @Column({nullable:true})
    store: number;
    @Column({ unique: true })
    email: string;
}
```
## Pazaryerleri
Genel İşlemler: https://github.com/newcart/wiki/blob/main/pazaryeri/genel-islemler.md

Kategori İşlemleri: https://github.com/newcart/wiki/blob/main/pazaryeri/kategori.md

Marka İşlemleri: https://github.com/newcart/wiki/blob/main/pazaryeri/marka.md

Ürün İşlemleri: https://github.com/newcart/wiki/blob/main/pazaryeri/urun.md

Sipariş İşlemleri: https://github.com/newcart/wiki/blob/main/pazaryeri/siparis.md
