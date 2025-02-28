# Manual Tecnico
## Hoja de trabajo 1 

### Descripcion del problema 

El propósito de esta hoja de trabajo es comprender y aplicar el protocolo VTP (VLAN
Trunking Protocol) en una red de switches, configurando diferentes modos de
operación y verificando la propagación de VLANs en un entorno de red jerárquico.

Utilizando Cisco Packet Tracer con 4 switches modelo 2960 con las siguientes configuraciones:

- 4 switches modelo 2960 con las siguientes configuraciones:
- Switch 1: Nombre servidor, configurado como servidor VTP
- Switch 2: Nombre transparente, configurado como transparente VTP
- Switch 3: Nombre cliente01, configurado como cliente VTP
- Switch 4: Nombre cliente02, configurado como cliente VTP
  ### Interconexiones
- Switch servidor interconectado con switch transparente
- Switch transparente interconectado con switch cliente01
- Switch transparente interconectado con switch cliente02
- Switch cliente01 interconectado con switch cliente02
  ### Conexión de dispositivos finales
- Switch cliente01 tendrá tres PC conectadas
- Switch cliente02 tendrá tres PC conectadas

### Vista general de las distribucion de la red

<img src="https://i.ibb.co/dwGrKcmW/Captura-de-pantalla-2025-02-27-235005.png" alt="Captura-de-pantalla-2025-02-27-235005" border="0">

## Comandos para la configuracion de los swiches
### Modo servidor (server)
enable
configure terminal
hostname SERVIDOR
vtp mode server
vtp domain 202001950
vtp password 202001950
exit
### Creación de las VLANS server

enable
configure terminal
vlan 10
name Administracion
vlan 20
name Ventas
vlan 30
name Invitados
exit
wr
### Modo Cliente (client)
enable
configure terminal
hostname SW_CLIENTE
vtp mode client
vtp domain 202001950
vtp password 202001950
exit
wr
### Modo Transparente (transparent)
enable
configure terminal
hostname SW_TRANSPARENTE
vtp mode transparent
vtp domain 202001950
vtp password 202001950
exit
wr
### Creación de las VLANS Transparente

enable
configure terminal
vlan 10
name Administracion
vlan 20
name Ventas
vlan 30
name Invitados
exit
wr
### Modo trunk para el servidor y el switch Transparente
enable
configure terminal
interface f0/1
switchport mode trunk

#Este sirve solo para dejar pasar las vlans que uno necesite en lugar de propagar todas
switchport trunk allowed vlan 10,20,30

exit
wr

### Modo access para los clientes
enable
configure terminal
interface f0/2
switchport mode access
switchport access vlan 10
exit
wr

## Protocolo VTP en cada switch
### servidor
<img src="https://i.ibb.co/jv1p3wsh/Captura-de-pantalla-2025-02-27-233455.png" alt="Captura-de-pantalla-2025-02-27-233455" border="0">

### Transparente
<img src="https://i.ibb.co/PZtPt8mV/Captura-de-pantalla-2025-02-27-233658.png" alt="Captura-de-pantalla-2025-02-27-233658" border="0">

### Cliente01
<img src="https://i.ibb.co/4w5Wq7Qy/Captura-de-pantalla-2025-02-27-233856.png" alt="Captura-de-pantalla-2025-02-27-233856" border="0">

### Cliente02
<img src="https://i.ibb.co/NgGXHZ82/Captura-de-pantalla-2025-02-27-233917.png" alt="Captura-de-pantalla-2025-02-27-233917" border="0">

## VLANS en cada switch
### servidor
<img src="https://i.ibb.co/TxXMyS49/Captura-de-pantalla-2025-02-27-234148.png" alt="Captura-de-pantalla-2025-02-27-234148" border="0">

### Transparente
<img src="https://i.ibb.co/zhcnsgqq/Captura-de-pantalla-2025-02-27-234339.png" alt="Captura-de-pantalla-2025-02-27-234339" border="0">

### Cliente01
<img src="https://i.ibb.co/qLQMmC5T/Captura-de-pantalla-2025-02-27-234442.png" alt="Captura-de-pantalla-2025-02-27-234442" border="0">

### Cliente02
<img src="https://i.ibb.co/4RK6bVnD/Captura-de-pantalla-2025-02-27-234531.png" alt="Captura-de-pantalla-2025-02-27-234531" border="0">



