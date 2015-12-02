# observations

## Elasticsearch
   логи 
    ```
    tail -f /var/log/elasticsearch
    ```
## Kibana
  по умолчанию скрипт для запуска кибаны не передает в аргументах файл для логов, 
  но это можно сделать изменив файл /etc/init.d/kibana4
  ```
start-stop-daemon --pidfile "$PID_FILE" --make-pidfile --background --exec $DAEMON --start -- --log-file /var/log/logstash/kibana.log

  ```
  
  как передавать аргументы start-stop-daemon можно узнать из мануала

## Postgresql
  "gotchas" в работе с таймзонами в постгресе. По умолчанию timestamp without time zone он интерпретирует не в utc, а хуй знает как! как разобраться - http://stackoverflow.com/questions/21277170/postgresql-wrong-converting-from-timestamp-without-time-zone-to-timestamp-with-t
  понятия не имею почему питон верно интерпретирует время

## rabbitmq
   rabbitmqctl add_user "my_smy_DEV" "khsaagGHHgasdgjahah238gG7ga"
   rabbitmqctl add_vhost "my_smy_DEV"
   rabbitmqctl set_permissions -p my_smy_DEV "my_smy_DEV" ".*" ".*" ".*"
   
