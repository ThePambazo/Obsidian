## Topología - Arquitectura

NBIoT


A nivel de Red de Comunicación
dISPOSITIVOS TERMINALES / End Point
Radio bases (no es control del usuario/cliente)
Cloud

![[Pasted image 20261007203952.png]]

LoraWAN

Nodos terminales, Endpoint: todos los dispositivos electronicos físicos 
Gateway: Encargado de hablar LoRAWAN, y se encarga de enviar información a la nube a través de una red 3G/4G o ethernet epmaquetando la información 

![[Pasted image 20261007204009.png]]



Servicio On Premise .Servidores Físicos
Nube: Infraestructure as a Service máquinas virtuales



## LTE CAT M1


Dispositivo Terminal -----> Base Station ----> Servidor Nube / Físico

![[Pasted image 20261007204624.png]]


## SigFox 

Dispositivos (solamente) ----> SigFox Base Station (controladas por terceros WND) -----> Servidor en la nube (Sigfox Cloude) 

SigFox mantiene el protocolo de comunicación y la herramienta donde almacena la información (Backend Sigfox).

![[Pasted image 20261007204913.png]]


## ZigBee

Es la red mas utilizada en domótica.

ZigBee Coordinator (Gateway) - - -  ZigBee Routers - - -  (Repetidores) ZigBee Devices

Depende si el fabricante indica que los dispositivos tienen capacidad de interconexión y repetición de información


![[Pasted image 20261007205230.png]]



![[Pasted image 20261007205656.png]]