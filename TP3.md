## Trabajo Práctico N°3: Lenguajes esotéricos

### Objetivos

Armar la GIC, BNF, EBNF y ABNF para un lenguaje esotérico. 

El lenguaje elegido es **Deadfish**.

### Descripción General
**Deadfish** es un lenguaje de programación esotérico creado en 2006 por Jonathan Todd Skinner, diseñado específicamente para ser minimalista y deliberadamente frustrante. Su principal característica es su extrema simplicidad sintáctica combinada con un comportamiento semántico restrictivo.

### Comandos válidos
  - `i`: Incrementa la variable `x` en 1
  - `d`: Decrementa la variable `x` en 1
  - `s`: Eleva `x` al cuadrado
  - `o`: Muestra el valor actual de `x`

### GIC

```gic
S -> λ | C
C -> iC | dC | sC | oC | i | d | s | o
```

### BNF

```bnf
<Program> ::= <Command>*
<Command> ::= i | d | s | o
```

### EBNF

```ebnf
<Program> ::= { <Command> }
<Command> ::= i | d | s | o
```

### ABNF

```abnf
Program: Command _op
Command:    i
            d
            s
            o
``` 



### Ejemplo de ejecución

``` deadfish
iisiiiisiiiiiiiio
iiiiiiiiiiiiiiiiiiiiiiiiiiiiio
iiiiiiioo
iiio
dddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddo
dddddddddddddddddddddsddo
ddddddddo
iiio
ddddddo
ddddddddo
>>> 7210110810811132119111114108100
```

El valor de 'x' se va acumulando a lo largo de la ejecución del programa. En este caso, el resultado final es `7210110810811132119111114108100`. Éste resultado si utilizamos su valor en ASCII sería `Hello World!`.