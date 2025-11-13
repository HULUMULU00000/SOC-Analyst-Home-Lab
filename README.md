# SOC-Analyst-Home-Lab
Домашняя лаборатория построена для работы с SIEM и тестирования атак на пользователей
# Используемое оборудование:
1. Виртуальная машина Windows 10 (Wazuh_agent)
2. Виртуальная машина Linux_Ubuntu (Wazuh_manager)
3. Решение Wazuh_SIEM

Решение Wazuh для управления информацией о безопасности и событиями (SIEM) - это централизованная платформа для сбора и анализа телеметрии в режиме реального времени для обнаружения угроз и обеспечения соответствия требованиям. Wazuh собирает данные о событиях из различных источников, таких как конечные точки, сетевые устройства, облачные рабочие нагрузки и приложения, для обеспечения более широкого охвата безопасности.

# Общий вид лаборатории
<img width="1022" height="771" alt="image" src="https://github.com/user-attachments/assets/53725884-7eb9-44af-bb59-f848d446fe7f" />
<img width="1287" height="800" alt="image" src="https://github.com/user-attachments/assets/d1b33e2d-dedd-4700-9c44-c4f3bff6a13a" />

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

# Установка Wazuh_Agent (Windows)
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

# Что можно делать и видеть с помощью wazuh?
Нужно добавить в конфигурационный файл папку, которую надо мониторить. Допустим, в ней лежат нужные файлы
<img width="1024" height="771" alt="image" src="https://github.com/user-attachments/assets/34b5f2ef-b811-4035-bfd9-e2e07fd6c858" />

Создам в тестовой папке создам текстовый файл, а после удалю его
<img width="1027" height="772" alt="image" src="https://github.com/user-attachments/assets/317fe3d1-7fcf-45ad-89ea-51a097ff22de" />

В Менеджере отразилось создание файла
<img width="1718" height="948" alt="image" src="https://github.com/user-attachments/assets/ce1bbfb6-4b54-48c2-acf0-ad3b31d37ee0" />

Удаляю файл
<img width="1028" height="774" alt="image" src="https://github.com/user-attachments/assets/fe7c51f3-f1cf-4d40-833f-7d3df05271e8" />

Это отражается в Менеджере
<img width="1718" height="925" alt="image" src="https://github.com/user-attachments/assets/2da511c3-3d3c-4507-9850-aa3f7a464be3" />

# На этом создание самого начального уровня SIEM-лабораторной можно закончить. В дальнейшем она будет развиваться, что позволит проводить более подробный и обширный мониторинг



