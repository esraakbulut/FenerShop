FenerShop — CSS Layout & Responsive Tasarım


KULLANIM
  1. index.html ve style.css aynı klasörde olmalı.
  2. index.html'e çift tıkla, tarayıcıda açılır.

  1. LAYOUT YÖNTEMLERİ — NEREDE KULLANDIM?

FLEXBOX kullandığım yerler:
  • Header (.header-inner)
    Logo sola, navigasyon sağa hizalamak için.
       justify-content: space-between ile yapıldı.

  • Ana Navigasyon (.main-nav)
    Linkleri yan yana dizmek için.

  • Filtre Satırı (.filtre-inner)
    Arama kutusu ve chip butonlarını yan yana
       tutmak, küçük ekranda alt alta kırmak için.
       flex-wrap: wrap ile responsive davranış sağlandı.

  • Chip Grubu (.chip-grup)
    Chip butonlarını yatay dizmek için.

  • Kart Alt Satırı (.kart-alt)
    Fiyat solda, buton sağda olacak şekilde
       hizalamak için. justify-content: space-between.

  • Footer (.footer-inner, .footer-nav)
    Telif metni ve linkleri karşılıklı hizalamak için.

CSS GRID kullandığım yer:
  • Ürün Kartları (.urunler-grid)
    8 kartı düzenli bir ızgaraya dizmek için.
       grid-template-columns: repeat(4, 1fr)
       Neden Grid? Çünkü 2 boyutlu (satır+sütun)
       hizalama gerekiyordu, Flex bunu daha zor yapar.

  2. BREAKPOINT'LER

  >= 1024px  →  4 sütun  (varsayılan, media query yok)
  600–1023px →  2 sütun
              @media (min-width: 600px) and (max-width: 1023px)

  < 600px    →  1 sütun
              @media (max-width: 599px)
              + Header menüsü logo altına düşer
                (flex-direction: column)
              + Filtre satırı alt alta kırılır
              + Footer ortaya hizalanır

  3. ÖĞRENDİKLERİM / ZORLANDIKLARIM

  1. Flex ile Grid'i birlikte kullanmak:
     İlk başta her şeye Flex uygulamaya çalıştım.
     Ürün kartlarını sıralayınca Grid'in çok daha
     uygun olduğunu anladım; Grid satır yüksekliklerini
     otomatik eşitledi, Flex'te bunu manuel yapmak
     gerekiyordu.

  2. position: sticky için z-index yönetimi:
     Header sticky yapınca filtre satırının üstüne
     biniyordu. Her sticky elemana ayrı z-index
     (header: 100, filtre: 90) vermek gerektiğini
     öğrendim.

  3. CSS değişkenleri kodun bakımını kolaylaştırdı:
     --primary rengini tek yerden değiştirince
     header, buton, rozet hepsi otomatik güncellendi.
     Önceden her rengi ayrı ayrı değiştiriyordum.


