Comandos básicos

ls - listar archivos de un directorio
ls -l -- listar toda la informacion
pwd - donde estoy
whoami - quien soy
cd / - Al home
cd .. - Subo un nivel


Directorio raiz /

etc - configuracion
bin - programas
var- datos d programas
home -usuarios (/home/ubuntu/environment)
tmp -  se borra al salir

Archivos en linux
drwxr-xr-x   2 root root  4096 Nov  2 17:05 bin
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