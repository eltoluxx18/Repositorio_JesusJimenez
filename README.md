# Portafolio de Evidencias de Pentesting

Este repositorio contiene evidencias de pruebas de penetración realizadas con diversas herramientas. Las evidencias están organizadas por herramienta.

## Estructura del repositorio:
- **NMAP**: Resultados de escaneos de red.
- **Masscan**: Escaneos rápidos de puertos.
- **Google Dorks**: Consultas avanzadas en motores de búsqueda.
- **Shodan**: Búsquedas de dispositivos expuestos.
- **SQLMAP**: Pruebas de inyección SQL automatizadas.
- **Wireshark**: Capturas de tráfico de red.
- **InyeccionSQL-DVWA**: Pruebas manuales de inyección SQL en DVWA.

## Documentación:

- **Nmap**
Comando Utilizado: sudo nmap -p- 192.168.0.101

Resultado: Nmap detectó los puertos abiertos en la IP, identificó los servicios asociados y realizó un análisis del sistema operativo. Los resultados mostraron los siguientes puertos abiertos:

Puerto 22: SSH

Puerto 80: HTTP

Mitigaciones de Seguridad:

Configurar reglas de firewall para limitar accesos no autorizados.

Deshabilitar servicios innecesarios o no utilizados.

- **Masscan**
Comando Utilizado: sudo masscan 192.168.0.101 -p0-65535

Resultado: Masscan detectó puertos abiertos en un escaneo de alta velocidad. Los resultados incluyeron:

Puerto 22: SSH

Puerto 80: HTTP

Mitigaciones de Seguridad:

Limitar la exposición de puertos abiertos y aplicar controles de acceso.

Monitorear actividad inusual en los puertos.

- **Google Dorks**
Comando Utilizado: site:.gob.mx filetype:pdf "manual de seguridad" intitle:"seguridad pública" filetype:pdf

Resultado: Este Google Dork buscó documentos públicos relacionados con manuales de seguridad en sitios gubernamentales (.gob.mx). Los resultados mostraron varios documentos disponibles para consulta.

Mitigaciones de Seguridad:

Restringir acceso a documentos confidenciales mediante permisos.

Monitorear posibles indexaciones no autorizadas en motores de búsqueda.

- **Shodan**
Comando Utilizado: Mexico country:"MX" city:"Merida" 

Resultado: Shodan detectó dispositivos en Merida, México. Los dispositivos identificados incluyen cámaras IP y routers con configuraciones accesibles.

Mitigaciones de Seguridad:

Actualizar firmware de dispositivos expuestos.

Configurar contraseñas robustas y deshabilitar accesos públicos.

- **Wireshark**
Captura Realizada: Tráfico de red durante 20 segundos en la red local.

Resultado: Wireshark capturó paquetes de diferentes protocolos, incluyendo DNS y HTTP, lo que permitió identificar patrones de comunicación y posibles vulnerabilidades.

Mitigaciones de Seguridad:

Configurar reglas para filtrar tráfico malicioso.

Utilizar herramientas de detección de intrusiones para monitorear tráfico.

- **InyeccionSQL-DVWA**
Comando Utilizado: 1' OR '1'='1

Resultado: Aprovecha una vulnerabilidad de inyección SQL al manipular la consulta del servidor, haciendo que la condición siempre sea verdadera (1 = 1). Esto permite acceder a información que no debería ser pública.

Mitigaciones de Seguridad:

Validar y sanitizar todas las entradas de usuario para evitar inyecciones SQL.

Utilizar consultas parametrizadas en el código del servidor.

Implementar mecanismos como WAF (Web Application Firewall) para prevenir ataques.


## Notas:
- Todas las pruebas fueron realizadas en entornos controlados y autorizados.


