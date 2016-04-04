Netbeans 8.1

Nesse repositório está presente o Dockerfile para construção da imagem do netbenas baseado na imagem  wildfly-mysql que está baseada no jdk e no ubuntu 14.04 lts. Já virá incluso na imagem do netbeans o JDK 8, o git, maven, e o projeto do SADE presente nesse repositório para facilitar a utilização.
 
Para rodar no terminal do docker

RUN ubuntu

Rodar comando abaixo primeiro.
xhost +local:docker

sudo docker run -it --env="DISPLAY" --workdir="/home/$USER" --volume="/home/$USER:/home/$USER" --volume="/etc/group:/etc/group:ro" --volume="/etc/passwd:/etc/passwd:ro" --volume="/etc/shadow:/etc/shadow:ro" --volume="/etc/sudoers.d:/etc/sudoers.d:ro" --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" --name netbeans ifbaeunapolis/netbeans-wildfly-mysql-driver

Rodar com o docker-compose
...