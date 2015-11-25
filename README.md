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
