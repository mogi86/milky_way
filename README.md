# milky_way
PHP, nginx, php-fmp, docker, ansible

# Requirement
- docker-compose 1.20.1+
- ansible 2.4.0.0+

# Docker set up

```
$ cd /path/to/milky_way/
$ docker-compose build
$ docker-compose up -d
```

# Provisioning

- {environment}には対象環境名(localなど)を入れる

### exce rovisioning

```
$ cd /path/to/milky_way/
$ ansible-playbook -i ansible/inventories/{environment} site.yml
```

### docker exec web container

```
$ cd /path/to/milky_way/
$ docker exec -it milky_way_web /bin/bash --login
```
