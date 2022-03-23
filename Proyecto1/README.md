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

<div id='indice'/>

## Requisitos:

Para la implementación de la topologia general, compuesta por las 3 siguientes topologias, se necesitan 3 maquinas fisicas, con gns3 instalado, donde a cada una de ellas se les asignará una topologia a representar, luego de esto, se necesita una cuenta en AWS donde se pueda crear una instancia de EC2, que hara la función de Servidor, para establecer la conexión a travez de la nube, esto implicaria que cada una de las máquinas, deben tener algun orquestador de redes, se recomienda openVPN, en el cual con el par de llaves, se podra tener acceso a la red, atravez de SSH, luego de estos requerimientos, se puede proceguir a la siguiente configuracion.

## Contenido

1. [Configuración de topologia 1](#id1)
2. [Configuración de topologia 2](#id2)
3. [Configuracion de topologia 3](#id3)
4. [Configuracion de la nube](#id4)
> ***Nota:*** ITodo esto se encuentra creado y configurado en un entorno de GNS3 y una Intancia en la nube de AWS. 

<div id='id1'/>

## 1. Configuración de Topología 1  [ ⇧](#indice)

Componentes:
  1. Vpcs
  2. Switch Ethelnet Capa 2
  3. Cloud

Su configuración final se ve de la siguiente manera, con respectivas etiquetas de configuración.

<img src="/Proyecto1/Imagenes/Top1/topologia1.jpg" alt="drawing">
&nbsp;
&nbsp;
Configuración de los Componentes de las topologias:

  1. Configuración de vcps:

<table>
 <tr>
  <td>
    Nombre VPC
    </td>
      
  <td>
    Configuración
    </td>
  </tr>
  <tr>
   <td>
    RRHH_1
    </td>
      
  <td>
   <img src="/Proyecto1/Imagenes/Top1/vpc_rrh1.jpg" alt="drawing">
    </td>
  </tr>
   <tr>
   <td>
    RRHH_2
    </td>
      
  <td>
   <img src="/Proyecto1/Imagenes/Top1/vpc_rrhh2.jpg" alt="drawing">
    </td>
  </tr>
   <tr>
   <td>
    CONTA_1
    </td>
      
  <td>
   <img src="/Proyecto1/Imagenes/Top1/vpc_conta1.jpg" alt="drawing">
    </td>
  </tr>
   <tr>
   <td>
    CONTA_2
    </td>
      
  <td>
   <img src="/Proyecto1/Imagenes/Top1/vpc_conta2.jpg" alt="drawing">
    </td>
  </tr>
   <tr>
   <td>
    VENTAS_1
    </td>
      
  <td>
   <img src="/Proyecto1/Imagenes/Top1/vpc_ventas1.jpg" alt="drawing">
    </td>
  </tr>
   <tr>
   <td>
    INFORMATICA_1
    </td>
      
  <td>
   <img src="/Proyecto1/Imagenes/Top1/vpc_info1.jpg" alt="drawing">
    </td>
  </tr>
  </table>








> ***Nota:*** Inicialmente, este dispositivo viene sin una configuración específica. 
>
> ![ConfiguracionDefecto](/Practica1/imagenes/img3.png "Configuracion por defecto VPC")


Mediante la utilización de la siguiente línea de comando, fue establecida la ***IP*** correspondiente a cada integrante. 

```sh
ip 192.168.12.x 255.255.255.0 192.168.12.1
```


Configuración de los Switch

<table>
<tr>
<td>
NOMBRE
</td>
<td>
CONFIGRUACION
</td>
</tr>
<tr>
<td>
ESW1
</td>
<td>
<img src="/Proyecto1/Imagenes/Top1/top1_esw1.jpg" alt="drawing">
</td>
</tr>
<tr>
<td>
ESW2
</td>
<td>
<img src="/Proyecto1/Imagenes/Top1/top1_esw2.jpg" alt="drawing">
</td>
</tr>
<tr>
<td>
ESW3
</td>
<td>
<img src="/Proyecto1/Imagenes/Top1/top1_Esw3.jpg" alt="drawing">
</td>
</tr>
</table>
<br/>

Configuración VLAN:
1. Antes de la Configuración:
No tiene VLans
    
<img src="/Proyecto1/Imagenes/Top1/vlnno.jpg" alt="drawing">
    
Por consecuencia no se puede establecer el estado
    
<img src="/Proyecto1/Imagenes/Top1/noesatus.jpg" alt="drawing">
  
2. Congifuración VLANS

<img src="/Proyecto1/Imagenes/Top1/WhatsApp Image 2022-03-22 at 11.33.15 PM (1).jpeg" alt="drawing"> 

3. Vlans configuradas

<img src="/Proyecto1/Imagenes/Top1/WhatsApp Image 2022-03-22 at 11.33.15 PM.jpeg" alt="drawing"> 

<br/>

Configuración VTP

<img src="/Proyecto1/Imagenes/Top1/configvtptop1.jpg" alt="drawing"> 

Conexión entre topologías:

<img src="/Proyecto1/Imagenes/Top1/WhatsApp Image 2022-03-22 at 11.33.15 PM (2).jpeg" alt="drawing"> 

<div id='id2'/>

## 2. Topología No.2  [ ⇧](#indice)

Resultado de la topología
<br/>
<img src="/Proyecto1/Imagenes/Top2/VPC.jpg" alt="drawing"> 
<br/>

1.Configuracion VPC
<br/>
<table>
<tr>
<td>
NOMBRE
</td>
<td>
CONFIGURACION
</td>
</tr>  
<tr>
<td>
INFORMATICA_2
</td>
<td>
<img src="/Proyecto1/Imagenes/Top2/VPC.jpg" alt="drawing"> 
</td>
</tr>  
</table>
<br/>
2.Configuracion Clientes
<br/>
<table>
<tr>
<td>
NOMBRE
</td>
<td>
CONFIGURACION
</td>  
<td>
RESULTADO
</td>
</tr>  
<tr>
<td>
CLIENTE_1
</td>
<td>
<img src="/Proyecto1/Imagenes/Top2/Cliente1_2.jpg" alt="drawing"> 
</td>
<td>
<img src="/Proyecto1/Imagenes/Top2/Cliente1_1.jpg" alt="drawing"> 
</td>
</tr>  
<tr>
<td>
CLIENTE_2
</td>
<td>
<img src="/Proyecto1/Imagenes/Top2/Cliente2_2.jpg" alt="drawing"> 
</td>
<td>
<img src="/Proyecto1/Imagenes/Top2/Cliente2_1.jpg" alt="drawing"> 
</td>
</tr>
<tr>
<td>
CLIENTE_3
</td>
<td>
<img src="/Proyecto1/Imagenes/Top2/Cliente3_2.jpg" alt="drawing"> 
</td>
<td>
<img src="/Proyecto1/Imagenes/Top2/Cliente3_1.jpg" alt="drawing"> 
</td>
</tr>  
</table>
<br/>

3.Configuracion Servers
<br/>
<table>
<tr>
<td>
NOMBRE
</td>
<td>
CONFIGURACION
</td>
</tr>  
<tr>
<td>
Server 1
</td>
<td>
<img src="/Proyecto1/Imagenes/Top2/Server1.jpg" alt="drawing"> 
</td>
</tr>
<tr>
<td>
Server 2
</td>
<td>
<img src="/Proyecto1/Imagenes/Top2/Server2.jpg" alt="drawing"> 
</td>
</tr>  
</table>
<br/>

4.Configuracion STP
<br/>
<table>
<tr>
<td>
NOMBRE
</td>
<td>
CONFIGURACION
</td>
</tr>  
<tr>
<td>
STP 1
</td>
<td>
<img src="/Proyecto1/Imagenes/Top2/STP1.jpg" alt="drawing"> 
</td>
</tr>
<tr>
<td>
STP 2
</td>
<td>
<img src="/Proyecto1/Imagenes/Top2/STP2.jpg" alt="drawing"> 
</td>
</tr>  
<tr>
<td>
STP 3
</td>
<td>
<img src="/Proyecto1/Imagenes/Top2/STP3.jpg" alt="drawing"> 
</td>
</tr>  

</table>

<br/>

<div id='id3'/>

## 3. Topología No.3  [ ⇧](#indice)
Resultado de la topología
<br/>
<img src="/Proyecto1/Imagenes/Top3/topo3.png" alt="drawing"> 
<br/>
1.Configuracion Servidores
<br/>
<table>
<tr>
<td>
NOMBRE
</td>
<td>
CONFIGURACION
</td>
</tr>  
 
<tr>
<td>
SERVIDOR_CONTA
<td>
<img src="/Proyecto1/Imagenes/Top3/server_conta.png" alt="drawing"> 
</td>
</tr>
<tr>
<td>
SERVIDOR_VENTAS
</td>
<td>
<img src="/Proyecto1/Imagenes/Top3/server_ventas.png" alt="drawing"> 
</td>
</tr>  
<tr>
<td>
SERVIDOR_RRHH
</td>
<td>
<img src="/Proyecto1/Imagenes/Top3/server_rrhh.png" alt="drawing"> 
</td>
</tr>  
<tr>
<td>
SERVIDOR_INFORMATICA
</td>
<td>
<img src="/Proyecto1/Imagenes/Top3/server_informatica.png" alt="drawing"> 
</td>
</tr>  
</table>
<BR/>
2.Configuracion Interfaces

<br/>

<table>
<tr>
<td>
NOMBRE
</td>
<td>
CONFIGURACION
</td>
</tr>  
 
<tr>
<td>
ESW8
<td>
<img src="/Proyecto1/Imagenes/Top3/ESW8-interfaces.png" alt="drawing"> 
</td>
</tr>
<tr>
<td>
ESW9
</td>
<td>
<img src="/Proyecto1/Imagenes/Top3/ESW9-interfaces.png" alt="drawing"> 
</td>
</tr>  
<tr>
<td>
ESW10
</td>
<td>
<img src="/Proyecto1/Imagenes/Top3/ESW10-interfaces.png" alt="drawing"> 
</td>
</tr>  
<tr>
<td>
ESW11
</td>
<td>
<img src="/Proyecto1/Imagenes/Top3/ESW11-interfaces.png" alt="drawing"> 
</td>
</tr>  
</table>
&nbsp;

3.Configuracion Vlans

<br/>

<table>
<tr>
<td>
NOMBRE
</td>
<td>
CONFIGURACION
</td>
</tr>  
 
<tr>
<td>
ESW8
<td>
<img src="/Proyecto1/Imagenes/Top3/ESW8-vlan.png" alt="drawing"> 
</td>
</tr>
<tr>
<td>
ESW9
</td>
<td>
<img src="/Proyecto1/Imagenes/Top3/ESW9-vlan.png" alt="drawing"> 
</td>
</tr>  
<tr>
<td>
ESW10
</td>
<td>
<img src="/Proyecto1/Imagenes/Top3/ESW10-vlan.png" alt="drawing"> 
</td>
</tr>  
<tr>
<td>
ESW11
</td>
<td>
<img src="/Proyecto1/Imagenes/Top3/ESW11-vlan.png" alt="drawing"> 
</td>
</tr>  
</table>
&nbsp;

4.Configuracion VTP

<br/>

<table>
<tr>
<td>
NOMBRE
</td>
<td>
CONFIGURACION
</td>
</tr>  
 
<tr>
<td>
ESW8
<td>
<img src="/Proyecto1/Imagenes/Top3/ESW8-vtp.png" alt="drawing"> 
</td>
</tr>
<tr>
<td>
ESW9
</td>
<td>
<img src="/Proyecto1/Imagenes/Top3/ESW9-vtp.png" alt="drawing"> 
</td>
</tr>  
<tr>
<td>
ESW10
</td>
<td>
<img src="/Proyecto1/Imagenes/Top3/ESW10-vtp.png" alt="drawing"> 
</td>
</tr>  
<tr>
<td>
ESW11
</td>
<td>
<img src="/Proyecto1/Imagenes/Top3/ESW11-vtp.png" alt="drawing"> 
</td>
</tr>  
</table>
&nbsp;

5.Configuracion Vlan transparente

&nbsp;

 <img src="/Proyecto1/Imagenes/Top3/ESW11-configuracion-VLAN-transparente.png" alt="drawing"> 
&nbsp;
 <img src="/Proyecto1/Imagenes/Top3/transparente.png" alt="drawing"> 
    


<div id='id4'/>

## 4. Configuración de nubes  [ ⇧](#indice)

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
