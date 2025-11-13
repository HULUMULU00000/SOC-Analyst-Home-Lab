# Installation Steps — Wazuh Manager + Windows Agent

## 1. Wazuh Manager (Ubuntu)

1. Установил Wazuh Manager по официальной инструкции
2. Настроил репозитории и установил сервисы
3. Проверил статус:
   systemctl status wazuh-manager
4. Настроил доступ к веб-интерфейсу

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

