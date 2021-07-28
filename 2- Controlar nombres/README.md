# Validar nombres

Tener en cuenta las siguientes definiciones
1) El termino ingresado pueden ser iniciales o palabras completas
2) Una inicial es solo un caracter mas un punto
3) Una palabra se comprende de 2 o mas caracteres, sin punto.

Un nombre Válido se puede escribir de alguna de las siguientes formas:
- E. Poe
- E. A. Poe
- Edgard Allan Poe
- Edgard A. Poe

Los siguientes ejemplos son inválidos:
- Edgard (solo nombres o apellidos no son validos)
- E Poe o E. A Poe (las iniciales deben contener un punto)
- e. Poe o E. poe o e. a. Poe (sin mayúsculas)
- E. Allan Poe (el segundo nombre completo, mientras que el primero es solo una inicial)
- E. A. P. (el apellido no es una palabra completa)
- Edg. A. Poe (la inicial debe ser una sola letra)

### Reglas
1) Tanto las iniciales como las palabras completas deben estar capitalizadas (la primera letra en mayúsculas)
2) Las iniciales deben terminar en punto (.)
3) Solo habrán 2 o 3 términos en el ingreso. Es decir, o dos nombres y un apellido o solo un nombre y un apellido
4) Si se ingresan dos nombres y un apellido, los dos primeros pueden ser iniciales, o solo el segundo. Nunca puede ser una inicial el primer nombre y no el segundo
5) El apellido siempre debe ser una palabra completa

LA tarea consiste en escribir una función que, siguiendo las reglas anteriores, devuelva si un
nombre es válido (true) o no (false). Ejemplos:
- ValidName("E. Poe") ➞ true
- ValidName("E. A. Poe") ➞ true
- ValidName("Edgard A. Poe") ➞ true
- ValidName("Edgard") ➞ false //deben ser 2 o tres palabras
- ValidName("e. Poe") ➞ false // capitalizacion
- ValidName("E Poe") ➞ false // falta el punto detrás de la inicial
- ValidName("E. Allan Poe") ➞ false // no es valido: inicial como primer nombre y palabra como segundo
- ValidName("E. Allan P.") ➞ false // Apellido como inicial
- ValidName("Edg. Allan Poe") ➞ false // Las palabras no pueden finalizar con punto (solo iniciales)