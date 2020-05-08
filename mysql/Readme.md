ANSIBLE PLAYBOOK WILDFLY 19 - OPENJDK 11 - CENTOS LINUX

LA INSTALACIÓN ES REALIZADA DESDE SSH POR LO QUE SE DEBERÁ GENERAR UN JUEGO DE LLAVES Y COPIARLA AL SERVIDOR INVOLUCRADO:


1 - Instalar ansible en el cliente que realizara la instalación.
2 - Generar un usuario en el servidor que se instalarán los paquetes, el mismo tiene que tener una contraseña y poder ejecutar comandos con sudo.
3 - Ejecute ssh-keygen en el cliente
4 - Ejecute en el cliente ssh-copy-id usuario@ip_del_servidor para copiar la llave al servidor
5 - Editar archivo envars.yaml según las necesidades
6 - Editar el archivo hosts.conf y definir la ip del o los servidores
7 - Ejecutar ansible-playbook -i hosts.conf -u USUARIO -K  playbook.yaml
Ansible le solicitará la contraseña del usuario indicado con el parámetro -u