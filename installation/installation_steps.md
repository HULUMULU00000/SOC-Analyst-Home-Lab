# Installation Steps — Wazuh Manager + Windows Agent

## 1. Wazuh Manager (Ubuntu)

# Установка Wazuh_Manager (Ubuntu)
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

Всё работает!
1. Установил Wazuh Manager по официальной инструкции
3. Настроил репозитории и установил сервисы
4. Проверил статус:systemctl status wazuh-manager
5. Настроил доступ к веб-интерфейсу

## 2. Windows Agent

1. Установил Wazuh Agent на Windows 10
2. Прописал адрес Wazuh Manager
3. Проверил подключение агента:
   - агент отображается в Dashboard
   - heartbeat поступает корректно

## 3. File Integrity Monitoring (FIM)

1. Включил мониторинг выбранных директорий
2. Создал и удалил тестовые файлы
3. Убедился, что события появились в Dashboard

