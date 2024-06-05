# Домашнее задание к занятию "`Домашнее задание к занятию 2 «Кластеризация и балансировка нагрузки»`" - `Бакулев Евгений`

### Задание 1
### Что нужно сделать:

1. Запустите два simple python сервера на своей виртуальной машине на разных портах
2. Установите и настройте HAProxy, воспользуйтесь материалами к лекции по ссылке
3. Настройте балансировку Round-robin на 4 уровне.
4. На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.

### Решение 1

[haproxy конфиг](https://github.com/garrkiss/cluster_and_balance/blob/main/files/haproxy.cfg)

![Скрин](https://github.com/garrkiss/cluster_and_balance/blob/main/img/%D0%A1%D0%BA%D1%80%D0%B8%D0%BD%D1%88%D0%BE%D1%82%2005.06.24_18.58.44.png)


### Задание 2
### Что нужно сделать:

Запустите три simple python сервера на своей виртуальной машине на разных портах
Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.

1. Запустите три simple python сервера на своей виртуальной машине на разных портах
2. Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
3. HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
4. На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.

### Решение 2

[Скрипт](https://github.com/garrkiss/disasterrecoverykepalived/blob/main/files/check.sh)

[Конфиг](https://github.com/garrkiss/disasterrecoverykepalived/blob/main/files/keepalived.conf)


Скриншот до смены имен файла 

![Скрин](https://github.com/garrkiss/disasterrecoverykepalived/blob/main/img/2%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5_%D0%B4%D0%BE%20%D1%81%D0%BC%D0%B5%D0%BD%D1%8B%20%D0%B8%D0%BC%D0%B5%D0%BD%D0%B8%20%D1%84%D0%B0%D0%B9%D0%BB%D0%B0.JPG)


Скриншот после смены имени файла. Видно что IP поменялся

![Скрин](https://github.com/garrkiss/disasterrecoverykepalived/blob/main/img/2%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5_%D0%BF%D0%BE%D1%81%D0%BB%D0%B5%20%D1%81%D0%BC%D0%B5%D0%BD%D1%8B%20%D0%B8%D0%BC%D0%B5%D0%BD%D0%B8%20%D1%84%D0%B0%D0%B9%D0%BB%D0%B0.JPG)
