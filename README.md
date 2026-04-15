# 80-5-topshiriq
Block klasini yaratish
# Custom Blockchain Implementation (5-chi topshiriq)

Bu loyiha Node.js va `crypto-js` kutubxonasidan foydalanib yozilgan Blockchain arxitekturasining to'liq va soddalashtirilgan modelidir.

## Xususiyatlari:
1. **Block Klassi**: Har bir blok index, timestamp, ma'lumot (data), o'z hashi va oldingi blok hashi bilan yaratiladi.
2. **SHA-256 Kriptografiyasi**: Bloklarni xavfsiz himoyalash va yagona Hash (ID) yaratish maqsadida ishlatilgan.
3. **Proof-of-Work (Mining)**: Yangi blok yaratish jarayonida ma'lum mantiqiy qiyinlik (`difficulty: 3`) ga erishilmaguncha kompyuter hisob-kitob bajaradi.
4. **Validation (Zanjir tekshiruvi)**: O'tmishdagi ma'lumotlar o'zgarmasligini ta'minlovchi `isChainValid` funksiyasi yozilgan.
5. **Hacking Simulyatsiyasi**: Eski ma'lumotni o'zgartirish va hashlarni qalbaki yangilash samarasizligi namoyish qilingan (Hujum qaytarildi!).

## Ishga tushirish

Loyihani sinab ko'rish uchun quyidagi buyruqlarni terminalda yozing:

```bash
# 1. Kutubxonalarni yuklab olish
npm install

# 2. Asosiy dasturni ishga tushirish
node index.js
```
Dastur ishga tushganda konsolda bloklar muvaffaqiyatli qazilgani, JSON shaklidagi blokcheynning to'liq holatini va "Validatsiya" natijalarini seza olasiz.
