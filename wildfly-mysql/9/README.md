
# Wildfly-mysql

Imagem do servidor Wildfly versão 9.0.2 Final
baseada na  imagem ifbaeunapolis/jdk que faz a instalação do jdk 8 em um sistema ubuntu:14.04
Configurado para rodar nas portas 8080 e 9990, e drive para o banco de dados MySQL versão 5.1.38

###Pull image no hub docker
```
docker pull ifbaeunapolis/wildfly-mysql
```
###Run image 
```
docker run -d --name web --link mysqldb:mysql -p 8080:8080 -p 9990:9990  ifbaeunapolis/wildfly-mysql -Dmysql.ipaddress=mysqldb -Dmysql.port=3306 -Dmysql.database=db_name -Dmysql.root_password=mysql -Dmysql.username=root -Dmysql.password=mysql 
```
###Run docker-compose
```
docker-compose up
```
No diretorio onde está o arquivo .yml em sua máquina.
