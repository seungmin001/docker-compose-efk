# docker-compose-efk
EFK Stack using docker compose <br>
E: elasticsearch <br>
F: fluentd <br>
K: kibana <br>

# setup
enter the following command from your project directory (where docker-compsoe.yml file exists) <br>
```
docker-compose up -d
```

### send data to fluentd
Fluentd will send data to elasticsearch. <br>
Index prefix will be fluentd. Modify 'fluent.conf' to change this setting. <br>
```
curl -XPOST http://localhost:9880 -H "Content-Type: application/json" -d '{"foo":"bar"}'
```

### check kibana
enter this url in your browser <br>
http://localhost:5601 <br>


# elasticsearch
3 nodes (es01:9200,es02:9201,es03:9202) <br>
heap size per node (256mb) (Modify 'heap.options' to change this setting.) <br>
x-pack security off <br>
