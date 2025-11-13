# FIM Event Analysis Report

## Сценарий
На Windows агенте был создан тестовый файл, затем удалён.  
Wazuh FIM зафиксировал оба события.

---

## Событие создания файла
![FIM Create Event](https://github.com/user-attachments/assets/ce1bbfb6-4b54-48c2-acf0-ad3b31d37ee0)

---

## Событие удаления файла
![FIM Delete Event](https://github.com/user-attachments/assets/2da511c3-3d3c-4507-9850-aa3f7a464be3)

---

## Выводы
- система корректно фиксирует изменения файлов  
- агент передаёт события на менеджер  
- дашборд отображает полную информацию о модификации  
