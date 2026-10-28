![[Pasted image 20260825155805.png]]
## Comunicación interna ( Corto Alcance)
- Protocolos alámbricos: UART, RS232, RS
	- Comunican Sensores o periféricos
	- CAN BUS
	- I2C 
	- RS485 comunicación industrial.
- Protocolos Inalámbricos
	- Bluetooth, Wifi, NFC, RFID, RF-Modulado directo 
	- Protocolos propietarios (tecnología de paga)
	- Bluetooth 4.0  ahorro de energía, multidispositivo.
	- Beacon: envía ubicación en función de la potencia que recibe, triangula posición de objetos.

IOT
- Productos de bajo costo.
- Poca intervención humana.
- Implementación con baterías. (poco uso de energía)
- Poca infraestructura.
## Comunicación de largo alcance
- **WAN** Redes de área amplia o  (Wide Area Network) alámbricas en cable coaxial, por trenzado o fibra óptica.
	- **Alcance:** Extenso; abarca desde distancias de miles de kilómetros hasta cobertura global. 
	- **Tecnología:** Utiliza infraestructura de telecomunicaciones, fibra óptica, enlaces satelitales o servicios de proveedores de internet (ISP). 
	- **Ventajas:** Permite interconectar distintas sucursales de una empresa o enlazar redes locales (LAN/WLAN) a nivel mundial. 

	- **Desventajas:** Mayor complejidad de configuración, costos más elevados de mantenimiento y requiere medidas de seguridad robustas (como firewalls o VPN)
- **WLAN** (Wireless Local Area Network) Redes y comunicación inalámbrica celular 2G, 3G y 4G **WAN** . A partir de las 3G  PP todas la empresas se homologan
- Protocolos de redes ampliar y bajo consumo energético LPWAN (Low Power Wide Area Network) - LTE CAT-M, NBIoT, Sigfox & LoRa-WAN.

![[Pasted image 20260824000350.png]]


![[Pasted image 20260824000425.png]]

PAN: No logran envíar voz pero no consumen gran energía
LAN
WAN 
LPWAN: Bajo consumo gran distancia de cobertura}
SigFox: Logra transmitir hasta 29 Km

![[Pasted image 20261007191828.png]]
## UIT - Unión Internacional de Telecomunicaciones.

- Existe desde 1865.
- Sede en Ginebra, Suiza.
- Emite recomendaciones para fomentar el desarrollo de las telecomunicaciones.
- Surge a partir de la primera red de telégrafos.

### IFT - Instituto Federal de Telecomunicaciones
- Organismo Regulador (Autónomo) 
- Antes Comisión Federal de Telecomunicaciones dependencia de la SCT.
- Bandas de uso libre y bandas concesionadas: **Espacios de Frecuencias donde se puede Transmitir Información**. 
	- Bandas de Uso Libre. No están regulado, puede contener ruido
	- Bandas Concesionadas. A través de licitación, se otorga a las bandas reguladas a cada proveedor de telecomunicaciones.
- Cuadro Nacional de Atribu
- Promueve competitividad entre empresas.
### Bandas de uso libre – IMT (Industriales, Médicas y Tecnológicas) - ISM( Idustrial, Scuientific, Technologic)
■ 902 - 928 MHz – Sigfox, LoRaWan
■ 1920 – 1930 MHz (utilizadas en 4G)
■ 2400 – 2483.5 MHz – Wifi 2.4, Bluetooth, Zigbee, Z-wave
■ 5150 – 5350 MHz (Aplicaciones libres)
■ 5470 - 5600 MHz (Aplicaciones libres)
■ 5650 - 5850 MHz –Wifi 5G
■ 57 - 64 GHz 
■ 71 - 76 GHz
■ 81 - 86 GHz

Entre mas alta la banda  la interferencia  con objetos es mayor: ej. Bandas Wifi 2.4 llega  a mas lugares de la casa que wifi 5g

Frecuencia mas alta mayor pérdida en distancia: Incluso gotas de lluvia pueden afectar la onda
Zwave
ZBee

Se necesitan 64 kbps para enviar voz a través de un medio


###  ZIGBEE
- Zigbee. Considerada aparte de las LPWAN debido a que se utiliza en robotica no de area amplia, sino de cobertura mas corta, utiliza las bandas de Wifi, no tiene suscripciones. Pero necesita un mallado
	- Utiliza tres roles de dispositivos:
	- Coordinador:
	- Router:
	- End Device:

### 5G, 4G, 4G, 2G
La tecnologías 5G, 4G, 4G, 2G, son las mejoras de la 
- Pioneros Huawei, Erickson y Nokia
- Velocidades mas altas
- Latencias más pequeñas
- Accesibilidad a mas personas
#### Tecnologías que caracterizan al 5G

- Dos bandas: Ondas milimétricas: sub 6GHz 21000 - 5000 MHz
	- Parte alta: 26 GHz . 39 GHz
- Células Pequeñas - Previamente macro y micro (ejemplo: antenas en el metro)
- Limpieza de Bandas: Bandas saturadas utilización 


## Selección de Red para Casos de Uso

![[Pasted image 20261008151233.png]]