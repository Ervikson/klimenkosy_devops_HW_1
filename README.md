Task 1

https://hub.docker.com/repository/docker/ervikson/custom-nginx/general

Task 2

<img width="1688" height="551" alt="task_2_1" src="https://github.com/user-attachments/assets/8f6f25df-1c62-4756-b98e-cef2851fceb8" />

<img width="1688" height="551" alt="task_2_2" src="https://github.com/user-attachments/assets/d82b31a5-0a87-4ce6-822a-654a6c0a7013" />

Task 3

<img width="1693" height="1399" alt="task_3_1" src="https://github.com/user-attachments/assets/10157e72-795b-42c3-98e8-441599891f80" />

Контейнер остановился потому, что команда nginx -g 'daemon off;' была прервана сигналом SIGINT (Ctrl+C). Nginx завершил работу, и поскольку это был основной процесс контейнера, контейнер также остановился.

<img width="1689" height="649" alt="task_3_2" src="https://github.com/user-attachments/assets/873fd29b-2fe3-4307-ac69-82ff070998bb" />

Мы изменили порт прослушивания nginx внутри контейнера на 81, но снаружи контейнер все еще опубликован на порт 8080 хоста, который перенаправляет на порт 80 контейнера. Теперь nginx слушает порт 81, а не 80.

<img width="1689" height="649" alt="task_3_3" src="https://github.com/user-attachments/assets/5a8f05c9-988f-4d0b-945f-44705492a37c" />

Удаляем контейнер с флагом -f (force)

Task 4

<img width="1689" height="649" alt="task_4_1" src="https://github.com/user-attachments/assets/d88208a7-4919-4a04-9530-d8bb84d18897" />

<img width="1689" height="237" alt="task_4_centOS" src="https://github.com/user-attachments/assets/0a268889-c37b-436b-a75b-383bc5561232" />

<img width="1689" height="400" alt="task_4_Debian" src="https://github.com/user-attachments/assets/27655c97-570f-4a39-8560-4ff9429dc646" />

Task 5

<img width="1689" height="495" alt="task_5_1" src="https://github.com/user-attachments/assets/fdcd7647-c312-4b01-b8af-2a2ba7c562dc" />

При выполнении docker compose up -d используется файл compose.yaml т.к. исходя из документации он предпочтительней (preferred), то есть при наличии docker-compose.yaml и compose.yaml, будет использоваться второй, хотя оба файла поддерживаются.

<img width="1689" height="677" alt="task_5_2" src="https://github.com/user-attachments/assets/e003bf96-cc1a-41a4-83c2-77b6993cff16" />

Оба файла запущены

<img width="1689" height="602" alt="task_5_3" src="https://github.com/user-attachments/assets/6abd5a1e-7e66-4d6c-847d-ed93bbd00494" />

Залил образ в локальное регистри

Portainer:

<img width="1689" height="602" alt="task_5_portainer_1" src="https://github.com/user-attachments/assets/92d4659a-1456-4099-83be-64b0bb874f1c" />

<img width="1118" height="1259" alt="task_5_portainer_2" src="https://github.com/user-attachments/assets/a4fd240c-fd43-4a59-bd8c-c03639642803" />

<img width="1586" height="342" alt="task_5_6" src="https://github.com/user-attachments/assets/9ab52ab1-22d0-43bf-add1-960b0f05002a" />

Docker Compose предупреждает, что найден только один файл (docker-compose.yaml) из двух, которые ранее использовались в проекте. Это может привести к неожиданному поведению, так как часть сервисов может отсутствовать.

<img width="1586" height="220" alt="task_5_7" src="https://github.com/user-attachments/assets/953fdc24-4f05-4f7b-a030-19e9c38e92d5" />

Перезапускаем с флагом --force-recreate

<img width="1586" height="186" alt="task_5_8" src="https://github.com/user-attachments/assets/8c8b7c06-af72-4a4e-9f23-73b0dbabc26e" />

Гасим compose командой docker compose down

