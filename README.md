# django_stripe
Simple Payment Project  with Django and Stripe library.

**Запуск проекта:**
<div>
*1. Создаем виртуальное окружение;*
*2. Устанавливаем библиотеку Django;*
*3. Устанавливаем библиотеку Stripe;* 
<p>Всю документацию по библиотеки Stripe можно посмотреть здесь --></p>
    <p><a href="https://stripe.com/docs/checkout/quickstart">Stripe Official Docs</a></p>
</div>

*4. В папке проекта не забываем добавить в settings наш app.*

```
INSTALLED_APPS = [
    'products',
    ....
```

*Также нужно помнить про Secret_Key/Public_Key & Webhook, которые мы возьмем с официального сайта в Developers/API Keys* <a href='https://dashboard.stripe.com/test/apikeys'> API Kyes</a>
**В папке settings нашего проекта**
```
STRIPE_SECRET_KEY = 'Print your secret key here'
STRIPE_PUBLIC_KEY = 'Print your public key here'
STRIPE_WEBHOOK_SECRET = 'Print webhook here'

```

__*Также в папке settings*__
```
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [BASE_DIR / 'templates'],
```
'DIRS' = ['BASE / DIR 'templates'] - добавить в квадратные скобки `BASE / DIR 'templates'`
