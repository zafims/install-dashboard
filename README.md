----------- Install Docker-----------------

https://github.com/zafims/install-docker

-------------------------------------------
Homarr:
1. wget https://raw.githubusercontent.com/zafims/install-dashboard/main/homarr.yml
2. mv homarr.yml docker-compose.yml
3. mkdir /docker-compose/script/homarr -p
4. mv docker-compose.yml /docker-compose/script/homarr
5. cd /docker-compose/script/homarr
6. docker-compose up

it-tools:
1. wget https://raw.githubusercontent.com/zafims/install-dashboard/main/it-tools.yml
2. mv it-tools.yml docker-compose.yml
3. mv docker-compose.yml /docker-compose/script/it-tools -p
4. cd /docker-compose/script/it-tools
5. docker-compose up

Dash:
1. wget https://raw.githubusercontent.com/zafims/install-dashboard/main/dash.yml
2. mv dash.yml docker-compose.yml
3. mv docker-compose.yml /docker-compose/script/dash -p
4. cd /docker-compose/script/dash
5. docker-compose up

Dozzle: Docker Log Viewer
1. https://raw.githubusercontent.com/zafims/install-dashboard/main/dozzle.yml
2. mv dozzle.yml docker-compose.yml
3. mv docker-compose.yml /docker-compose/script/dozzle -p
4. cd /docker-compose/script/dozzle
5. docker-compose up

=================== Install Portainer ==============

---> First let's create our volume, for that use the command below:

$ sudo docker volume create portainer_data

---> To install the Portainer, use the command below:

$ sudo  docker run -d -p 9000:9000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest -H unix:///var/run/docker.sock

--->Browse : IP:9000
			---> ex: 170.64.157.123:9000
