# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts. 
Herramienta de IA usada: (Claude) 

## Ejercicio 2: Tokens y ventana de contexto
| Texto | Caracteres | Tokens |
|-------|-------------|---------|
| Los estudiantes programan en Java. |35|8|
| The students program in Java. |29|6|
| desafortunadamente |18|4|
## Ejercicio 3: Temperatura
| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0 |100%|BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec|
| 0.5 |65.3%|BiblioTec, NubeDeTinta, BiblioTec, BiblioTec, LibroYa|
| 1 |44.5%|BiblioTec, NubeDeTinta, BiblioTec, BiblioTec, LibroYa|
| 1.8 |32.2%|LibroYa, PrestaLibro, NubeDeTinta, PaginaLibre, PrestaLibro|

A medida que sube la temperatura, el porcentaje de Bibliotec baja y aparecen mas nombres distintos entre los 5 intentos. EL simulador no inventa nombres nuevos porque solo elige entre los nombre que ya estan definidos en la lista.

## Ejercicio 4: Prompt vago vs estructurado 
| Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema |Si|Si|
| Menciona a los usuarios principales |No|Si|
| Tiene exactamente 3 funcionalidades |No|Si|
| Esta en 3 parrafos |No|Si|
| Lo usaria en un informe real |No|Si|

## Ejercicio 5: Anatomia de un prompt
| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol |Crea un programa en Java|
| Instruccion |Actua como desarrollador Java. Crea un programa en Java.|
| Contexto |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda.|
| Ejemplo |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda. usando una clase Producto con los atributos codigo, nombre, precio y stock. Explica primero la estructura de la clase y luego presenta el codigo Java. Usa este estilo para los metodos: getPrecio(), setPrecio(double precio).|
| Formato |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda. usando una clase Producto con los atributos codigo, nombre, precio y stock. Explica primero la estructura de la clase y luego presenta el codigo Java.|

Nivel 1: Me dijo que debia hacer el programa y me dio ejemplos.

Nivel 2: Al agregar el rol siguio preguntandome que debia hacer el programa.

Nivel 3: Al agregar el contexto, la IA me creao un ejemplo de gestion de productos de una tiempo mediante un menu en consola.

Nivel 4: Al agregar la instruccion me creo un ejemplo con la clase Producto con los atributos pedidos.

Nivel 5: Al agregar el formato, la IA explico la estructura de la clase antes de mostrar el codigo.

## Ejercicio 6: Del prompt basico al profesional
| Que revisar | Cumple (Si / No) |
|---|---|
| Esta escrito en Java y usa Swing? |Si|
| Pide correo y contrasena? |Si|
| Explica el funcionamiento antes o despues del codigo? |Si|
| El codigo esta organizado en clases? |Si|
| Valida los datos que ingresa el usuario? |Si|

```text
Actua como desarrollador Java. Crea un ejemplo de login para una
aplicacion de escritorio utilizando Swing. El usuario debe ingresar
correo y contrasena. Explica brevemente el funcionamiento y presenta
el codigo organizado por clases. 
Mejora el codigo anterior con estas restricciones: no uses librerias
externas, valida que el correo contenga @ y que la contrasena tenga
al menos 8 caracteres, y muestra los mensajes con JOptionPane.
```


