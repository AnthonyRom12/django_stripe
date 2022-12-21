# Django_Stripe
__*Simple Payment Project  with Django and Stripe library.*__

**Запуск проекта:**


<div>
    <p>1. Создаем виртуальное окружение;</p>
    <p>2. Устанавливаем библиотеку Django;</p>
    <p>3. Устанавливаем библиотеку Stripe;</p>
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

*Также в папке settings*
```
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [BASE_DIR / 'templates'],
```
'DIRS' = ['BASE / DIR 'templates'] - добавить в квадратные скобки `BASE / DIR 'templates'`

__*Тоже добавляем settings*__
`EMAIL_BACKEND = 'django.core.mail.backend.console.EmailBackend'`

**Необходимо будет установить Stripe CLI**
<p><a href='https://stripe.com/docs/stripe-cli#install'> Stripe CLI Install Guide</a></p>
<p>Вот необходимая документация.</p>

__Если пользуетесь Pycharm не забывайте уставть данный знак в терминале перед запуском'.\'__

<p>запускаем Listen</p>

```
.\stripe listen --forward-to localhost:8000/webhooks/stripe/

```
**Запускаем сервер**

```
python manage.py runserver
```

**Ну вот и все 
:white_check_mark:**


# English version

**Launch of the project:**
<div>
    <p>1. Create a virtual environment;</p>
    <p>2. Installing the Django library;</p>
    <p>3. Installing the Stripe library;</p>
    <p>All Stripe library documentation can be found here --></p>
    <p><a href="https://stripe.com/docs/checkout/quickstart">Stripe Official Docs</a></p>
</div>

*four. In the project folder, do not forget to add our app.* to settings

```
INSTALLED_APPS = [
    'products',
    ....
```

*You also need to remember about Secret_Key/Public_Key & Webhook, which we will take from the official site in Developers/API Keys* <a href='https://dashboard.stripe.com/test/apikeys'> API Kyes</a>
**In the settings folder of our project**
```
STRIPE_SECRET_KEY = 'Print your secret key here'
STRIPE_PUBLIC_KEY = 'Print your public key here'
STRIPE_WEBHOOK_SECRET = 'Print webhook here'

```

__*Also in the settings folder*__
```
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [BASE_DIR / 'templates'],
```
'DIRS' = ['BASE / DIR 'templates'] - add in square brackets `BASE / DIR 'templates'`

__*Also add settings*__
`EMAIL_BACKEND = 'django.core.mail.backend.console.EmailBackend'`

**You will need to install Stripe CLI**
<p><a href='https://stripe.com/docs/stripe-cli#install'> Stripe CLI Install Guide</a></p>
<p>Here is the required documentation.</p>

__If you are using Pycharm don't forget to set this character in the terminal before running'.\'__

<p>run Listen</p>

```
.\stripe listen --forward-to localhost:8000/webhooks/stripe/

```
**Starting the server**

```
python manage.py runserver
```

**OK it's all over Now
:white_check_mark:**
