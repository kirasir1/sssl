# Практическая работа №1
Были созданы две виртуальные машины в одной подсети<br />
Машина 1:<br /><br />![280467404-57b715f2-ba07-4222-be21-f16b56cbed78-1](https://github.com/user-attachments/assets/83217035-b207-497a-b9f8-f7763799932b)
<br /><br />
Машина 2:<br /><br />![280467576-eeeb7897-d6bf-4847-b43c-a57fbd5c4af6](https://github.com/user-attachments/assets/ef483820-362b-4e3c-a85b-d0689593e576)
<br /><br />
Установлен rsyslog<br /><br />
![280468473-58189a6c-34cb-4818-bd73-f5a825e3d94a](https://github.com/user-attachments/assets/671b30d3-43fa-4572-9764-30110a0a9aab)
<br /><br />
На машине 2 раскомментированы строки в конфигурации для настройки серверной стороны по протоколу UDP<br /><br />
![280469100-afadb461-9d7a-4ef8-9f98-a0e11f1ae87d](https://github.com/user-attachments/assets/c6ec26fa-c960-4caf-b6d0-d710425517b5)
<br /><br />
После настройки директории для сохранения файлов перезагрузили сервис и проверили, открыт ли сокет на сервере:<br /><br />
![280469901-3b926466-397c-424d-86bc-ed95225d56b8](https://github.com/user-attachments/assets/200c177f-6866-4787-a638-0c6e2b9f28e3)
<br /><br />
Папка с логами доступна на сервере:<br /><br />
![280541384-b86fc4d0-d814-417d-9594-81452757c622](https://github.com/user-attachments/assets/17322a61-2af5-40fc-a085-dbeff294efe2)
<br /><br />
Устанавливаем Grafana Loki<br /><br />
![281906684-a72e6f42-91b9-430e-ae0e-e4cee6deec2a](https://github.com/user-attachments/assets/1c9561a9-238c-43da-8fdd-7821d7be95d7)
<br /><br />
На клиенте настроили promtail для отправки логов<br /><br />
![281906780-d3933da7-c479-40ab-bb8b-604c115aa352](https://github.com/user-attachments/assets/86c093eb-a878-4b25-9acc-c99d77a3e96f)
<br /><br />
Loki работает исправно<br /><br />
![281906780-d3933da7-c479-40ab-bb8b-604c115aa352-1](https://github.com/user-attachments/assets/fa724cd5-2159-45f2-9053-00c8b3574361)
<br /><br />
![281906798-ace526e6-ee7f-450f-bf6b-20a32f79e0b9](https://github.com/user-attachments/assets/6df5f359-1f8e-41a1-9fe8-327e8e6dbde2)
<br /><br />
На сервере поднимается сервер Signoz<br /><br />
![281906845-66c039b5-ad06-4b55-a693-df7d89d4f42c](https://github.com/user-attachments/assets/e924500a-a827-4213-9a7d-d8a8601fa755)
<br /><br />
![281906856-218ec804-89b3-492f-86ab-c821ddb0db08](https://github.com/user-attachments/assets/74364c52-b75d-48fc-ab92-6ef6f2b3a9be)
<br /><br />
На клиенте - приложение на nodejs из репозитория Signoz<br /><br />
![281906920-f6a20329-ee56-4501-9f62-1a6dfa88b031](https://github.com/user-attachments/assets/1c38ef6a-fbbc-4c69-a1db-915075393ce8)
<br /><br />
![281906934-e71724cd-cc5c-4ea5-bea6-08558a4c9b15](https://github.com/user-attachments/assets/7ac76e8f-47d2-41aa-996a-df74fbbb2a15)
<br /><br />
Телеметрия отображается в Signoz<br /><br />
![281906985-714a92ce-d8fc-470b-8359-8147bacd9860](https://github.com/user-attachments/assets/85b5351f-52dc-42e8-9da9-0c3169402be9)
<br /><br />
