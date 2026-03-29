# ERP Django - Umumiy ko'rsatmalar

ERP (Enterprise Resource Planning) - biznes jarayonlarini qamrab oluvchi dasturiy ta'minot bo'lib, barcha resurslar va faoliyatlarni birlashtiradi va boshqaradi.

## Loyihaning maqsadi

Ushbu loyiha, tashkilotlar uchun barcha jarayonlarni boshqarish imkonini beruvchi ERP tizimini yaratish maqsadida ishlab chiqilgan.

## Talablar

Loyihani ishga tushirish uchun quyidagi dasturiy ta'minotlar o'rnatilgan bo'lishi zarur:
- Python 3.8 yoki yangi versiya
- Django 3.1 yoki yangi versiya
- Django REST framework

## O'rnatish

1. **Repoziitoriyani klonlash**  
   `git clone https://github.com/abdumannon-rabbimqulov/ERP.django.git`

2. **Tizimga o'tish**  
   `cd ERP.django`

3. **Talab qilish**  
   `pip install -r requirements.txt`

## Dasturiy ta'minot tuzilmasi

Loyiha quyidagi asosiy papkalarga bo'lingan:
- **backend/** - Backend kodlari (Django)
- **frontend/** - Frontend kodi (agar mavjud bo'lsa)
- **migrations/** - Ma'lumotlar bazasidagi o'zgarishlarni boshqarish uchun migratsiyalar

## Ishga tushirish

Dasturiy ta'minotni ishga tushirish uchun quyidagi buyruqlarni bajaring:

```bash
python manage.py migrate  # Ma'lumotlar bazasini tayyorlash
python manage.py runserver  # Serverni ishga tushirish
```

Kodni ishga tushirgandan so'ng, brauzeringizda `http://127.0.0.1:8000` manziliga o'ting.

## Kod misoli

Django modellarini qanday yaratish

```python
from django.db import models

class Mahsulot(models.Model):
    nom = models.CharField(max_length=100)  # Mahsulot nomi
    narx = models.DecimalField(max_digits=10, decimal_places=2)  # Mahsulot narxi

    def __str__(self):
        return self.nom  # Mahsulot nomini qaytarish
```

## Yana ma'lumotlar

Ushbu loyiha haqida batafsil ma'lumot uchun [Django rasmiy hujjatiga](https://www.djangoproject.com/) murojaat qilishingiz mumkin.

## Mualliflar

Ushbu loyiha abdumannon-rabbimqulov tomonidan taqdim etilgan.

## Litsenziya

Loyihaning litsenziyasi [MIT](LICENSE) sifatida belgilanadi.