# docker-compose-multi-container-usando-a-mesma-network

# Todos os passos a seguir são para distribuições linux

Primeiro passo: Instalar o docker-engine e o docker-compose

$ sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

Segundo passo: Criar diretorio para o arquivo docker-compose.yml

$ mkdir pasta-docker
$ cd pasta-docker

Terceiro passo: Arquivo docker-compose.yml

Você pode baixar e mover o arquivo docker-compose.yml que esta no main ou criar um arquivo docker-compose.yml e colar as linhas do mesmo

Quarto passo: Criando os containers

Dentro do diretorio com o arquivo docker-compose.yml já salvo você digitará:

$ docker-compose up -d

#Pronto ja esta criado os dois containers, um com imagam do nginx e outro do mysql

Quinto passo: Entrando no container do nginx usando bash 

Abra outra aba no terminal e digite:

$ docker exec -it pasta-docker_web_1 bash 

Sexto passo: Colocando ou modificando seu index.html

Dentro do container do ngnix você digitará:

$ cd /usr/share/nginx/html

Após isso usando instale a ferramenta de edição de texto de sua preferencia, já que não terá nenhuma no container, no meu caso usei o vim, instalando-o com os seguintes passos:

$ apt-get update 
$ apt-get install vim -y




