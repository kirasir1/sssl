# Практика №5
## Инфраструктура
Для выполнения работы были развернуты несколько контейнеров:
`kirill@sharapov:~/lab$ docker ps
CONTAINER ID   IMAGE                                                  COMMAND                  CREATED          STATUS          PORTS                                                                                  NAMES
c3d5fe0731a1   docker.elastic.co/kibana/kibana:7.10.2                 "/usr/local/bin/dumb…"   38 minutes ago   Up 38 minutes   0.0.0.0:5601->5601/tcp, :::5601->5601/tcp                                              kibana
f965ab089231   metasploitframework/metasploit-framework               "docker/entrypoint.s…"   38 minutes ago   Up 38 minutes   0.0.0.0:4444->4444/tcp, :::4444->4444/tcp, 0.0.0.0:8080->8080/tcp, :::8080->8080/tcp   metasploit
f56ae293dd9a   bkimminich/juice-shop                                  "/nodejs/bin/node /j…"   38 minutes ago   Up 38 minutes   0.0.0.0:3000->3000/tcp, :::3000->3000/tcp                                              vulnerable_app
6958cd510d38   greenbone/openvas-scanner                              "/bin/sh -c /usr/loc…"   38 minutes ago   Up 38 minutes   0.0.0.0:9392->9392/tcp, :::9392->9392/tcp                                              openvas
1a953d54a35a   docker.elastic.co/elasticsearch/elasticsearch:7.10.2   "/tini -- /usr/local…"   38 minutes ago   Up 38 minutes   9200/tcp, 9300/tcp`
