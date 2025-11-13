# Installation Steps — Wazuh Manager + Windows Agent

## 1. Wazuh Manager (Ubuntu)

1. Получение Wazuh GPG-Key с помощью консольной команды

curl -s https://packages.wazuh.com/key/GPG-KEY-WAZUH | sudo gpg --dearmor -o /usr/share/keyrings/wazuh-archive-keyring.gpg
2. Загрузка и запуск установочного скрипта Wazuh

curl -sO https://packages.wazuh.com/4.13/wazuh-install.sh && sudo bash ./wazuh-install.sh -a -i

● -a: Устанавливает все компоненты (менеджер, индексатор).

● -i: Запуск в интерактивном режиме

<img width="1287" height="799" alt="image" src="https://github.com/user-attachments/assets/29df01e5-355f-4807-bd4d-4eda8eef7043" />

3. Доступ к панели управления Wazuh

Система работает в веб-интерфейсе, поэтому надо зайти, указывая ip-адрес виртуальной машины

<img width="1720" height="871" alt="image" src="https://github.com/user-attachments/assets/ae7c08c9-ebc7-44a8-8608-88a450a8dd5c" />

<img width="1719" height="877" alt="image" src="https://github.com/user-attachments/assets/25320a8e-28f8-4377-8558-fc02d5665d7a" />

## 2. Windows Agent

На этом этапе всё просто: установка через графический интерфейс
<img width="1030" height="774" alt="image" src="https://github.com/user-attachments/assets/e9a37f16-0d33-4934-af89-ef75b3a5f89d" />
Всё работает!

# Регистрация Агента у Менеджера
Для этого нужно сгенерировать ключ агента с помощью команды sudo /var/ossec/bin/manage_agents
<img width="1716" height="930" alt="image" src="https://github.com/user-attachments/assets/a7488c4b-e7e5-4641-a302-ff70015477ed" />
Осталось скопировать ключ и вставить в интерфейс агента на Windows машине
<img width="1023" height="772" alt="image" src="https://github.com/user-attachments/assets/7e8273ec-82e1-47a1-8d15-4fe7a1003e5d" />
После добавления ip-адреса Менеджера видно, что система работает
<img width="1028" height="773" alt="image" src="https://github.com/user-attachments/assets/f459a329-44b7-46bc-8a31-1e6807e580f4" />
<img width="1719" height="950" alt="image" src="https://github.com/user-attachments/assets/da71facc-fbbc-40be-b1b3-ae243a896e32" />


## 3. File Integrity Monitoring (FIM)

1. Включил мониторинг выбранных директорий
2. Создал и удалил тестовые файлы
3. Убедился, что события появились в Dashboard

