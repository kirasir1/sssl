# Практическая работа №4
## Вход в лабораторию
![изображение](https://github.com/user-attachments/assets/f45a39c7-5ae1-4a44-8832-9d0abf077a91)
## Выбранная база данных
![изображение](https://github.com/user-attachments/assets/57bae068-c9c0-4428-a4d1-d4e6d69fa8db)
## Анализ попавших в выборку адресов
![изображение](https://github.com/user-attachments/assets/e26a9b22-a105-47f9-96e2-4e346dd48fd4)
Это легитимная активность - данный пул адресов нужно добавить в вайтлист, он относится к сети Skype
![изображение](https://github.com/user-attachments/assets/7f33bc66-dd14-4f9b-b45e-34b730ba5c57)
Смотрим следующую цель
![изображение](https://github.com/user-attachments/assets/ec43d9e7-0cb3-4823-80c5-d9d4ad1d65e3)
Смотрим взаимосвязи узла
![изображение](https://github.com/user-attachments/assets/5f3cac19-8b4c-4862-91b8-20ccc5ae8116)
В VirusTotal внешний адрес связан с ntp пулами
![изображение](https://github.com/user-attachments/assets/1c3080d7-af33-4c5f-a1ba-d2c7b6180004)
Смотрим статистику по самым длинным сессиям
![изображение](https://github.com/user-attachments/assets/74246bb8-f914-445b-b6ec-ea624bf8ddcd)
## Анализ следующих логов
Импортирую логи
![изображение](https://github.com/user-attachments/assets/db08e79c-c43a-43c2-9835-910ceaf14cf7)
Вредоносный трафик - слишком много обращений по этому адресу, который в User Agent себя идентифицирует как Windows 7, данная версия ОС давно достигла EOL периода и не должна использоваться в безопасной инфраструктуре. Также IP не идентифицируется в FQDN.
![изображение](https://github.com/user-attachments/assets/62abeed6-24f4-47de-9a33-55000dfaa5e3)
Оставшиеся адреса резолвятся в инфраструктуру Microsoft:
![изображение](https://github.com/user-attachments/assets/a1388f23-5359-47fe-a720-982a03a46126)
В долгих подключениях такая картина:
![изображение](https://github.com/user-attachments/assets/fe43e75d-178a-4c79-b563-cdc8975cae0f)
VirusTotal показывает связи с каким-то сторонним сервисом:
![изображение](https://github.com/user-attachments/assets/9c494726-3f94-4e8a-b357-3e8a81790500)
Второй IP связан с инфраструктурой Microsoft.
## Анализ третьих логов
Во вкладке анализа DNS есть обращения к одному домену, но прямых подключений к нему 0
![изображение](https://github.com/user-attachments/assets/4f198439-71e1-42a7-b449-311a9908134e)
Смотрим все субдомены:
![изображение](https://github.com/user-attachments/assets/6b5df0ca-ef10-4398-bbcd-d28cd8879fe4)
Выглядит как потенциальная С2 атака через DNS.
## Анализ четвертых логов
Из подозрительных подключений находится это:
![изображение](https://github.com/user-attachments/assets/2eaed13d-eb44-431c-a858-6923ec009315)
FQDN, который не валидируется в потенциальной инфраструктуре Skype, плюс ко всему этому используется User Agent Internet Explorer.
Адрес обращается на хостинг Digital Ocean с достаточно длинным временем подключения:
![изображение](https://github.com/user-attachments/assets/feb2a0e4-4113-4bb8-8ea0-fe0f4a261290)
