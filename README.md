Jenkins Setup
==========

> Jenkins with the Blue Ocean UI up and using `docker` and `docker-compose`

## How to use:

1. Set `.env` file `JENKINS_HTTP_PORT` and `JENKINS_HTTPS_PORT` to a high port (e.g. 18443) on Minikube.

2. Run docker-compose to bring up Jenkins

```sh
$ docker-compose up -d
```

3. Get your initial admin password

```sh
$ docker-compose exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword
```

4. Open Jenkins in your browser by going to either http://0.0.0.0:8080/ or https://0.0.0.0:8443/ (or whatever your Docker Machine IP is).