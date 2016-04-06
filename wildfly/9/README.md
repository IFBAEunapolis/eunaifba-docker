
# Wildfly

Imagem do servidor Wildfly versão 9.0.2 Final
baseada na  imagem ifbaeunapolis/jdk que faz a instalação do jdk 8 em um sistema ubuntu:14.04
Configurado para rodar nas portas 8080 e 9990.

###Pull image no hub docker
```
docker pull ifbaeunapolis/wildfly
```
###Run image 
```
docker run -d --name wildfly9 -p 8080:8080 -p 9990:9990 ifbaeunapolis/wildfly 
```
###Run docker-compose
```
docker-compose up
```
No diretorio onde está o arquivo .yml em sua máquina.
