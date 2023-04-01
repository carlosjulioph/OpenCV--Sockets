# [`socket`](https://docs.python.org/3/library/socket.html#module-socket) — Interfaz de red de bajo nivel

El módulo `socket` de Python provee una interfaz para la API de los sockets Berkeley (otro nombre para los sockets de Internet).

## **Conceptos**

Un **cliente** es todo programa que hace solititudes a un servidor y recive información de este, como por ejemplo: navegadores web, aplicaciones de chat y correo electrónico, entre otras.

Un **servidor** es un programa que recive y maneja las peticiones de los clientes para entregar cada pieza de información al cliente que la solicitó. Algunas aplicaciones servidor son: la misma web, bases de datos, chats y correos electrónicos, etc.

Los **sockets** son los extremos de un canal de comunicación bidireccional. Los sockets se pueden comunicar dentro de un proceso, entre procesos dentro de la misma máquina o entre procesos de máquinas de continentes diferentes.

Los sockets pueden ser implementados a traves de un diferente número de canales: sockets de dominio UNIX, TCP, UDP, etc. La librería `socket` de **python** provee clases específicas para manejar el transporte común asi como también una interfaz genérica para controlar todo lo demás.

Para crear un objeto de este tipo en Python*,* debemos utilizar la función  `socket.socket()` disponible en el módulo *socket,* con la siguiente sintaxis:

```
socket_0 = socket.socket(socket_family, socket_type, protocol=0)
```

Veamos una descripción detallada de los parámetros:

- **socket_family:** es la familia de protocolos que es usada como mecanismo de transporte. Estos valores son constantes tales como **AF_INET, PF_INET, PF_UNIX, PF_X25,** entre otras.
- **socket_type:** el tipo de comunicación entre los dos extremos de la conexión, usualmente se usa **SOCK_STREAM** para protocolos orientados a conexiones y **SOCK_DGRAM** para protocolos sin conexiones.
- **protocol:** Normalmente es 0, este parámetro es usado para identificar la variante de un protocolo dentro de una familia y tipo de socket.
