----------- Install Docker-----------------

https://github.com/zafims/install-docker

-------------------------------------------
Homepage:3005
1. wget https://raw.githubusercontent.com/zafims/install-dashboard/main/homepage.yml
2. mv homepage.yml docker-compose.yml
3. mkdir /docker-compose/script/homepage -p
4. mv docker-compose.yml /docker-compose/script/homepage
5. cd /docker-compose/script/homepage
6. docker-compose up -d

Homarr:3004
1. wget https://raw.githubusercontent.com/zafims/install-dashboard/main/homarr.yml
2. mv homarr.yml docker-compose.yml
3. mkdir /docker-compose/script/homarr -p
4. mv docker-compose.yml /docker-compose/script/homarr
5. cd /docker-compose/script/homarr
6. docker-compose up -d

it-tools:3006
1. wget https://raw.githubusercontent.com/zafims/install-dashboard/main/it-tools.yml
2. mv it-tools.yml docker-compose.yml
3. mkdir /docker-compose/script/it-tools -p
4. mv docker-compose.yml /docker-compose/script/it-tools
5. cd /docker-compose/script/it-tools
6. docker-compose up -d

Dash:3002
1. wget https://raw.githubusercontent.com/zafims/install-dashboard/main/dash.yml
2. mv dash.yml docker-compose.yml
3. mkdir /docker-compose/script/dash -p 
4. mv docker-compose.yml /docker-compose/script/dash
5. cd /docker-compose/script/dash
6. docker-compose up -d

Dozzle:3002 Docker Log Viewer
1. wget https://raw.githubusercontent.com/zafims/install-dashboard/main/dozzle.yml
2. mv dozzle.yml docker-compose.yml
3. mkdir /docker-compose/script/dozzle -p
4. mv docker-compose.yml /docker-compose/script/dozzle
5. cd /docker-compose/script/dozzle
6. docker-compose up -d

HEIMDALL:3003
1. wget https://raw.githubusercontent.com/zafims/install-dashboard/main/heimdall.yml
2. mv heimdall.yml docker-compose.yml
3. mkdir /docker-compose/script/heimdall -p
4. mv docker-compose.yml /docker-compose/script/heimdall
5. cd /docker-compose/script/heimdall
6. docker-compose up -d

=================== Install Portainer ==============

---> First let's create our volume, for that use the command below:

$ sudo docker volume create portainer_data

---> To install the Portainer, use the command below:

$ sudo  docker run -d -p 9000:9000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest -H unix:///var/run/docker.sock

--->Browse : IP:9000
			---> ex: 170.64.157.123:9000
