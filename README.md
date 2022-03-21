Enum Types: Arnold se está cociendo
===================================

Fecha límite de entrega: 21 de marzo, en tu GitHub.

Esta semana vamos a introducir un nuevo concepto de la programación, los **tipos enumerados**. Son muy sencillos y no necesitan mucha explicación. Eso sí, son un ejemplo fantástico del **patrón singleton**, y resuelven muchos problemas en la vida real TM.

Recomiendo leer el **capítulo 18 "Enum Types" del Libro _Beginning Java 8 Fundamentals_ Subrayado**. Están explicados a través de un par de ejercicios que recomiendo ir codificando en vuestro editor favorito `IntelIJ throws FileNotSupportedException`

Además, vamos a hacerlo "tipo examen", para ir practicando para el de junio:
 - He incluido los casos test que ha de pasar vuestro código.
 - He incluido el programa principal.
  
De esta manera, nos aseguramos que aprendéis todo lo que es necesario saber sobre tipos enumerados, y aprendéis las **_fluent assertions_**, que harán vuestros casos test más optimos. Ojo que el día del examen las usaré.


## Ejercicio

Se trata de calcular el peso de una persona en los distintos planetas de nuestro Sistema Solar*, al estilo de este sitio web:

http://www.traducimos.cl/planet/

Es importante para evitar que os pase lo de Arnold en Desafio Total** cuando salió a dar un paseíto por la superficie marciana, estando de cuarentena como estábamos en marzo de 2019:

https://www.youtube.com/watch?v=86scPKqWFvc

El peso en otro planeta se lo preguntáis a los que han estudiado Física en la universidad o bachiller (call @Arturo @JoanNIcolau y cia) y así no tenéis que programar esta semana. Si no se lo saben de memoria, aplicad este sencilla fórmula:

`Peso_en_Superficie = tu_Masa * Gravedad_en_superficie`

donde 

`Gravedad_en_superficie = G * Masa_del_planeta / Radio_del_planeta_al_cuadrado`

donde: 

`G = 6.67300E-11`

y 

`tu_masa = tu_peso_en_la_Tierra / gravedad_superficial_tierra`

Los valores de masa y radio de cada planeta (en `Kg` y `m` respectivamente) son:
```
MERCURY (3.303e+23, 2.4397e6),     
VENUS   (4.869e+24, 6.0518e6),     
EARTH   (5.976e+24, 6.37814e6),     
MARS    (6.421e+23, 3.3972e6),     
JUPITER (1.9e+27,   7.1492e7),     
SATURN  (5.688e+26, 6.0268e7),     
URANUS  (8.686e+25, 2.5559e7),     
NEPTUNE (1.024e+26, 2.4746e7);      
```

La salida del programa en consola es esta (sirve también como caso test), donde 175 es tu peso en la Tierra:

`tu_masa = tu_peso_en_la_Tierra / gravedad_superficial_tierra;`

```sh
$ java Planet 175 
Your weight on MERCURY is 66.107583 
Your weight on VENUS is 158.374842 
Your weight on EARTH is 175.000000 
Your weight on MARS is 66.279007 
Your weight on JUPITER is 442.847567 
Your weight on SATURN is 186.552719 
Your weight on URANUS is 158.397260 
Your weight on NEPTUNE is 199.207413
```

## Casos test - AssertJ Fluent Assertions

Aquí tienes los casos test que ha de satisfacer tu código:

https://github.com/dfleta/arnold-enum-type/blob/main/src/test/java/org/foobarspam/arnoldEnumType/test/ArnoldEnumTypeTest.java 

Para utilizar estos casos test, has de incluir en el `POM.xml` del proyecto Maven o en el fichero `build.gradle` una dependencia adecuada a la librería de **AssertJ**. Búscala en el repo de Maven:

https://mvnrepository.com/

¿Cómo funcionan las Fluent Assertions?:

http://joel-costigliola.github.io/assertj/assertj-core-quick-start.html


## Script principal - main

Programa la lógica para que, además de los casos test, satisfaga este script principal del programa:

https://github.com/dfleta/arnold-enum-type/blob/main/src/main/java/org/foobarspam/arnoldEnumType/main/ArnoldMain.java

### Solución

Resuelto por mi:

https://github.com/dfleta/Java/tree/master/arnoldEnumTypeMaven

Resuelto por Oracle:

https://docs.oracle.com/javase/tutorial/java/javaOO/enum.html

------
* ¿Y Plutón? ¿Dónde está Plutón?  

Pluto is not a planet! You can't kill the truth, father!
https://www.youtube.com/watch?v=S4E2ZuPCBG0
https://www.youtube.com/watch?v=X46NN3BdvcA

------
** Existe una versión mucho más divertida, ingeniosa y edificante de la infame película Desafío Total en el capítulo 4 de la temporada 2 de Rick and Morty, titulado "Total Rickall". Eso sí, tiros y vísceras hay a partes iguales:

https://www.youtube.com/watch?v=bnLqIJxNiAk