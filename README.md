# Practica-wifi-segura
## Introducción:
En este trabajo vamos a inspeccionar la conexión a una página http para poder comparar la información que se transmite al navegar en una conexión realizada sin vpn, y otra con vpn. Así como también mencionaremos los potenciales riesgos de seguridad que podemos tener al navegar en redes wifi públicas.
## Analisis de navegacion sin VPN. Inspeccionar la conexión
Vamos a ingresar a la pagina http://neverssl.com para poder ver lo que ocurre en el navegador en una conexión sin cifrar.
Captura ingresando a la pagina http://neverssl.com y abriendo los elementos de desarrollador con F12. Actualizamos la pagina con F5 y aquí vamos a poder inspeccionar la conexión.
<img width="971" height="441" alt="image" src="https://github.com/user-attachments/assets/19a5d34a-4afb-4703-a21a-4c3340702a39" />
<img width="974" height="440" alt="image" src="https://github.com/user-attachments/assets/da20f226-a690-4688-9504-f61165e0911f" />
<img width="981" height="445" alt="image" src="https://github.com/user-attachments/assets/98dc3efe-7d0e-4927-8faf-fc2061c18e23" />
## Documentamos lo visible
URL de solicitud: http://sublimefunsoothingmagic.neverssl.com/online/

Método De Solicitud: GET

Accept-Encoding: gzip,deflate

Accept-Language: es-ES,es;q=0.9,en;q=0.8

Connection: keep-alive

Host: sublimefunsoothingmagic.neverssl.com

Referer: http://neverssl.com/

User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.0.0 Safari/537.36

Protocolo: http/1.1

El protocolo HTTP, es un protocolo que transmite información sin cifrar.

## Explicamos el riesgo

¿Qué podría interceptar alguien que esté conectado a la misma wifi que yo?

Alguien malintencionado que se encuentre conectado a la misma wifi pública que yo y llegara a lograr capturar el tráfico de otros dispositivos, puede ver la información que se transmite sin cifrar.

## Tres escenarios de riesgo:

 1.	Sniffing: Es la captura de tráfico. Sucede cuando se capturan los paquetes de datos que circulan por una red. Por ejemplo: sitios web, direcciones IP, contenido transmitido sin cifrado, datos ingresados en páginas http.
 2.	Intermediario: Un atacante hace creer a tu dispositivo que él es el router. Consigue ubicarse entre tu dispositivo y el servidor con el que quiere comunicarse. En este caso también puede quedar expuesta la información que surja entre las solicitudes y respuestas intercambiadas entre el navegador y el servidor.
 3.	Red gemela: Es una red wifi creada por un atacante que imita el nombre de una red legitima. En este caso también queda comprometida la información que sea ingresada en páginas falsas que imitan sitios legítimos.

<img width="1156" height="97" alt="image" src="https://github.com/user-attachments/assets/5b35d9c9-0bda-46be-8007-4a8ff09a3d7a" />

## Sumamos la VPN

## Documentamos lo visible y detallamos la diferencia entre ingresar sin vpn y con vpn

<img width="1003" height="456" alt="image" src="https://github.com/user-attachments/assets/52d6e42f-1d97-49d1-b825-ef4d0f5cae00" />

<img width="1010" height="459" alt="image" src="https://github.com/user-attachments/assets/5a7076e7-7f71-4510-af81-12382911a162" />

URL de solicitud: https://silverinnerslowsecret.neverssl.com/online/

Método De Solicitud: GET

Accepted-Encoding: gzip, deflate, br, zstd

Accept-Language: es-ES,es;q=0.9,en;q=0.8

Connection: keep-alive

Host: silverinnerslowsecret.neverssl.com

Referer: http://neverssl.com/

User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.0.0 Safari/537.36

## Evidencia encontrada: 
Sin vpn podemos observar la solicitud mediante el protocolo http/1.1 que transmite información sin cifrado. Luego con vpn activa, se observó una solicitud mediante https, siendo ésta conexión la cual presenta un cifrado en la comunicación con el sitio web.

## Cómo cambia la escena con la VPN activa 

## Túnel activo: 
La VPN funciona como un túnel blindado. La pc deja de comunicarse directamente con internet para enviar el tráfico a través de un túnel vpn cifrado. 
De este modo, la dirección IP pública queda oculta para los sitios que se visiten, así como también los datos viajan primero al servidor vpn, y éste se encarga de reenviar las solicitudes hacia el destino. 

## Cifrado: 
La vpn cifra el tráfico que va desde la pc hacia el servidor vpn. De esta manera, se intenta impedir que otras personas que estén conectadas a la misma red accedan a mi información.

## Encapsulamiento: 
Refiere a que los datos originales viajen protegidos dentro de una nueva estructura de comunicación.

<img width="762" height="95" alt="image" src="https://github.com/user-attachments/assets/3bc3a901-1cc3-4da3-a16d-fbfdb02705f5" />

## 3 reglas de oro para navegar en redes wifi-públicas

1.	Revisar siempre el dominio.
2.	Utilizar una VPN antes de conectarse a redes wifi públicas.
3.	Evitar redes desconocidas, o utilizar datos del celular en caso de realizar ingresos a aplicaciones sensibles, como por ejemplo la aplicación del banco.



  












