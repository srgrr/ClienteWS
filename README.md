# WSUtil 1.0.1
Este repositorio contiene el programa Java necesario para poder interactuar con el WebService del consorcio. Para mayor comodidad, de ahora en adelante nos referiremos a este programa como WSUtil.

## Pasos previos
### Instalación de Java
Para poder ejecutar este programa es necesario tener Java 8 instalado. Recomendamos instalar Java desde este link:

[Instalador de Java 8](https://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html)

### Comprobar la instalación de Java 
Para comprobar que Java está bien instalado podemos abrir una consola de comandos (o CMD) y escribir el comando `java -version`.

[Cómo abrir una consola de comandos](https://es.wikihow.com/abrir-la-l%C3%ADnea-de-comandos-en-Windows)

La salida producida por el comando `java -version` debería ser muy similar a la siguiente:

```
java version "1.8.0_221"
Java(TM) SE Runtime Environment (build 1.8.0_221-b11)
Java HotSpot(TM) 64-Bit Server VM (build 25.221-b11, mixed mode)
```

Si la versión indicada difiere en los últimos números no debemos preocuparnos. Lo único que importa es que la versión empiece por 1.8.
Si en lugar de una salida así obtenemos un mensaje indicando que no se reconoce el comando Java será necesario volver al paso anterior.

## Instalar WSUtil

## Configurar WSUtil
Una vez instalado el programa Java será necesario poner nuestras credenciales en el fichero de configuración. Para ello iremos al directorio donde hayamos dejado el programa, abriremos el fichero `config.properties` ubicando en el directorio `resources` y pondremos nuestro nombre de usuario y contraseña en los campos indicados, sin dejar ningún espacio entre el signo de igual y el primer caracter de estos valores. Podemos tomar de ejemplo los campos ya rellenados, como las diferentes direcciones a los diferentes servicios. 

## Utilizando WSUtil
Para utilizar WSUtil debemos emplear los siguientes comandos. Estos comandos pueden ejecutarse en una consola o desde otro lenguaje de programación.

Como observación, si el lugar desde el que llamamos al programa no es la misma carpeta que lo contiene deberemos poner la ubicación o path absoluto.

Un path absoluto es aquel que no tiene en cuenta el directorio desde donde se está y siempre se refiere a la misma ubicación.

Por ejemplo `resources/config.properties` no es un path absoluto, mientras que `C://users/juanito/programajava/resources/config.properties` sí lo es.

Si las rutas hacia los ficheros contienen espacio debemos rodear los nombres entre comillas.

### GET
```
java -jar WSUtil-1.0.1.jar --service-name=get --get-codigo-perito=codigo_perito --get-expediente=expediente --get-informweb=informeweb --output-path=path_a_fichero_salida
```

### Base64
```
java -jar WSUtil-1.0.1.jar --service-name=base64 --input-path=path_a_fichero_entrada --output-path=path_a_fichero_salida
```

### Base64 (decodificar)
```
java -jar WSUtil-1.0.1.jar --service-name=base64decode --input-path=path_a_fichero_entrada --output-path=path_a_fichero_salida
```

### Registrar formulario
```
java -jar WSUtil-1.0.1.jar --service-name=registrarFormulario --input-path=path_a_fichero_entrada --output-path=path_a_fichero_salida
```

### Solicitar informe
```
java -jar WSUtil-1.0.1.jar --service-name=solicitarInforme --input-path=path_a_fichero_entrada --output-path=path_a_fichero_salida
```

### Subir formulario
```
java -jar WSUtil-1.0.1.jar --service-name=subirDocumentoFormulario --input-path=path_a_fichero_entrada --output-path=path_a_fichero_salida
```

### Validar formulario
```
java -jar WSUtil-1.0.1.jar --service-name=validar --input-path=path_a_fichero_entrada --output-path=path_a_fichero_salida
```

## Errores con WSUtil
Cuando WSUtil no funcione bien aparecerá un fichero `WSUtil.err` en la carpeta de instalación del programa.

Podéis enviar este fichero por correo o bien abrir un ticket en este mismo repositorio adjuntando el contenido de dicho fichero.