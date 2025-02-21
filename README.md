# Manual Tecnico
## Practica 

### Descripcion del problema 

Sigma Studio es un estudio de arquitectura y diseño gráfico reconocido por su enfoque
innovador en la creación de espacios funcionales y estéticamente atractivos. Gracias a su
combinación de talento arquitectónico y creatividad digital, la empresa ha trabajado con
clientes en proyectos de urbanismo, interiorismo y diseño publicitario.

Se realizo la organizacion 30 computadoras para el personal de las diferentes areas del estudio, configurando asi una red local (LAN) en las oficinas de Sigma Studio lo cual permite una comunicacion entre todas las computadoras, se les configuro una direccion IP a cada computadora las cuales estan conectadas a sus swiches correspondientes.

## Tabla de las IP utilizadas

| **Área**                 | **Dispositivo** | **Dirección IP**  |
|--------------------------|-----------------|------------------|
| Recepción y Administración | RyA1           | 192.168.50.1     |
| Recepción y Administración | RyA2           | 192.168.50.2     |
| Recepción y Administración | RyA3           | 192.168.50.3     |
| Recepción y Administración | RyA4           | 192.168.50.4     |
| Recepción y Modelado       | RyM1           | 192.168.50.5     |
| Recepción y Modelado       | RyM2           | 192.168.50.6     |
| Recepción y Modelado       | RyM3           | 192.168.50.7     |
| Recepción y Modelado       | RyM4           | 192.168.50.8     |
| Recepción y Modelado       | RyM5           | 192.168.50.9     |
| Recepción y Modelado       | RyM6           | 192.168.50.10    |
| Alta Dirección             | AD1            | 192.168.50.11    |
| Alta Dirección             | AD2            | 192.168.50.12    |
|Alta Dirección              | AD3            | 192.168.50.13    |
| Alta Dirección             | AD4            | 192.168.50.14    |
| Ayuda y Urgencias          | AyU1           | 192.168.50.15    |
| Ayuda y Urgencias          | AyU2           | 192.168.50.16    |
| Ayuda y Urgencias          | AyU3           | 192.168.50.17    |
| Ayuda y Urgencias          | AyU4           | 192.168.50.18    |
| Ayuda y Urgencias          | AyU5           | 192.168.50.19    |
| Ayuda y Urgencias          | AyU6           | 192.168.50.20    |
| Ayuda y Urgencias          | AyU7           | 192.168.50.21    |
| Ayuda y Urgencias          | AyU8           | 192.168.50.22    |
| Ayuda y Urgencias          | AyU19          | 192.168.50.23    |
| Ayuda y Urgencias          | AyU10          | 192.168.50.24    |
| Dirección General y Proyectos | DGyP1      | 192.168.50.25    |
| Dirección General y Proyectos | DGyP2      | 192.168.50.26    |
| Dirección General y Proyectos | DGyP3      | 192.168.50.27    |
| Dirección General y Proyectos | DGyP4      | 192.168.50.28    |
| Dirección General y Proyectos | DGyP5      | 192.168.50.29    |
| Dirección General y Proyectos | DGyP6      | 192.168.50.30    |

### Vista general de las distribucion de la red
<img src="https://i.ibb.co/JWc5zMJg/red.png" alt="red" border="0">

## Comandos usados en para la configuracion de los Switches
#Entrar al usuario privilegiado 
enable
#Configuracion global
configure terminal
no ip domain-lookup
hostname admin

enable password 202001950
#guardar la configuracion
write memory


## Configuracion de las PCSs
### Area de Recepcion y Administracion
<img src="https://i.ibb.co/DPshsqhC/Captura-de-pantalla-2025-02-20-001112.png" alt="Captura-de-pantalla-2025-02-20-001112" border="0">

### Area de Renderizado y Modelado 3D
<img src="https://i.ibb.co/QjfP2MwP/Captura-de-pantalla-2025-02-20-001010.png" alt="Captura-de-pantalla-2025-02-20-001010" border="0">

### Area de Alta direccion 
<img src="https://i.ibb.co/1f2myGzZ/Captura-de-pantalla-2025-02-20-000843.png" alt="Captura-de-pantalla-2025-02-20-000843" border="0">

### Area de Arquitectura y Urbanismo
<img src="https://i.ibb.co/Yn0wZvR/Captura-de-pantalla-2025-02-20-000750.png" alt="Captura-de-pantalla-2025-02-20-000750" border="0">

### Area de Diseño Grafico y Publicidad
<img src="https://i.ibb.co/C3RcXBDG/Captura-de-pantalla-2025-02-20-001223.png" alt="Captura-de-pantalla-2025-02-20-001223" border="0">

## Pigns entre hosts
<img src="https://i.ibb.co/XrT8bCnr/Captura-de-pantalla-2025-02-20-182303.png" alt="Captura-de-pantalla-2025-02-20-182303" border="0">

<img src="https://i.ibb.co/ZpF0JHQv/ping2.png" alt="ping2" border="0">

<img src="https://i.ibb.co/Hfhmk8k5/ping3.png" alt="ping3" border="0">

<img src="https://i.ibb.co/zWSMzYm0/ping4.png" alt="ping4" border="0">

<img src="https://i.ibb.co/SXk1cJDg/ping5.png" alt="ping5" border="0">

## Captura de paquete ARP
<img src="https://i.ibb.co/bgDVhZgm/arp.png" alt="arp" border="0">

## Captura de paquete ICMP
<img src="https://i.ibb.co/GfpXhH6y/icmp.png" alt="icmp" border="0">
