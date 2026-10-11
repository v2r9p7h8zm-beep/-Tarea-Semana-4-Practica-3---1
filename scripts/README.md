
TOPOLOGÍA
FG-DMZ:
  port1 = gestión 192.168.46.129/24
  port2 = enlace troncal 802.1Q a SW-USERS
  port3 = enlace a SW-DMZ
  port5 = WAN 192.168.42.205/24, gateway 192.168.42.1

REDES
  VLAN10 = 10.86.10.0/25; gateway 10.86.10.1
  VLAN20 = 10.86.20.0/25; gateway 10.86.20.1
  DMZ = 10.86.30.0/28; gateway 10.86.30.1
  SRV-CAJA = 10.86.30.2
  SRV-INVENTARIO = 10.86.30.3
  SRV-DB = 10.86.30.4

SW-USERS (GNS3 Ethernet switch)
  puerto 0: dot1q / trunk al FortiGate
  puertos de usuarios: acceso VLAN 10 o VLAN 20
SW-DMZ
  puertos de acceso para FortiGate y tres servidores

POLÍTICAS DOCUMENTADAS (descripción, no CLI exportada)
  VLAN10 -> Inventario: HTTP/HTTPS permitido
  VLAN20 -> servidores DMZ: SSH permitido
  DMZ -> repositorios Ubuntu: HTTP/HTTPS permitido para actualizaciones
  DMZ -> resolutores DNS autorizados: DNS permitido
  Otro tráfico no autorizado: DENY implícito

PRUEBAS REGISTRADAS
  DHCP y ping a gateway VLAN10/VLAN20
  HTTP 200 al Inventario desde VLAN10
  SSH no autorizado desde VLAN10: timeout
  SSH desde VLAN20: solicitud de contraseña
  Aislamiento DMZ-LAN: tráfico bloqueado
  apt update: ejecutado con acceso restringido a repositorios


TOPOLOGÍA
FG-DMZ:
  port1 = gestión 192.168.46.129/24
  port2 = enlace troncal 802.1Q a SW-USERS
  port3 = enlace a SW-DMZ
  port5 = WAN 192.168.42.205/24, gateway 192.168.42.1

REDES
  VLAN10 = 10.86.10.0/25; gateway 10.86.10.1
  VLAN20 = 10.86.20.0/25; gateway 10.86.20.1
  DMZ = 10.86.30.0/28; gateway 10.86.30.1
  SRV-CAJA = 10.86.30.2
  SRV-INVENTARIO = 10.86.30.3
  SRV-DB = 10.86.30.4

SW-USERS (GNS3 Ethernet switch)
  puerto 0: dot1q / trunk al FortiGate
  puertos de usuarios: acceso VLAN 10 o VLAN 20
SW-DMZ
  puertos de acceso para FortiGate y tres servidores

POLÍTICAS DOCUMENTADAS (descripción, no CLI exportada)
  VLAN10 -> Inventario: HTTP/HTTPS permitido
  VLAN20 -> servidores DMZ: SSH permitido
  DMZ -> repositorios Ubuntu: HTTP/HTTPS permitido para actualizaciones
  DMZ -> resolutores DNS autorizados: DNS permitido
  Otro tráfico no autorizado: DENY implícito

PRUEBAS REGISTRADAS
  DHCP y ping a gateway VLAN10/VLAN20
  HTTP 200 al Inventario desde VLAN10
  SSH no autorizado desde VLAN10: timeout
  SSH desde VLAN20: solicitud de contraseña
  Aislamiento DMZ-LAN: tráfico bloqueado
  apt update: ejecutado con acceso restringido a repositorios
  
