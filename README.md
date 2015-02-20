docker-fcrepo4
==============

Inspired by Chris Beer's cbeer/docker-fcrepo4.

Features (from jolokia/tomcat-8.0):

- Tomcat Version: 8.0.5
- Java Version: Oracle 1.7.0_51-b13 (base image: dockerfile/java)
- Port: 8080
- User admin (Password: admin) has been added to access the admin applications /host-manager and /manager)

- Documentation and examples have been removed

- Command: `/opt/tomcat/bin/deploy-and-run.sh` which links `.war` files from `/maven` to 
  `/opt/tomcat/webapps` and the calls `catalina.sh run`

This repository adds:

- Fedora 4.1.0 deployed to http://$DOCKER_HOST:8080/fcrepo/rest

```console
$ docker pull bencomp/docker-fcrepo4
$ docker run -p 8080:8080 bencomp/docker-fcrepo4
$ curl http://localhost:8080/fcrepo/rest/
```
