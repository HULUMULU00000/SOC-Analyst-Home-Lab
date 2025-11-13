# Installation Steps — Wazuh Manager + Windows Agent

## 1. Wazuh Manager (Ubuntu)

1. Установил Wazuh Manager по официальной инструкции
<img width="1022" height="771" alt="image" src="https://github.com/user-attachments/assets/53725884-7eb9-44af-bb59-f848d446fe7f" />
<img width="1287" height="800" alt="image" src="https://github.com/user-attachments/assets/d1b33e2d-dedd-4700-9c44-c4f3bff6a13a" />
3. Настроил репозитории и установил сервисы
4. Проверил статус:
   systemctl status wazuh-manager
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

