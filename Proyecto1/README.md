><img src="https://upload.wikimedia.org/wikipedia/commons/4/4a/Usac_logo.png" alt="drawing" width="100">
>
>Universidad San Carlos de Guatemala
>
>Facultad de Ingeniería 
>
>Escuela de Ciencias y Sistemas 
>
>Primer Semestre, 2022
>
>Laboratorio de Redes de Computadoras 1 Sección *N Impares*

### Grupo No.2

Integrantes:

| Nombre                               | Carnet    | Estudiante* |
| ------------------------------------ | --------- | ----------- |
| <img src="/Practica1/imagenes/icon.png" alt="icon_m" width="25"> &nbsp; Josué Alfredo González Caal          | 201602489 | 1 |
| <img src="/Practica1/imagenes/icon.png" alt="icon_m" width="25"> &nbsp;Jimmy Yorbany Noriega Chávez          | 200915691 | 2 |
| <img src="/Practica1/imagenes/icon.png" alt="icon_m" width="25"> &nbsp; Melyza Alejandra Rodríguez Contreras | 201314821 | 3 |
| <img src="/Practica1/imagenes/icon.png" alt="icon_m" width="25"> &nbsp; Romael Isaac Pérez Godinez           | 201213545 | 4 |


# Proyecto No.1

# Práctica 1

<div id='indice'/>

## Contenido

1. [Configuración de *VPCs*](#id1)
2. [Configuración de nubes](#id2)
3. [*Ping* entre *hosts*](#id2)

<div id='id1'/>

## 1. Configuración de *VPCs*  [ ⇧](#indice)

Para este apartado se utilizó el componente ***VPC*** integrado nativamente en **GNS3**.

<img src="/Practica1/imagenes/img2.png" alt="drawing">
&nbsp;
&nbsp;
<img src="/Practica1/imagenes/img1.png" alt="drawing">



> ***Nota:*** Inicialmente, este dispositivo viene sin una configuración específica. 
>
> ![ConfiguracionDefecto](/Practica1/imagenes/img3.png "Configuracion por defecto VPC")


Mediante la utilización de la siguiente línea de comando, fue establecida la ***IP*** correspondiente a cada integrante. 

```sh
ip 192.168.12.x 255.255.255.0 192.168.12.1
```
- **Estudiante 1**

```sh
ip 192.168.12.10 255.255.255.0 192.168.12.1
```
![VPC1](/Practica1/imagenes/img7.jpeg "Configuracion VPC1")

- **Estudiante 2**

```sh
ip 192.168.12.20 255.255.255.0 192.168.12.1
```

![VPC2](/Practica1/imagenes/img6.jpg "Configuracion VPC2")

- **Estudiante 3**

```sh
ip 192.168.12.30 255.255.255.0 192.168.12.1
```
![VPC3](/Practica1/imagenes/img4.png "Configuracion VPC3")

![VPC3](/Practica1/imagenes/img5.png "Configuracion VPC3")

- **Estudiante 4**

```sh
ip 192.168.12.40 255.255.255.0 192.168.12.1
```
![VPC4](/Practica1/imagenes/img8.jpeg "Configuracion VPC4")

<div id='id2'/>

## 2. Configuración de nubes  [ ⇧](#indice)

Para lograr la configuración de las nubes que permitieron la comunicación entre los integrantes del grupo, se empleó el componente ***Cloud***, este pertenece a los componenetes que **GNS3** nos brinda por defecto.

<img src="/Practica1/imagenes/img2.png" alt="drawing">
&nbsp;
&nbsp;
<img src="/Practica1/imagenes/img9.png" alt="drawing">

Se realizaron las siguientes configuraciones, por ejemplo, entre el **Estudiante 2** y el **Estudiante 3**.

- Creación de un **Tunel UDP** con los puertos ***Local*** y ***Remoto*** de forma cruzada.

<img src="/Practica1/imagenes/img10.jpg" alt="drawing" width="50%">

> El **Estudiante 2** configuró los puertos ***Local***=30000 y ***Remoto***=20000

<img src="/Practica1/imagenes/img13.png" alt="drawing" width="50%">

> El **Estudiante 3** configuró los puertos ***Local***=20000 y ***Remoto***=30000 
> 
> Ambas **IP** fueron proporcionadas por el servidor de ***VPN*** en uso.

Cada uno de los integrantes del grupo realizó esta configuración apuntando hacia el resto de sus compañeros. A continuación, se muestra el resultado de las topologías implementadas en **GNS3**.

- **Estudiante 1**

![CE1](/Practica1/imagenes/cloude1.jpg "Cloud estudiante 1")

- **Estudiante 2**

![CE2](/Practica1/imagenes/cloude2.jpg "Cloud estudiante 2")

- **Estudiante 3**

![CE3](/Practica1/imagenes/cloude3.jpg "Cloud estudiante 3")

- **Estudiante 4**

![CE4](/Practica1/imagenes/cloude4.jpg "Cloud estudiante 4")

<div id='id3'/>

## 3. *Ping* entre *hosts*  [ ⇧](#indice)

Para corroborar que las configuraciones realizadas anteriormente se hayan llevado a cabo de manera correcta, realizamos ***Ping*** entre cada uno de los miembros del grupo, utilizando el comando descrito a continuación.

Desde la consola de la **VPC** de cada integrante, escribimos: 

```sh
ping 192.168.12.x
```

> Donde ***x*** representa la **IP** de la **VPC** del integrante al que se le desea hacer ***Ping***. Esta **IP** fue configurada en la sección [Configuración de *VPCs*](#id1).

- ***Ping*** entre **Estudiante 2** y el resto de integrantes.

![PingEstudiante2](/Practica1/imagenes/ping1.jpeg "Ping estudiante 2")

- ***Ping*** entre **Estudiante 3** y el resto de integrantes.

![PingEstudiante3](/Practica1/imagenes/ping3.png "Ping estudiante 3")

![PingEstudiante3](/Practica1/imagenes/ping2.png "Ping estudiante 3")

![PingEstudiante3](/Practica1/imagenes/ping4.png "Ping estudiante 3")
