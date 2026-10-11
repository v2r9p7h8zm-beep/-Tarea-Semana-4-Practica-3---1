Infraestructura 1 – Seguridad de Redes | ITLA

Asignatura: Seguridad de Redes
Institución: Instituto Tecnológico de Las Américas (ITLA)
Proyecto: Implementación de una infraestructura de red segura mediante FortiGate, segmentación VLAN y DMZ.

🎥 Video demostrativo
Enlace del video: Ver demostración

El video presenta la topología, las configuraciones de seguridad y las pruebas realizadas para verificar el cumplimiento de los objetivos del laboratorio.

🎯 Propósito del laboratorio

Diseñar e implementar una infraestructura de red segmentada y protegida mediante un firewall FortiGate, utilizando una zona desmilitarizada (DMZ), VLAN, políticas de seguridad y controles de acceso.

El laboratorio busca demostrar cómo la segmentación y las políticas de firewall permiten controlar la comunicación entre usuarios, servidores e Internet, reduciendo los riesgos de acceso no autorizado y movimiento lateral.

🖧 Topología de red

La infraestructura propuesta contempla:

1 firewall FortiGate: control de tráfico, segmentación y políticas de seguridad.

2 switches: conectividad y configuración de VLAN.

3 servidores: Web Server – Sistema de Caja, Web Server – Sistema de Inventario y DB Server.

2 redes de usuarios: VLAN 10 y VLAN 20.

Servicio DHCP: asignación automática de direcciones IP.

DMZ: aislamiento de los servidores respecto a las redes internas.

Diagrama de topología



🔐 Objetivos de seguridad

Configurar la DMZ para alojar los servidores.

Restringir la comunicación entre la DMZ y la LAN.

Limitar las conexiones salientes de los servidores a los endpoints necesarios para actualizaciones.

Permitir acceso SSH a los servidores únicamente desde VLAN 20.

Restringir el acceso de VLAN 10 al Sistema de Inventario.

Demostrar el bloqueo de acceso mediante las políticas del firewall.

Implementar DHCP para las redes de usuarios.

Aplicar configuraciones básicas de seguridad en los switches.

Realizar las configuraciones y demostraciones de FortiGate mediante su interfaz gráfica (GUI).

📁 Documentación técnica

La documentación completa se encuentra organizada en el directorio documentacion/ e incluye los procedimientos de configuración, capturas, pruebas de conectividad, resultados y problemas encontrados durante la implementación.

📸 Evidencias

Las capturas se organizan en evidencias/ para documentar la configuración y las pruebas de seguridad.

⚙️ Configuraciones y scripts

configuraciones/: running-configs y configuraciones exportadas de los dispositivos.

scripts/: scripts utilizados para instalar, configurar o administrar los servicios.

Las credenciales, claves privadas y demás información sensible deben excluirse de los archivos publicados.

📊 Resultados y limitaciones

Los resultados obtenidos, las pruebas satisfactorias, los errores encontrados y los requisitos pendientes de completar se documentan en el informe técnico. Cada prueba debe estar respaldada por evidencia verificable.

📚 Conclusión

Este laboratorio tiene como finalidad aplicar los principios de segmentación, mínimo privilegio y control de acceso para proteger los servicios de una infraestructura empresarial mediante FortiGate y tecnologías de redes.

Instituto Tecnológico de Las Américas (ITLA)
Asignatura: Seguridad de Redes
