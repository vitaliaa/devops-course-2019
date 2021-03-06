## Преамбула:
* Все ресурсы создаём в зоне *Ireland(eu-west-1)*
* Мы предоставил для ДЗ платные ресурсы которые не доступны при бесплатном использовании, по этому относитесь до задания серьезно и создавайте только те ресурсы которые **нужные для выполнения ДЗ!**
* Невыполения любого из условий ДЗ автоматически закрывает ваш PR

## Задание 1(Minimum):
* Создать EC2 ноду. Тип ноды: *t3a.micro*. Способ оплаты *spot*. 
* Название EC2 ноды и EC2 диска должно быть: *name.surname*
* На этой ноде запустить ДЗ №3. Веб сервер должен быть доступен из "мира"(работать в режиме 0.0.0.0).
* Добавить *ssh key* который лежит в корне папки.

### Результат выполеного задания №1:
* PR с текстовым файлом. Содержимое файла: IP адресс вашей ноды.
* Не использовать *IAM role*: *SystemAdministrator*
* Не удалять и не модифицировать чужие *EC2* ноды

### Tip's:
* Вам придётся разобраться из *IAM roles* и *EC2 Security groups*

## Задание 2(Recommended):
* Создать репозиторий в сервисе *ECR*. Имя репозитория должно быть: *name.surname*
* Сделать push в ново созданный репозиторий. 
* Выполненое *Задание 1.* (Docker контейнер должен работать с образа(**image**) который был "запушен" в ваш репозиторий)
* Создать **A** запись в сервисе *Route53* которая будет вести на вашу ноду. Имя записи должно иметь формат: *name-surname*
* Сделать SSL сертификат для вашего веб сервера. Настроить перенаправление с http на https.


### Результат выполеного задания №2:
* PR c текстовым файлом. Который содержит IP адресс вашей ноды и https адресс который ведёт на ваш веб-сервер.
* Невыполения любого условия из вышеперечисленого списка автоматически закрывает ваш PR
* Не удалять и не модифицировать чужие записи в *Route53*

### Tip's:
* Для создание SSL сертификата можно использовать сервис от *Letsencrypt*

## Задание 3(With asterisk):
* Выполненное заданиие 1 и 2.
* С помощь *aws cli* скачать картинку **cake.jpg** с *S3* корзины **ma-devops-bucket-with-image**. Добавить картинку на ваш веб-сервер.
* Картинка должна быть доступна по пути https://*name-surname*.ma-devops.mocintra.com/image/cake.jpg

### Tip's:
* Ключи доступа можно найти в бакете: *masteracademy_devops_access*

## Deadline: 22:00 15.12.2019
* 16.12.2019 в 21:00 все аккаунты и доступы к AWS удаляются и блокируються. 
