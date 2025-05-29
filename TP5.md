### Trabajo Práctico N°5: Parámetros

## Parámetros en funciones

Los **parámetros** permiten a las funciones recibir datos externos para trabajar con ellos. Sirven para **generalizar comportamientos** y hacer el código más reutilizable.

Podemos pensar en los parámetros como **variables locales** que representan la información que se envía al invocar una función.

Existen dos tipos de parámetros:
- **Formales:** Son los que aparecen en la definición de la función.
- **Reales o argumentos:** Son los valores que se pasan cuando se llama a la función.

### Modos de asociación

• **Por orden (posición):** El primer argumento se asigna al primer parámetro, y así sucesivamente.

```python

def quien_es(nombre, edad):
    print(f"{nombre} tiene {edad} años")

quien_es("Luis", 28)
```

• **Por nombre (clave-valor):** Los argumentos se indican usando el nombre del parámetro.

```python
quien_es(edad=28, nombre="Luis")
```

### Consideraciones

- En lenguajes **fuertemente tipados** como Java o Kotlin, se debe especificar el tipo del parámetro.
- En lenguajes **débilmente tipados** como Python o JavaScript, los parámetros pueden tomar cualquier tipo de dato.
- En algunos lenguajes **funcionales** (ej. Haskell), los argumentos se evalúan solo si se usan (**lazy evaluation**).

---

## Tipos de Binding en parámetros

| **Tipo de Binding**                             | **Definición**                                                                        | **Ej. estático (tiempo de compilación)**               | **Ej. dinámico (tiempo de ejecución)**                     |  
|--------------------------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------|------------------------------------------------------------|
| **Por valor**                             | Se copia el valor del argumento en el parámetro.                                       | `int x = 7; cambiar(x); // x sigue valiendo 7`         | `def cambiar(n): n += 1; cambiar(7)`                       |
| **Por tipo**                                     | El tipo del dato que puede aceptar el parámetro.                                       | `void imprimir(String texto)`                          | `def imprimir(texto): print(texto)`                       |
| **Por nombre**                                   | El nombre que se utiliza dentro de la función para referirse al argumento.             | `int sumar(int a, int b)`                              | `def sumar(a, b): return a + b`                           |
| **Por posición**                          | Cómo se enlazan los argumentos a los parámetros.                                       | `saludo("Ana", 22)`                                    | `saludo(nombre="Ana", edad=22)`                           |
| **Por referencia**                               | Se pasa la dirección de memoria, se puede modificar el argumento original.             | `void modificar(List& datos)` en C++                   | `def modificar(dic): dic["ok"] = True`                    |
| **Por evaluación**                               | Determina en qué momento se evalúa el argumento.                                       | `f(2 + 3)` evalúa `2 + 3` antes de llamar `f`          | `main = print (f (undefined))` en Haskell, se evalúa tarde |
