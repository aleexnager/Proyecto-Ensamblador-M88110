>[!WARNING]\
>[!WARNING]\
># AVISO
>El plagio o intento de copia de este material en el proyecto de la asignatura de Estructura de Computadores supondrá un suspenso inmediato. Este contenido es únicamente informativo y de uso didáctico, los autores de este proyecto no nos hacemos responsables del mal uso que se le pueda dar al contenido de este repositorio. ([LICENSE](/LICENSE))

# Proyecto Estructura de Computadores (ETSIINF-UPM)
Proyecto de programación en ensamblador M88110

## Autores
[Diego Vigneron Olmos](https://github.com/diegovoos)

[Alejandro Náger Fernández-Calvo](https://github.com/aleexnager)

## Herramientas
El MC88110 es un microprocesador RISC superescalar que forma parte de la familia 88000 de Motorola. Es capaz de iniciar dos instrucciones cada ciclo de reloj, respetando siempre la apariencia de ejecución secuencial del programa a través del mecanismo de pipeline del secuenciador. Las instrucciones se despachan hacia diez unidades funcionales que trabajan en paralelo.

El simulador del MC88110 que se utiliza en este proyecto permite configurar distintos parámetros de la memoria principal, de las memorias cache de instrucciones y datos y de la CPU.

El proyecto se realizará utilizando el ensamblador nativo del 88110 y empleando la configuración del fichero serie que se incluye en la distribución. Este fichero configura la CPU según los siguientes parámetros:

- Cache de datos e instrucciones inhibidas
- Memoria de un solo bloque con tiempo de acceso de 10 ciclos.
- Ejecución serie.
- Ordenamiento de bytes en memoria little-endian.
- Modo de redondeo al más cercano.

```
- 88110ins: Programa que permite generar o modificar un fichero de configuración. 
 
- paralelo: Fichero de configuración de un computador superescalar con cache de instrucciones y datos. 
 
- INSTALL: ShellScript que instala la aplicación. Además genera el script mc88110 que invoca al emulador 
          con el fichero de configuración serie. Se invoca con ./INSTALL ó sh INSTALL
```
## Compilar y ejecutar un programa principal
Para poder probar el códgio hay que quitar los comentarios en los datos y el programa principal (_PPALX_) que se quiera ejecutar.

- Compilar:
```
88110e -e PPALX -ml -o CDV CDV.ens
```
- Ejecutar:
```
mc88119 CDV
```
Para más información, consulta el manual.

## Manual
[Manual 88110](/doc/Manual88110.pdf)

## Instalación
[Instalación](/doc/instala.pdf)

## Enunciado del proyecto
[Enunciado](/doc/enunciado.pdf)

## Presentación del proyecto
[Presentación](/doc/presentacion.pdf)
