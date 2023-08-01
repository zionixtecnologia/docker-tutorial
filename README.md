# docker-tutorial
Docker tutorial by Wesley Willians

Para iniciar o serviço do docker
$ sudo service docker start

Lista todas os containers disponíveis para serem inicializados
$ docker ps -a

Monta um servidor NGINX na porta 8080
$ docker run -p 8080:80 -d nginx


Monta um servidor NGINX na porta 8080 e compartilha a pasta local do projeto
$ docker run -p 8080:80 -v $(pwd)/html:/usr/share/nginx/html nginx

Cria a própria imagem, neste exemplo do servidor NGINX
$ docker build -t zionix/nginx:latest .
$ docker push zionix/nginx:latest
