# Rodando dbeaver e duas versões do postgres

### subir os serviços
 ```
 $ docker-compose -f docker-compose_test.yaml up -d
```

### Pegar o ID do container do postgres

```$ docker ps```

### Pegar o IP do container para criar a conexão no dbeaver

``` 
$ docker inspect -f \ '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <<container_id>>
```