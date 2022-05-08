><img src="https://upload.wikimedia.org/wikipedia/commons/4/4a/Usac_logo.png" alt="drawing" width="75">
>
> Universidad San Carlos de Guatemala
>
>Facultad de Ingeniería 
>Escuela de Ciencias y Sistemas 
>Primer Semestre, 2022
>
>Laboratorio de Redes de Computadoras 1 Sección *N Impares*



### Grupo No.2

Integrantes:

| Nombre                               | Carnet    |
| ------------------------------------ | --------- |
| <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRH6Uyi30Ty2WkMb0ZjuFLoXmkRwrrMObm-X2zztWtGbOgyA-i7mFzuiSKltN14HLAJDVM&usqp=CAU" alt="drawing" width="20"> &nbsp;Jimmy Yorbany Noriega Chávez         | 200915691 |
|  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQvke8Pr8T6xz52yM8v0ieg0oQy9L9SwfkO4hy4IKoRpxyQBKSGUWto7sWmzj9YYgm1VzU&usqp=CAU" alt="drawing" width="20"> &nbsp; Melyza Alejandra Rodríguez Contreras | 201314821 |
| <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRH6Uyi30Ty2WkMb0ZjuFLoXmkRwrrMObm-X2zztWtGbOgyA-i7mFzuiSKltN14HLAJDVM&usqp=CAU" alt="drawing" width="20"> &nbsp; Romael Isaac Pérez Godinez           | 201213545 |
| <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRH6Uyi30Ty2WkMb0ZjuFLoXmkRwrrMObm-X2zztWtGbOgyA-i7mFzuiSKltN14HLAJDVM&usqp=CAU" alt="drawing" width="20"> &nbsp; Josué Alfredo González Caal          | 201602489 |



 <h1 align="center" > PROYECTO 2</h1>



<div id='content'/>

## CONTENIDO

1. [DESCRIPCION](#id1)
2. [RED FISICA](#id2)
3. [TOPOLOGIA 1](#id3)
4. [TOPOLOGIA 2](#id4)
5. [TOPOLOGIA 3](#id5)

<div id='id1'/>

## 1. DESCRIPCION  [ ⇧](#content)
<div class=''text-justify''>
La empresa “Libros Real S.A”, nos ha contratado para la siguiente configuración que les servirá para organizar de manera segura y eficiente los diferentes departamentos con los que cuenta la empresa, en dos distintos lugares de trabajo; uno de esos lugares es el centro de datos y el otro es la oficina central la cual está próxima a inaugurarse.

Para este caso el centro de datos consta con 4 servidores, el servidor web de ventas, de contabilidad, de recursos humanos e informática, los cuales se encuentran
en subredes diferentes como se muestra en la topología del centro de datos.

La empresa quiere implementar una topología de red para comunicarse desde la
oficina central con el centro de datos.

Los administradores, la base de datos y los servidores web deben de estar en
VLAN diferentes cada uno.

Se debe de proveer la siguiente configuración en la red para cumplir con las
expectativas y requerimientos que la empresa necesita:

- Garantizar que el servidor de contabilidad sea solo accedido por usuarios del departamento de contabilidad y el servidor de recursos humanos sea solo accedido por usuarios del departamento de recursos humanos.

- Garantizar que el servidor web de e-commerce sea accedido solo por los usuarios de ventas.

- Garantizar que el servidor de informática sea accedido únicamente por usuarios del departamento de desarrollo.

- Garantizar la comunicación de los administradores con todos los servidores web.
 </div>
<div id='id2'/>

## 2. RED FISICA [ ⇧](#content)
Para el Proyecto 2, nos hemos apoyado de las herramientas:

<p align="center">
  <img src="/Proyecto2/imagenes/log_gcp.png" alt="drawing" width="200"> <img src="/Proyecto2/imagenes/logo_gns3.png" alt="drawing" width="200"> <img src="https://es.vpnmentor.com/wp-content/uploads/2017/08/Openvpn20Logo.png" alt="drawing" width="200"> 
</p>




Para darle solucion a este problema, conectaron 3 computadoras fisicas por medio de la VPN formando una pequeña red donde estas tienen conexión y acceso a propiedades de red tradicionales como archivos compartidos, y muchas cosas mas por defecto. A continuacion se muestra el grafico que describe nuestra Red Fisica:

<p align="center">
  <img src="/Proyecto2/imagenes/redfisica.png" alt="drawing" width="600">
</p>

<div id='id3'/>

## 3. TOPOLOGIA 1  [ ⇧](#content)
Se realizo el cálculo de subredes de la red 10.2.0.0/16, y se obtuvieron las subredes necesarias para conectar toda la red.
- Se asignaron las direcciones IP a cada uno de los router.
- Se configuraron las rutas estáticas necesarias en los routers para que sea posible establecer la comunicación del centro de datos y la oficina central.
- Se configuro el protocolo de redundancia GLBP.
- Se configuro protocolo de redundancia HSRP.

### Red WAN (Interconexión de centro de datos y oficina central)
```sh
Imagen descriptiva de la Topologia 1
```
<p align="center">
  <img src="/Proyecto2/imagenes/topologia1/topologia1.jpg" alt="drawing">
</p>

```sh
Para esta red se realizo el calculo FLSM que se describe en la siguiente tabla: 
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia1/tablaFLSM.jpg" alt="drawing" width="620" height="400">
</p>

```sh
CONFIGURACIONES
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia1/router1.jpg" alt="drawing" width="600" height="400">
  
  <img src="/Proyecto2/imagenes/topologia1/router3.jpg" alt="drawing" width="600" height="400">
  
  <img src="/Proyecto2/imagenes/topologia1/router2.jpg" alt="drawing" width="600" height="400">
  
  <img src="/Proyecto2/imagenes/topologia1/router4.jpg" alt="drawing" width="600" height="400">
</p>


<div id='id4'/>

## 4. TOPOLOGIA 2  [ ⇧](#content)

### Oficina Central

Dentro de la oficina central se encuentran cuatro departamentos:
  - Recursos Humanos
  - Contabilidad
  - Ventas
  - Bases de datos.


El departamento de recursos humanos cuenta con: 
  - 1 Gerente
  - 15 Reclutadores
  - 5 Analistas de recursos humanos.


El departamento de contabilidad es el más pequeño y actualmente cuenta con:
  - 1 Gerente
  - 5 asistentes de contabilidad 
  - 1 contador en general 
  - 1 auditor

El departamento ventas es el departamento más grande, la empresa prevé un crecimiento de hasta un 32%, cuenta con:
  - 76 Operadores de ventas
  - 4 Encargados de cuentas
  - 12 Managers
  - 1 gerente

  
En el departamento de informática se prevee un crecimiento hasta un 18% por lo que se considero el crecimiento de la Red, cuenta con:
  - 15 Programadores
  - 5 Gestores de proyectos
  - 1 Administrador de la base de datos
  - 3 Analistas de infraestructura
  - 6 Testers
  - 1 Gerente


```sh
Imagen descriptiva de la Topologia 2
```
<p align="center">
  <img src="/Proyecto2/imagenes/topologia2/topologia.jpg" alt="drawing">
</p>


```sh
Para esta red se realizo el calculo VLSM que se describe en la siguiente tabla: 
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia2/subredesVLSM.jpg" alt="drawing">
</p>


```sh
CONFIGURACION DE INTERFACES EN LOS SWITCH
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia2/InterfacesAcces1.jpg" alt="drawing" width="600" height="400">
</p>

<p align="left">
  <img src="/Proyecto2/imagenes/topologia2/interfacesAccess2.jpg" alt="drawing" width="600" height="400">
</p>


```sh
INTERFACE TRONCAL
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia2/interfacesTrunk.jpg" alt="drawing" width="600" height="400">
</p>


```sh
INTERVLAN
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia2/interVLAN.jpg" alt="drawing" width="600" height="400">
</p>


```sh
VLAN20: CONTABILIDAD
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia2/pcContaVlan20.jpg" alt="drawing" width="600" height="400">
</p>


```sh
VLAN40: INFORMATICA
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia2/pcInforVlan40.jpg" alt="drawing" width="600" height="400">
</p>


```sh
VLAN10: RECURSOS HUMANOS
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia2/pcRRHHVlan10.jpg" alt="drawing" width="600" height="400">
</p>


```sh
VLAN30: VENTAS
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia2/pcVentasVlan30.jpg" alt="drawing" width="600" height="400">
</p>


```sh
TODAS LAS VLANS
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia2/vlans.jpg" alt="drawing" width="600" height="400">
</p>


```sh
TABLA DE RUTEO 1
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia2/TablaRuteo1.jpg" alt="drawing" width="600" height="400">
</p>


```sh
TABLA DE RUTEO 2
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia2/TablaRuteo2.jpg" alt="drawing" width="600" height="400">
</p>





<div id='id5'/>

##  TOPOLOGIA3 [ ⇧](#content)


### Centro de Datos
Para esta topologia ise utilizo la red 192.168.25.0/24 la cual se administro en subredes para los departamentos que se mensionaron anteriormente.


 
  - Se crearon las VLANs correspondientes para realizar la configuración de los puertos, asignando el modo y VLAN correspondientes.
  - Se configuraron las rutas estáticas necesarias en R1 para que sea posible establecer comunicación entre el centro de datos y la oficina central


```sh
Imagen descriptiva de la Topologia 2
```
<p align="center">
  <img src="/Proyecto2/imagenes/topologia3/_topologia3.png" alt="drawing">
</p>


```sh
Para esta red se realizo el calculo que se describe a continuacion: 
192.168.25.0/24
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia3/calculos.png" alt="drawing">
</p>

```sh
ACCESS
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia3/access.png" alt="drawing">
</p>


```sh
VLANs
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia3/vlan.png" alt="drawing">
</p>


```sh
INTERVLANs
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia3/intervlan.png" alt="drawing">
</p>



```sh
RUTAS
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia3/rutas.png" alt="drawing">
</p>


```sh
VPC1
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia3/vpc1.png" alt="drawing">
</p>

```sh
VPC2
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia3/vpc2.png" alt="drawing">
</p>

```sh
VPC3
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia3/vpc3.png" alt="drawing">
</p>

```sh
VPC4
```
<p align="left">
  <img src="/Proyecto2/imagenes/topologia3/vpc4.png" alt="drawing">
</p>
