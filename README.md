# Элехант + ESPHOME + Home Assistant
Считывание показаний газового счетчика Элехант, с помощью ESP32 (ESPHOME + Home Assistant)

Мне удалось найти несколько уже существующих способов проброса данных счетчика газа Элехант в НА,
1. через сервер с Home Assistant, у которого есть встроенный Bluetooth адаптер - https://github.com/SzenProgs/elehant_meter
2. через Bluetooth хаб, построенном на базе ESP32 - https://github.com/alutov/ESP32-R4sGate-for-Redmond
3. Прошивка для ESP32 для сбора данных со счетчиков Элехант СВД-15 - https://github.com/vooon/elehant-to-mqtt 

Мне же хотелось воспользоваться преимуществами нативной поддержки API Home Assistant в ESPHOME, без добавления в систему дополнительных компонентов, т.е. получать и отправлять данные пользуясь только интеграцией ESPHOME, с минимум дополнительных действий и отсутствием дополнительных "прокладок".

## Железо

1. ESP32-WROOM-32U, выбор был продиктован возможностью подключить внешнюю WiFi антенну , по сути данная конфигурация должна работать на любой ESP32 со встроенным Bluetooth адаптером.
2. Счетчик газа Элехант СГБ-4

## Установка
1. Необходимо установить дополнение ESPHome в HA.
2. Добавить код из confg.yaml в конфигурационный файл вашей платы.
3. Прошить ESP32.
