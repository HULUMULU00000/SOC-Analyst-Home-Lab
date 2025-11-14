# SOC Analyst Home Lab — Wazuh SIEM

Домашняя лаборатория, созданная для изучения работы SIEM на примере Wazuh, подключения Windows-агента и анализа событий безопасности (FIM — File Integrity Monitoring).

Цель проекта — получить практический опыт работы с SIEM, мониторингом и ведением отчётности:
- развернуть SIEM;
- подключить агент;
- проверить сбор телеметрии;
- отследить события безопасности;

---

# Архитектура лаборатории

Лаборатория состоит из:

- **Ubuntu (Wazuh Manager)** — центральный компонент SIEM  
- **Windows 10 (Wazuh Agent)** — источник событий  
- **Wazuh Dashboard** — визуализация и анализ событий  

![](https://github.com/user-attachments/assets/53725884-7eb9-44af-bb59-f848d446fe7f)
![](https://github.com/user-attachments/assets/d1b33e2d-dedd-4700-9c44-c4f3bff6a13a)

---

# Документация проекта

Проект структурирован на отдельные этапы:

### Установка и настройка компонентов  
Подробная установка Wazuh Manager, Windows Agent и регистрация агента:  
[installation_steps.md](installation/installation_steps.md)

### Пример использования: File Integrity Monitoring (FIM)   
Создание и удаление файлов, настройка FIM и события в Dashboard:  
[use_case_fim.md](use-case-fim/use_case_fim.md)

### Анализ событий FIM  
Краткий отчёт по обнаруженным событиям и выводы:  
[fim_event_analysis.md](reports/fim_event_analysis.md)

---

# Использованные технологии

- Wazuh SIEM  
- Ubuntu Linux  
- Windows 10  
- Wazuh Agent  
- File Integrity Monitoring  
- Работа с логами событий безопасности  
- Базовая диагностика и анализ телеметрии  

---

# Итог

Базовая SIEM-лаборатория успешно создана.  
Получена телеметрия от Windows-агента, FIM корректно фиксирует изменения файлов.
