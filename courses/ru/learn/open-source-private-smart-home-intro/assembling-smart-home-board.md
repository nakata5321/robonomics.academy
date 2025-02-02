---
title: "Сборка демонстрационного стенда умного дома"
lastUpdate: Wed May 10 2023 13:55:09 GMT+0400 (Samara Standard Time)
description: Вы научите собирать стенд умного дома!
metaOptions: [Learn]
defaultName: Introduction to open source solution for private smart homes
---

<LessonImages imageClasses="mb" src="smart-home-intro/spring-school-2023-smart-stand-intro.gif" />

## Панель умного дома

Эта панель предназначена для использования в качестве центрального устройства управления с наиболее часто используемыми переключателями и данными, отображаемыми на ней. Также есть возможность подключить домофон и использовать ее как внутренний монитор. По сути, в нашем случае это просто планшет под управлением ОС Android. Все, что вам нужно сделать, это обеспечить питание. Мы считаем, что эта панель должна быть установлена там, где вы бы разместили внутренний монитор.


<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmcbdAJqbwHAQ3NeyWQUwSoS4drDexa3AEs7HXuM1BrUT1', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-1.png" />


## Выключатель

Умные выключатели света более или менее похожи на обычные, за исключением того, что вместо переключателей используются нажимные кнопки. Кнопка возвращается в исходное положение после нажатия. Нет никакой разницы в подключении между обычным выключателем и умным: подключите нейтральный провод к N, провод питания к L и нагрузку к L1. После сборки выключателя для его сопряжения по ZigBee нажмите кнопку не менее 5 секунд.

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/Qmb138DiQWWBgowMj2fC9kmiGYh9WEeytteSkqumWCv2LB', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-2.png" />

В случае двухкнопочного выключателя (трех и более) единственное отличие заключается во второй (третьей, …) нагрузке.

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmZiStYZG4rmyNPXXmCXsVPm7witPpnNJMBzD8GtxedgPo', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-3.png" />

## Умная лампочка 

Умные лампочки, вероятно, самый простой способ попробовать что-то умное, вам даже не нужно быть электриком. Ими можно управлять дистанционно и менять яркость или цвет. Вы можете установить их вместе с умными выключателями или отдельно. Использование таких устройств может открыть целую страницу автоматизации в зависимости от вашего настроения или внешних условий! Новые лампочки готовы к подключению через ZigBee. Если вы не можете найти ее в устройствах, включите и выключите 5 раз.


<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmbiMHLJqnDpr1Whzvo6Y7zE33cQPuTs7furbt3JW2uiek', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-4.png" />

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmTzK4dY168HVgLvVBsRxR4M4vda55XC7pFhpW5kRexujQ', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-5.png" />

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmNZFpvVUavKc1Za9SeXqikrfySsfFHuVrkdzgbVB8um7T', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-6.png" />

## Умная розетка

Есть ряд «не умных» устройств, которые нам обычно нужно иногда включать и выключать. Если мы подключим такое устройство через умную розетку, мы сможем включать и выключать его в соответствии с нашими потребностями, расписанием или условиями. Также такие розетки могут отслеживать энергопотребление, поэтому у нас есть данные о том, сколько потребляет это устройство. Подключение довольно простое, для сопряжения смарт-розетки нажмите кнопку в течение 5 секунд.

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmRtmKXSv7csHLbKVuZkoA5Eb2zyTkEAbUxLYT6Qt1yxZH', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-7.png" />

## Выключатель для бойлера

Причина, по которой выключатель бойлера существует как специальное устройство, заключается в том, что он может выдерживать большую нагрузку. Обычно бойлеры потребляют 3кВтч и даже больше, поэтому обычные (даже умные) выключатели в данной ситуации не подходят. Выключатель для бойлера рассчитан на работу в этих условиях. Соединения и сопряжение почти такие же, как и для выключателя света.

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmNZyRtXXRYCrAQe6s6ZFJLXtUrH7SZHJC1Bt61kTrRX54', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-8.png" />

## Wifi/Zigbee термостат

Он выглядит как обычный термостат, но имеет возможность беспроводного управления. Возможны варианты: подключить систему отопления напрямую к термостату или разделить их. В последнем случае термостат сообщит нам режим (обогрев, охлаждение, вентиляция и т. д.) и температуру.

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmRjxo9EGUvQiMm84xvXCL6LfrQJYza71vmFsa9Zpy7qmz', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-9.png" />

## Переключатель для штор

Еще один специальный переключатель, на этот раз для штор. С технической точки зрения нет необходимости использовать только этот переключатель, мы могли бы использовать любой трехкнопочный переключатель и присоединить его к двигателю штор, но этот имеет специальные значки. Для сопряжения переключателя нажмите и удерживайте среднюю кнопку

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmRpEpZbyNkzby8Sk22Ymz59DbAcnty1B1osWc2kZr5FZ7', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-10.png" />

## Умный запорный кран

Выбирайте кран в соответствии с имеющимися у вас клапанами. Самый очевидный сценарий — совместить этот кран с датчиком протечки воды. Для сопряжения устройства удерживайте кнопку в течение 5 секунд

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmcjZcJ6P8Q5yUfSRx8R2mR4A7r2fi5bLs5uoUr3EAXLZs', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-11.png" />

## Датчик протечки воды

Довольно простое устройство, которое подает сигнал при соединении двух своих контактов. Вода проводит электричество и при наличии воды под датчиком его контакты замыкаются. Датчик работает от батарейки и обычно его хватает на 1-2 года. Чтобы подключить датчик через ZigBee, нажмите и удерживайте его кнопку некоторое время.

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmbgetJK1E8qQMcnBVREutpy8tKfbesqaxXiebjzpoyrdV', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-12.png" />

## Умный ИК пульт

Можно думать об этом устройстве как о пульте дистанционного управления телевизором… но умном! И это не ограничивается работой только с телевизорами. Если у вашего кондиционера есть пульт дистанционного управления, его можно заменить этим интеллектуальным. Чтобы соединить его, нажмите кнопку сброса на задней панели на некоторое время. Есть куча библиотек с готовыми командами, например [https://github.com/smartHomeHub/SmartIR](https://github.com/smartHomeHub/SmartIR). Все, что вам нужно сделать, это найти модель вашего телевизора или кондиционера.

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmVjj92fMLbA6QJ5QhnmiqBT1huD5b7xyfi3VadHFDYwtm', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-13.png" />

## Датчик открытия двери/окон

Еще один датчик, работающий от батареи, но помогающий в построении простой системы безопасности или подключении ее к источникам света и другим устройствам. Чтобы соединить его через ZigBee, вставьте иголку в отверстие и надавите на нее на некоторое время.

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmZyb66dKEqk9iCVKhaBk5ZKASi7dXdFSg2CBXY1fwuu5J', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-14.png" />

## Датчик движения

Так же, как датчик открытия, может использоваться в различных сценариях. Наиболее очевидными из них являются управление освещением или обнаружение движений, когда вас нет дома.

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmUA7TLg12pkhkbdGH6fwNDasU1kiyLHBJSutA2YG71Mka', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-15.png" />

## Датчик температуры и влажности

Хорошо знать, в каких условиях вы живете, правда? Этот датчик будет измерять температуру и влажность. Затем вы можете использовать эти данные для включения/выключения кондиционера или других систем отопления/охлаждения. Для сопряжения датчика есть кнопка сзади

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmayYFowfJVwQBVxPUSvi5inedqKzhyRZXp8fBUUayJnqH', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-16.png" />

## Камера видеонаблюдения

В конце концов, хорошо бы посмотреть, что происходит с вашим домом. Хорошей автоматизацией было бы подключение датчика движения к камере, чтобы у вас было 10-секундное видео при обнаружении движения.

<LessonVideo :videos="[{src: 'https://crustipfs.info/ipfs/QmX8nnDCgTx2kuwfAGv6B4orkEg4w6phtJtxSp44HfdD9T', type: 'webm'}]" cover="smart-home-intro/assembling-smart-home-board-17.png" />

## Стенд умного дома
Взгляните на результат [https://www.youtube.com/watch?v=B3er7bwtvkw](https://www.youtube.com/watch?v=B3er7bwtvkw )
И попробуйте сами [https://twitter.com/vadim_manaenko/status/1653777703718334469?s=20](https://twitter.com/vadim_manaenko/status/1653777703718334469?s=20)

