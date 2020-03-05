# Arcadia Finance

Arcadia Finance Application

![picture](https://gitlab.com/arcadia-application/main-app/-/raw/master/Micro%20Services%20architecture.png)

Credentials are admin/iloveblue (will be changed soon - issue opened)

//////////////////////

/api is App2

/app3 is App3

/files is the Back End App

//////////////////////

docker network create internal

//////////////////////

docker run -dit -h mainapp --name=mainapp --net=internal registry.gitlab.com/arcadia-application/main-app/mainapp:latest

//////////////////////


docker run -dit -h backend --name=backend --net=internal registry.gitlab.com/arcadia-application/back-end/backend:latest

//////////////////////

docker run -dit -h app2 --name=app2 --net=internal registry.gitlab.com/arcadia-application/app2/app2:latest

//////////////////////

docker run -dit -h app3 --name=app3 --net=internal registry.gitlab.com/arcadia-application/app3/app3:latest

//////////////////////

docker run -dit -h nginx --name=nginx --net=internal -p 80:80 -v full_path_to_nginx_conf_file:/etc/nginx/conf.d/default.conf registry.gitlab.com/arcadia-application/nginx/nginxoss:latest

Use default.conf NGINX file for the NGINX API GW.
