# Tarea: Mi prompt profesional

## Funcionalidad elegida

Un programa en Java que calcule el promedio de las notas de un alumno
y determine si aprobo o desaprobo.

## Version 1: prompt basico

```text
Hazme un programa que calcule notas.
```
la IA asumio informacion que nunca le di. Eligio Python sin que
se lo pidiera, invento 4 notas con pesos especificos (15%, 20%, 25%, 40%)
y establecio por su cuenta que la nota minima para aprobar es 11. Nada de
esto fue indicado en el prompt; el resultado fue impredecible.

## Version 2

```text
Crea un programa en Java que calcule el promedio de 3 notas de un
alumno (ingresadas por teclado) y me diga si aprobo o desaprobo,
sabiendo que la nota minima para aprobar es 11.
```
Que cambie: agregue contexto e instruccion especifica. Que mejoro: la IA ya no asumio el lenguaje ni el criterio, genero exactamente lo pedido con Scanner y la logica if/else correcta. Que le falta: no tiene un rol definido, no explica el funcionamiento antes del codigo, no valida que las notas esten en un rango valido (ej. 0 a 20), y el codigo no esta organizado en varias clases ni metodos separados.

## Version 3: prompt final

```text
Actua como profesor de programacion en Java. Crea un programa que calcule
el promedio de 3 notas de un alumno (rango valido de 0 a 20) y determine
si aprobo o desaprobo, sabiendo que la nota minima para aprobar es 11.
Usa Scanner para leer los datos por teclado y organiza el codigo en un
metodo separado llamado calcularPromedio(). No uses librerias externas.
Explica primero el funcionamiento del programa en 2 lineas y luego
presenta el codigo Java completo.
```
Que cambie: agregue el rol (profesor de programacion), el formato (explicar
antes del codigo) y una restriccion explicita (no usar librerias externas).
Que mejoro: la IA valido el rango de las notas con bucles do-while, organizo
el calculo en un metodo separado calcularPromedio() tal como se pidio, y
explico brevemente el funcionamiento antes de mostrar el codigo. Este fue
el prompt mas completo y el que menos tuvo que adivinar.

## Componentes del prompt final

| Componente | Texto de mi prompt |
|------------|---------------------|
| Rol | Actua como profesor de programacion en Java |
| Instruccion | Crea un programa que calcule el promedio de 3 notas de un alumno y determine si aprobo o desaprobo |
| Contexto | rango valido de 0 a 20, la nota minima para aprobar es 11, usa Scanner para leer los datos por teclado, organiza el codigo en un metodo separado llamado calcularPromedio() |
| Ejemplo | Ejemplo de salida esperada: Promedio: 15.3 / Resultado: APROBADO |
| Formato | Explica primero el funcionamiento del programa en 2 lineas y luego presenta el codigo Java completo |

## Evaluacion del resultado

| Que revisar | Cumple (Si / No) |
|---|---|
| Esta escrito en Java? | Si |
| Valida que las notas esten entre 0 y 20? | Si |
| El calculo esta organizado en un metodo separado? | Si |
| Explica el funcionamiento antes del codigo? | Si |
| No usa librerias externas? | Si |
| La salida coincide con el ejemplo pedido? | Si |

## Errores que evite

**Ser demasiado general:** en la version 1 mi prompt era muy general
("Hazme un programa que calcule notas") y la IA tuvo que asumir todo
(el lenguaje, la cantidad de notas, los pesos y el criterio de aprobacion).
Lo evite en la version 3 dando instrucciones especificas: cantidad de
notas, rango valido, criterio de aprobacion y nombre del metodo.

**No indicar el formato:** en las primeras versiones no especifique
como debia presentarse la respuesta ni un ejemplo de salida. En la
version 3 pedi explicitamente que explicara el funcionamiento antes
del codigo y agregue un ejemplo de salida esperada, lo que hizo la
respuesta mas ordenada y predecible.