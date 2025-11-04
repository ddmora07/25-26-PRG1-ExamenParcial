# Examen Parcial - ddmora07

**Usuario GitHub:** ddmora07
**Fecha:** 4 de noviembre de 2025
**Retos tenidos en cuenta:** Reto 003

---

## Instrucciones

A continuación encontrarás fragmentos de código extraídos de tus entregas. Cada fragmento contiene una o más situaciones relacionadas con los conceptos vistos en clase.

Para cada pregunta debes:
1) Identificar a qué se refiere la observación
2) Explicar si es o no un error y por qué
3) Proponer la corrección

Nota: Responde 5 de las 10 preguntas (en función a lo indicado en el examen).


---

## Pregunta 1

Archivo: `Edificiointereactivo.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/166e129d4c0c4cf46f752f8011ed5a2626eb42ec/entregas/moraDaniel/Edificiointereactivo.java) (Reto 003)

```java
class Edificiointereactivo {
    public static void main(String[] args) {
        // ...
    }
}
```

¿Qué observas en este código?
En este codigo observamos su parte inicial en la cual estamos nombrando a la clase como Edificointeractivo lo cual es un nombre muy poco específico y no nos queda claro para que estamos creando este código . Es ambiguo no apunta al problema que queremos resolver . Es un error por comoo he dicho debemos ser muy específicos y intencionales a la hora de declarar nuestras clases . Una propuesta sería class VentanasEnLaSemanaDeUnHotel por ejemplo , aunque es largo nos deja claro para que sirve el código . 

---

## Pregunta 2

Archivo: `Edificiointereactivo.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/166e129d4c0c4cf46f752f8011ed5a2626eb42ec/entregas/moraDaniel/Edificiointereactivo.java) (Reto 003)

```java
while (dia <= DIAS) {
    int consumoDia = 0;
    // ...
    int hora = 0;
    while (hora < HORAS) {
        // ...
        hora++;
    }
}
```

¿Qué observas en este código?
Este error es un error que ya me has señalado que es en el mal uso de la  estructura de control repetitiva`while` para iterar (sobre días y horas). La variable dia no se incrementa dentro del bucle externo lo que lo hace que pueda ser infinito .La declaración de el nombre de las variables es poco descriptivo y pobre lo que no facilita la lectura del codigo y no le da claridad . Y para este ejercicio en vez de `while` se podría usar la estructura `for` lo que lo haría más claro y más eficiente , En donde pondríamos `for ( inicialización ; condición ; incremento ) { ` lo usaríamos para días y horas ahorrandonos los errores y confusiones en el código . 

---

## Pregunta 3

Archivo: `Edificiointereactivo.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/166e129d4c0c4cf46f752f8011ed5a2626eb42ec/entregas/moraDaniel/Edificiointereactivo.java) (Reto 003)

```java
if (hayRayo && c == columnaRayo) {
    celda = "[X]";
} else if (hayMantenimiento && p == plantaMantenimiento && hora >= horaMantenimiento) {
    celda = "[#]";
} else if (persianaAbierta && luzEncendida) {
    celda = "[*]";
    consumoDia++;
} else if (persianaAbierta && !luzEncendida) {
    celda = "[º]";
} else {
    celda = "[ ]";
}
```

¿Qué observas en este código?
En este código se puede observar un fallo típico a la hora de resolver un problema en el cual tenemos como que " dibujar" código , Estoy poniendo muchas líneas de celda y cambiando su valor constantemente lo cual está mal hecho . lo que debería de hacer es antes de el estructura de control if , Declarar los diferentes tipos de celdas para lo que usaríamos un `final int PERSIANA_ABIERTA = " Los diferentes tipos de de celdas que podemos usar" ; ` por ejemplo . y luego tendríamos que a `celda = PERSIANA_ABIERTA ` Y así al final de la estructura pondríamos `System.out.println(celda) ; ` y ya nos quedaría resuelto en vez de para cada caso darle un valor diferente a la celda . También veo otro error en la declaración de las estructuras de control en donde la condición estoy usando variables la cuales no quedan definidas , no se que significan como por ejemplo `c` ` p ` lo cual hace que el código no quede claro y dificulte su lectura y compresión 




---

## Pregunta 4

Archivo: `Edificiointereactivo.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/166e129d4c0c4cf46f752f8011ed5a2626eb42ec/entregas/moraDaniel/Edificiointereactivo.java) (Reto 003)

```java
System.out.println("Dia " + dia + " - " + hora + ":00  Consumo hora: " + consumoDia);
```

¿Qué observas en este código?

---

## Pregunta 5

Archivo: `Edificiointereactivo.java` — [Ver archivo](https://github.com/mmasias/25-26-PRG1/blob/166e129d4c0c4cf46f752f8011ed5a2626eb42ec/entregas/moraDaniel/Edificiointereactivo.java) (Reto 003)

```java
System.out.println("Media semanal: " + (consumoTotalSemana / 7));
```

¿Qué observas en este código?

---

## Pregunta 6

Archivo: `UnEdificio.java` — [PRs del alumno](https://github.com/mmasias/25-26-PRG1/pulls?q=is%3Apr+author%3Addmora07+is%3Aall) (Reto 003, línea 10)

```java
final String LADRILLOS = ":";
```

¿Qué observas en este código?

---

## Pregunta 7

Archivo: `UnEdificio.java` — [PRs del alumno](https://github.com/mmasias/25-26-PRG1/pulls?q=is%3Apr+author%3Addmora07+is%3Aall) (Reto 003, líneas 15-16)

```java
int numeroEncendidas=0;
int totalGastodia=0;
```

¿Qué observas en este código?

---

## Pregunta 8

Archivo: `UnEdificio.java` — [PRs del alumno](https://github.com/mmasias/25-26-PRG1/pulls?q=is%3Apr+author%3Addmora07+is%3Aall) (Reto 003, líneas 27-40)

```java
for (int columna = 1; columna <= 7; columna++) {
    for (int fila = 1; fila <= 7; fila++) {

        abierta = Math.random() < PROBABILIDAD_PERSIANA_ABIERTA;
        encendida = Math.random() < PROBABILIDAD_LUZ_ENCENDIDA;
        if (fila == 4) {
            System.out.print(ASCENSOR);
        } else {
            System.out.print(
                    LADRILLOS + (!abierta ? VENTANA_CERRADA : encendida ? LUZ_ENCENDIDA : LUZ_APAGADA)
                            + LADRILLOS);
            if(abierta && encendida){
                numeroEncendidas++;
                totalGastodia++;
            }
```

¿Qué observas en este código?

---

## Pregunta 9

Archivo: `UnEdificio.java` — [PRs del alumno](https://github.com/mmasias/25-26-PRG1/pulls?q=is%3Apr+author%3Addmora07+is%3Aall) (Reto 003, línea 30)

```java
abierta = Math.random() < PROBABILIDAD_PERSIANA_ABIERTA;
```

¿Qué observas en este código?

En este fragmento observo dos fallos el primero es que no estoy declarando el tipo de dato que estamos usando , de los que conocemos solemos usar los llamados primitivos y para esta línea deberíamos usar un int o un double ya que se trata de un número . Segundo error posible es el nombre de la variable  : no explica nada el nombre `abierta` debería ser persianaAbierta ya que así queda claro para que sirve esta variable . Nuestro código quedaría así `int persianaAbierta =` . Muy importante para declarar esta variable usamos `camel case` que sirve para dar cierto formato a las variables y para este tipo es el que solemos usar en donde la primera letra es mínuscula siempre siempre siempre ... y si queremos poner otra palabra ya empieza en mayúsculas


---

## Pregunta 10

Archivo: `UnEdificio.java` — [PRs del alumno](https://github.com/mmasias/25-26-PRG1/pulls?q=is%3Apr+author%3Addmora07+is%3Aall) (Reto 003, línea 4)

```java
public class UnEdificio {
```

¿Qué observas en este código?
En el inicio del código para la declaración de la clase he usado el public class lo cual está "prohibido" ya que como se ha explicado en clase no es necesario para los retos que estamos abordando actualmente , sería usar más recursos de los necesarios ya que esto sirve para conectar diferentes proyectos y la información de la clase actual usarla en otro , cosa que actualmente no nos hace falta .
