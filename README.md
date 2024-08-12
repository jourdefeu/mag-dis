# mag-dis

## Менеджер уязвимостей с открытым исходным кодом

Перед безопасностью стоят две сложные задачи: разработка интеллектуальных способов получения новой информации и отслеживание результатов для улучшения усилий по исправлению. С Faraday вы можете сосредоточиться на обнаружении уязвимостей, пока мы помогаем вам с остальным. Просто используйте его в своем терминале и организуйте свою работу на бегу. Faraday был создан для того, чтобы вы могли использовать преимущества доступных в сообществе инструментов по-настоящему многопользовательским способом.

Faraday агрегирует и нормализует данные, которые вы загружаете, позволяя исследовать их в различных визуализациях, полезных как для менеджеров, так и для аналитиков.
![image](https://github.com/user-attachments/assets/ea75d280-bd45-478d-a7d3-eef24a6aca68)
![image](https://github.com/user-attachments/assets/09891183-cf20-449a-8ec8-5192023dde7d)

## Установка

### Docker-compose

Самый простой способ запустить faraday — использовать наш docker-compose

$ wget https://raw.githubusercontent.com/infobyte/faraday/master/docker-compose.yaml
$ docker-compose up
Если вы хотите настроить, вы можете найти пример конфигурации здесь Ссылка

Докер
Сначала вам нужно запустить Postgres.

 $ docker run \
     -v $HOME/.faraday:/home/faraday/.faraday \
     -p 5985:5985 \
     -e PGSQL_USER='postgres_user' \
     -e PGSQL_HOST='postgres_ip' \
     -e PGSQL_PASSWD='postgres_password' \
     -e PGSQL_DBNAME='postgres_db_name' \
     faradaysec/faraday:latest
PyPi
$ pip3 install faradaysec
$ faraday-manage initdb
$ faraday-server
Двоичные пакеты (Debian/RPM)
Вы можете найти установщики на нашей странице релизов

$ sudo apt install faraday-server_amd64.deb
# Add your user to the faraday group
$ faraday-manage initdb
$ sudo systemctl start faraday-server
Добавьте пользователя в группу, а затем выполнитеfaraday
