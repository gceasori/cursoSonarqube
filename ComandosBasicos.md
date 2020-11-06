Comandos básicos

ls - listar archivos de un directorio
ls -l -- listar toda la informacion
pwd - donde estoy
whoami - quien soy
cd / - Al home
cd .. - Subo un nivel
clear -- limpia

Directorio raiz /

etc - configuracion
bin - programas
var- datos d programas
home -usuarios (/home/ubuntu/environment)
tmp -  se borra al salir

Archivos en linux
drwxr-xr-x   2 root root  4096 Nov  2 17:05 bir
Nombre:bin
Fecha hora edicion:Nov  2 17:05
Tamaño en bytes:4096
Grupo propietario (conjunto usuarios con los mismos permisos): root
Usuario propietario:root

Permisos del archivo: drwxr-xr-x (tres bloques) (rwx r-x r-x) (r-read w-writer x-ejecucion) - 
Primera letra (d-directorio l-enlace simbolico(acceso directo)-b-binario , nada un fichero de texto)
Primer bloque - propietario  (rwx)
2 bloque - grupo r-x
3 bloque - resto r-x


Repositorio
https://github.com/

git clone https://github.com/gceasori/cursoSonarqube.git curso
git clone https://github.com/IvanciniGT/cursoSonarqube.git  ivan

gid add*
git commit -m "Comentario"

git push
git pull

docker --version
node --version
git --version
java -version

docker pull sonarqube
docker images

docker pull tomcat

docker rmi (aquiPongoElIDDElaimagen)

docker rmi $(docker images -q)

ocker container create --name misonarqube -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true -p 8080:9000 sonarqube
739be43a6dde796e9bb65f6aa6a8934f2e5e273f7c851a821ff7774cc5bc721c

docker container list

docker container list --all

docker start misonarqube
docker stop misonarqube


docker rm misonarqube



docker rmi sonarqube

mkdir proyectos

Modificamos nombre del contenedor y puerto
docker run -d --name misonarqube -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true -p 8080:9000 sonarqube:latest


https://hub.docker.com/_/sonarqube (el get started)
De una sola vez

$ docker run -d --name sonarqube -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true -p 9000:9000 sonarqube:latest

sudo su - (para ejecutar como root)
https://hub.docker.com/_/sonarqube (me salgo)

sysctl -w vm.max_map_count=262144
sysctl -w fs.file-max=65536
ulimit -n 65536
ulimit -u 4096


docker rm sonarqube -f (fuerza el parado)

sonarqube - (user/pwd admin/admin)


docker start misonarqube

Ejemplos java
https://github.com/BruceEckel/OnJava8-Examples


Project key* - OnJava8
Token -- GemmaOnJava8
Token -- 73f5692f6825363a6982ade0971d39265ed19fba

GemmaOnJava8: 73f5692f6825363a6982ade0971d39265ed19fba

git clone https://github.com/BruceEckel/OnJava8-Examples.git


Actualización java
sudo yum install java-1.8.0-openjdk


1º-

2º ./gradlew sonarqube \
  -Dsonar.projectKey=OnJava8 \
  -Dsonar.host.url=http://localhost:8080 \
  -Dsonar.login=73f5692f6825363a6982ade0971d39265ed19fba


JavaScriptIvan

https://github.com/Tudor44/cobol-stuff



1 - Clono el proyecto
 git clone https://github.com/davidflanagan/javascript6_examples.git
 git clone https://github.com/Tudor44/cobol-stuff.git
 2- Añado el proyecto en SonarQube manualmente (ejemplo JavaScriptIvan)
        Clave
        Nombre
        tokenProyectoIvan: 12b9f2b669d71de55ee638bbb2aa83541ecb8766
 3- Selecciono lenguaje y SO.
 4 - Para el proyecto java he usado gradle para pasar el código a sonar.
     Con javascript necesito otro proyecto. (SonarScaner)
 
 
 hacemos el unzip sonar-scanner-cl....

 
si creas el fichero de configuración
la clave le pones el tu nombre de proyecto
y luego ejecutas esto
docker run --network=host -e SONAR_HOST_URL='http://127.0.0.1:8080' --user="$(id -u):$(id -g)" -v "$PWD:/usr/src" sonarsource/sonar-scanner-cli 
 
unzip sonar-scanner-cli-4.5.0.2216-linux.zip

echo $PATH
/home/linuxbrew/.linuxbrew/bin:/home/linuxbrew/.linuxbrew/sbin:/home/ubuntu/.nvm/versions/node/v10.23.0/bin:/home/ubuntu/.rvm/gems/ruby-2.6.3/bin:/home/ubuntu/.rvm/gems/ruby-2.6.3@global/bin:/home/ubuntu/.rvm/rubies/ruby-2.6.3/bin:/home/linuxbrew/.linuxbrew/bin:/home/linuxbrew/.linuxbrew/sbin:/home/ubuntu/.rvm/gems/ruby-2.6.3/bin:/home/ubuntu/.rvm/gems/ruby-2.6.3@global/bin:/home/ubuntu/.rvm/rubies/ruby-2.6.3/bin:/home/ubuntu/.rvm/gems/ruby-2.6.3/bin:/home/ubuntu/.rvm/gems/ruby-2.6.3@global/bin:/home/ubuntu/.rvm/rubies/ruby-2.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/home/ubuntu/.local/bin:/home/ubuntu/bin:/home/ubuntu/.rvm/bin:/home/ubuntu/.local/bin:/home/ubuntu/bin:/home/ubuntu/.rvm/bin:/home/ubuntu/.rvm/bin:/home/ubuntu/.local/bin:/home/ubuntu/bin:/home/ubuntu/.rvm/bin:/home/ubuntu/.rvm/bin

set PATH=$PATH:/home/ubuntu/environment/sonar/bin

export PATH=$PATH:/home/ubuntu/environment/sonar/bin

ls /home/ubuntu/environment/sonar/bin

sonar-scanner

sonar-scanner \
  -Dsonar.projectKey=JavaScriptIvan \
  -Dsonar.sources=. \
  -Dsonar.host.url=http://localhost:8080 \
  -Dsonar.login=12b9f2b669d71de55ee638bbb2aa83541ecb8766
  
  
  ./gradlew sonarqube \
  -Dsonar.projectKey=onJava8-2 \
  -Dsonar.host.url=http://localhost:8080 \
  -Dsonar.login=73f5692f6825363a6982ade0971d39265ed19fba
  
  mvn compile
  mvn verify
  
  Permisos
  chmod 777 sonar
  
  
  mvn sonar:sonar \
  -Dsonar.projectKey=NewProject \
  -Dsonar.host.url=http://localhost:8081 \
  -Dsonar.login=c35cd6cc961b0a08a435004c35df6511f07c4a2e
  
  
  en curso/proyectos/mi-aplicacion
  
  
  mvn sonar:sonar \
  -Dsonar.projectKey=NewProject \
  -Dsonar.host.url=https://ec66dec155ab496692ae84e9ba1ad058.vfs.cloud9.eu-west-1.amazonaws.com:8081 \
  -Dsonar.login=c35cd6cc961b0a08a435004c35df6511f07c4a2e
  
 docker-compose up -d
 
 docker logs jenkins