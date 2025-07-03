
# 📘 Lenguaje **Elysion**

## 🎯 Objetivo
**Elysion** es un lenguaje esotérico diseñado con fines didácticos y de análisis formal. A diferencia de otros lenguajes esotéricos minimalistas, **su sintaxis es clara y expresiva**, pensada para ser fácil de entender, leer y extender.

---

## 🧠 Filosofía

- Sintaxis amigable y de alta legibilidad.
- Tipado estático y obligatorio.
- Control de flujo estructurado (sin saltos).
- Inspirado en pseudocódigo académico.
- Se ejecuta entre `inicio` y `fin`.

---

## 🔠 Tipos de Datos

`texto`, `entero`, `booleano`, `decimal`

**Ejemplos:**
```Elysion
mensaje: texto = "Hola"
contador: entero = 10
activo: booleano = verdadero
pi: decimal = 3.14
```

---

## 🔧 Asignación y Variables

```Elysion
nombre: texto = "Ana"
edad: entero = 25
```

Reasignación:
```Elysion
edad = 26
```

---

## 🔁 Bucles

```Elysion
repetir i desde 0 hasta 10 {
  mostrar(i)
}
```

O también:

```Elysion
mientras edad < 30 {
  edad = edad + 1
}
```

---

## 🔀 Condicionales

```Elysion
si edad >= 18 {
  mostrar("Mayor de edad")
} sino {
  mostrar("Menor de edad")
}
```

---

## ✨ Funciones

```Elysion
funcion sumar(a: entero, b: entero): entero {
  resultado: entero = a + b
  retornar resultado
}
```

Llamada:

```Elysion
total: entero = sumar(10, 5)
```

---

## 📢 Entrada / Salida

```Elysion
leer(nombre)
mostrar("Hola " + nombre)
```

---

## 📐 BNF (fragmento)

```bnf
<programa> ::= inicio <bloques>* fin

<bloques> ::= <declaracion> | <asignacion> | <condicional> | <bucle> | <funcion> | <llamada> | <io>

<declaracion> ::= <identificador>: <tipo> = <valor>
<asignacion> ::= <identificador> = <valor>

<condicional> ::= si <expresion> { <bloques>* } (sino { <bloques>* })?
<bucle> ::= repetir <identificador> desde <valor> hasta <valor> { <bloques>* }
          | mientras <expresion> { <bloques>* }

<funcion> ::= funcion <identificador>(<parametros>): <tipo> { <bloques>* retornar <valor> }

<llamada> ::= <identificador>(<argumentos>)

<io> ::= leer(<identificador>) | mostrar(<expresion>)

<tipo> ::= texto | entero | booleano | decimal
<valor> ::= número | cadena | verdadero | falso | expresión
```

---

## 🛠️ Ejemplo

```Elysion
inicio

nombre: texto = "Ana"
edad: entero = 17

si edad >= 18 {
  mostrar("Es mayor de edad")
} sino {
  mostrar("Es menor de edad")
}

funcion cuadrado(n: entero): entero {
  retornar n * n
}

mostrar(cuadrado(5))

fin
```

---


## 📊 Características Técnicas de Elysion

| **Aspecto**                        | **Descripción**                                                                 |
|------------------------------------|----------------------------------------------------------------------------------|
| **Paradigma**                      | Imperativo, estructurado                                                        |
| **Tipo de datos**                  | Primitivos: `texto`, `entero`, `booleano`, `decimal`                            |
| **Tipado**                         | Estático                                                                        |
| **Inferencia de tipos**           | No (el tipo debe declararse explícitamente)                                     |
| **Asignación**                     | Sí, con sintaxis `<identificador>: <tipo> = <valor>` y reasignación posterior   |
| **Nivel de abstracción**          | Medio (estructura clara, sin colecciones complejas ni objetos)                  |
| **Independencia de la máquina**   | Sí (lenguaje pseudocódigo, independiente de hardware y sistema operativo)       |
| **Orientado a objetos**           | No                                                                              |
| **Esotérico**                     | Moderadamente (por ser diseñado con fines didácticos y no de producción)        |
| **Extensibilidad**                | Parcial (no permite nuevos tipos, pero sí más funciones)                        |
| **Modularidad**                   | Parcial (soporta funciones pero no módulos o espacios de nombres)               |
| **Concurrencia**                  | No                                                                              |
| **Gestión de errores/excepciones**| No contemplada                                                                  |
| **Gestión de memoria**            | No modelada (modelo abstracto sin alocación explícita)                          |
| **Modelo de ejecución**           | Interpretado (pseudocódigo, no compilado)                                       |
| **Entrada de datos**              | Sí (`leer(<identificador>)`)                                                    |


## 🔁 Control de Flujo en Elysion

| **Mecanismo**                            | **Soportado**                            |
|------------------------------------------|-------------------------------------------|
| **Secuencial**                           | ✔️ Sí                                     |
| **Condicional**                          | ✔️ Sí (`si`, `sino`)                      |
| **Iterativo**                            | ✔️ Sí (`mientras`, `repetir`)             |
| **Recursividad**                         | ✔️ Sí (funciones pueden llamarse a sí mismas) |
| **Pasaje de parámetros**                 | ✔️ Por valor                              |
| **Valores por defecto en parámetros**    | ❌ No                                      |
| **Funciones con retorno**                | ✔️ Sí                        |
| **Saltos incondicionales**      | ❌ No                                      |
| **Saltos controlados**| ❌ No                                      |
| **Control estructurado**                 | ✔️ Sí                                      |
| **Control no estructurado**              | ❌ No                                      |

## 🧾 Resumen técnico de Elysion

| **Campo**             | **Valor**                         |
|-----------------------|-----------------------------------|
| **Nombre**            | Elysion                          |
| **Paradigma**         | Imperativo, estructurado          |
| **Nivel**             | Medio                             |
| **Dominio**           | Educativo / Didáctico             |
| **Traductor**         | Interpretado                      |
| **Almacenamiento**    | Estático (tipado explícito)       |
| **Generación**        | Cuarta generación (lenguaje de alto nivel) |


## Algunas consideraciones

- **Elysion** es un lenguaje diseñado para ser didáctico, por lo que no incluye características avanzadas como concurrencia, gestión de memoria o excepciones.
- Sobrecarga: No se permite la sobrecarga de funciones o operadores.
- No se permite la creación de nuevos tipos de datos o estructuras complejas más allá de los tipos primitivos.
- No se contempla la gestión de errores o excepciones, por lo que cualquier error de sintaxis o semántica detendrá la ejecución del programa.
- El modelo de ejecución es interpretado, lo que significa que no se compila a código máquina, sino que se ejecuta directamente como pseudocódigo.
- La entrada de datos se realiza de manera sencilla a través de la instrucción `leer`, y la salida se maneja con `mostrar`.
- El lenguaje no contempla la creación de bibliotecas o módulos externos, por lo que todas las funciones deben definirse dentro del mismo programa.
