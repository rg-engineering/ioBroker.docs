---
translatedFrom: en
translatedWarning: Если вы хотите отредактировать этот документ, удалите поле «translationFrom», в противном случае этот документ будет снова автоматически переведен
editLink: https://github.com/ioBroker/ioBroker.docs/edit/master/docs/ru/adapterref/iobroker.fb-checkpresence/README.md
title: без заголовка
hash: sz5GEfBmsI/P9oIGCuaFT9qb3UogJ83YDErrfMQlPYg=
---
![Количество установок](http://iobroker.live/badges/fb-checkpresence-stable.svg)
![Версия NPM](http://img.shields.io/npm/v/iobroker.fb-checkpresence.svg)
![Загрузки](https://img.shields.io/npm/dm/iobroker.fb-checkpresence.svg)
![Статус зависимости](https://img.shields.io/david/afuerhoff/iobroker.fb-checkpresence.svg)
![Известные уязвимости](https://snyk.io/test/github/afuerhoff/ioBroker.fb-checkpresence/badge.svg)
![НПМ](https://nodei.co/npm/iobroker.fb-checkpresence.png?downloads=true)
![Трэвис-Си](http://img.shields.io/travis/afuerhoff/ioBroker.fb-checkpresence/master.svg)
![AppVeyor](https://ci.appveyor.com/api/projects/status/github/afuerhoff/ioBroker.fb-checkpresence?branch=master&svg=true)

<h1><img src="admin/fb-checkpresence.png" width="64"/>ioBroker.fb-checkpresence</h1>

## Адаптер fb-checkpresence для ioBroker
Адаптер проверяет присутствие членов семьи над фритцбоксом.
Вы должны указать имя члена семьи и mac-адрес (или ip-адрес) используемого устройства.
Комментарий не является обязательным, и вы можете включить или отключить члена семьи.
Точка данных основана на имени члена.

### Предварительные условия адаптера
Для правильной работы вам необходимо установить адаптер истории. Вы можете выбрать один из следующих адаптеров:

* История
* SQL
* InfluxDB

## Используемое устройство
Для этого адаптера используется AVM Fritzbox. Здесь вы можете найти информацию о Fritzbox https://avm.de/produkte/fritzbox/.
Сервисы fritzbox используются по протоколу TR-064.

### Условия Fritzbox
Используемый интерфейс TR-064 от fritzbox описан здесь: https://avm.de/service/schnittstellen/.
Используются следующие услуги и действия TR-064:

* Хосты: 1 - X_AVM-DE_GetHostListPath (поддерживается с 2017-01-09)
* Хосты: 1 - X_AVM-DE_GetMeshListPath
* Хосты: 1 - GetSpecificHostEntry
* Хосты: 1 - X_AVM-DE_GetSpecificHostEntryByIP (поддерживается с 18 мая 2016 г.)
* DeviceInfo: 1 - GetSecurityPort
* DeviceInfo: 1 - GetInfo
* WANPPPConnection: 1 - GetInfo
* WANIPConnection: 1 - GetInfo
* WLANConfiguration3 - SetEnable
* WLANConfiguration3 - GetInfo
* X_AVM-DE_HostFilter - DisallowWANAccessByIP
* X_AVM-DE_HostFilter - GetWANAccessByIP
* DeviceConfig: 1 - перезагрузка

По умолчанию интерфейс TR-064 не активирован. Однако это можно легко изменить через веб-интерфейс FritzBox. Для этого войдите в свой FritzBox и убедитесь, что режим эксперта активирован.
Затем вы найдете ниже «Домашняя сеть» Обзор домашней сети »Настройки сети» пункт «Разрешить доступ для приложений». Здесь вам нужно установить флажок, а затем перезапустить FritzBox один раз.

Подсказка: после изменения параметров не забудьте перезапустить Fritzbox!<img src="doc/access_settings_network.JPG"/>

## Диалог конфигурации
### Генеральный
Значения конфигурации проверены, и можно сохранить только правильные значения. В противном случае кнопка сохранения неактивна.

### IP-адрес, пользователь и пароль Fritzbox
Конфигурация ip-адреса, пользователя и пароля необходима для получения данных устройства из fritzbox.
Следовательно, пользователь должен быть создан в fritzbox. Это требуется для более новой версии прошивки (> = 7.25) fritzbox. См. Здесь информацию: https://avm.de/fileadmin/user_upload/Global/Service/Schnittstellen/Empfehlungen%20zur%20Benutzerfu%CC%88hrung%20bei%20der%20Anmeldung%20an%20einer%20FRITZ%.1Box. Пароль зашифрован и не был сохранен в виде открытого текста. Имя пользователя и пароль могут состоять максимум из 32 символов. См. Информацию: https://service.avm.de/help/de/FRITZ-Box-Fon-WLAN-7490/014/hilfe_zeichen_fuer_kennwoerter#:~:text=Namen%20f%C3%BCr%20Benutzer,Kennwortfeld%20darf % 20nicht% 20leer% 20sein.

### Параметр SSL
В некоторых случаях адаптер не мог подключиться к fritzbox. Может помочь отключить эту опцию.
В этом случае адаптер пытается подключиться без https.

### Интервал
У вас есть отдельные интервалы для членов семьи и устройств Fritzbox.
Интервал для устройств Fritzbox можно настроить от 1 до 59 минут. Обычно значение от 1 до 5 минут является оптимальным интервалом для чтения данных fritzbox. Члены семьи могут быть настроены от 10 до 600. Каждый новый цикл начинается, если предыдущий цикл завершен.

### Адаптер истории
По адаптеру истории вычисляются некоторые значения. Вы можете выбрать, будет ли использоваться история, sql или адаптер infxdb для этих вычислений. Адаптер истории должен быть установлен предварительно, а затем его можно будет выбрать в диалоговом окне конфигурации.
Если конфигурация истории отключена, то вычисление некоторых значений не может быть выполнено.

### Формат даты
Параметры маски формата даты описаны на этой веб-странице: https://www.npmjs.com/package/dateformat.
Маска формата используется для форматирования объектов таблиц html и json.

### Создание FB устройств
Если этот параметр отмечен, объекты создаются для каждого устройства в списке устройств Fritzbox.
Если этот параметр отключен, информация о сетке также отключена.

### Ресинхронизация объектов устройства FB
Если этот флажок установлен, объект устройства FB повторно синхронизируется со списком устройств Fritzbox.

### Создание информации о сетке
Этот параметр можно проверить, если создание устройств FB разрешено. Если этот флажок установлен, объекты сетки создаются для каждого устройства в списке устройств Fritzbox.

### Настройки членов семьи
Для настроенного члена семьи вы должны ввести Имя, MAC- или IP-адрес, комментарий и указать, включен ли член для расчета. Для каждого члена адаптер создает объекты данных и проверяет, присутствует ли член или нет.
Для получения информации о скорости в объектах необходимо выбрать опцию fb-devices.

### Настройки белого списка
В белый список вы можете вставить все известные устройства. Любые неизвестные устройства перечислены в объекте черного списка.
Если вы установите флажок в заголовке таблицы, будут выбраны все устройства.

## Особенности
### Проверка поддержки AVM
Функция проверяет наличие используемых функций fritzbox. Доступность регистрируется как информация. Если у вас есть проблемы, посмотрите, все ли функции установлены на true.

### Включение / выключение гостевой wlan
В гостевой папке вы можете установить для состояния wlan значение true или false, а затем гостевой wlan включится или выключится.

### Включение / выключение доступа в Интернет устройств Fritzbox
В папке FB-devices вы можете установить для отключенного состояния значение true или false, а доступ в Интернет для этого устройства будет заблокирован в Fritzbox.

### Получить гостей, черный список
В этой функции проверяется, вошел ли какой-либо пользователь в систему как гость. Также проверяется, нет ли какого-либо устройства в белом списке.
Эти устройства добавлены в черный список.

### Стань активным
Для каждого члена семьи вычисляется присутствие, даты приезда и отъезда, а также некоторые другие сведения, которые сохраняются в объекте члена, если выбран адаптер истории.

### Номер хоста, активные устройства
Количество устройств и количество активных берется из fritzbox.

## Объекты
### Наличие объекта Все
Если присутствуют все члены семьи, то объект верен.

### Наличие объекта
Если присутствует один член семьи, значит, объект верен.

### Объектные устройства
Все эти устройства перечислены в fritzbox.

### Объект activeDevices
Это количество всех активных устройств в fritzbox

### Объект html, json
Эти объекты представляют собой таблицы (json и html) с информацией о приходе и уходе всех членов семьи в них.

### Информация об объекте
Здесь перечислены сведения о последнем обновлении и состоянии подключения адаптера.

### Объект гость
Здесь перечислены сведения о количестве активных гостей и объекты таблицы с информацией об устройстве в ней.

### Черный список объектов
Здесь перечислены сведения о количестве неизвестных устройств и объекты таблицы с информацией о неизвестных устройствах.

### Объект member.present
Здесь вы найдете информацию о присутствии участника в текущий день и о том, как долго этот участник имел статус истинный с момента последнего изменения.

### Объект member.absent
Здесь вы найдете информацию об отсутствии участника в текущий день и о том, как долго участник находился в статусе false с момента последнего изменения.

### Объект member.comming, member.going
Здесь вы найдете информацию, когда член семьи прибывает или выходит из дома.

### Объект member.history, member.historyHtml
Здесь вы найдете информацию об истории текущего дня.

## Changelog
<!--
    Placeholder for the next version (at the beginning of the line):
    ## __WORK IN PROGRESS__
    * Did some changes
    * Did some more changes
-->

### 1.1.1 (2020-12-27)
* (afuerhoff) Configuration optimized
* (afuerhoff) Bugfix dateformat pattern
* (afuerhoff) SSL (https) workaround implemented
* (afuerhoff) Connection check optimized
* (afuerhoff) Documentation added
* (afuerhoff) Mesh handling optimized 

### 1.1.0 (2020-10-24)
* (afuerhoff) second interval for family members implemented
* (afuerhoff) mesh info added
* (afuerhoff) configuration validation added
* (afuerhoff) switch on, off guest wlan
* (afuerhoff) switch on, off internet access of devices 
* (afuerhoff) structural changes
* (afuerhoff) code optimization

### 1.0.4 (2020-06-28)
* (afuerhoff) bugfix json list and guest handling, new object guest.presence

### 1.0.3 (2020-05-26)
* (afuerhoff) bugfix checking mac or ip

### 1.0.2 (2020-05-24)
* (afuerhoff) error handling optimized
* (afuerhoff) external ip implemented
* (afuerhoff) check if mac or ip are listed in fritzbox

## License
MIT License

Copyright (c) 2019-2020 Achim Fürhoff <achim.fuerhoff@outlook.de>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.