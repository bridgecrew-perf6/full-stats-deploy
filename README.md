## Порядок деплоя

1. Зайти на сервер по ssh
2. Стянуть бэкенд с гита
3. Создать БД
4. Запустить в фоне с помощью команды rails s -d
5. Изменить конфиг ngnix на тот, который лежит в файле config
6. Перезапустить nginx
7. Создать папку /var/www/full_stats/html
8. Сделать запрос на урл: api/v1/basketball/message, должен прийти правильный ответ
9. Перейти в папку фронта
10. Установить переменную окружения в правильное значение
11. Сбилдить фронт командо npm run build
12. Скопировать содержимое папки билд в целевую папку на вервере командой scp -r ./build/* "user"@IP:/var/www/full_stats/html
