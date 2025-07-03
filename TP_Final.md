
# 📘 Lenguaje Esotérico: **LUMINA**

## 🎯 Objetivo
**LUMINA** es un lenguaje esotérico diseñado con fines didácticos y de análisis formal. A diferencia de otros lenguajes esotéricos minimalistas, **su sintaxis es clara y expresiva**, pensada para ser fácil de entender, leer y extender.

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
```lumina
mensaje: texto = "Hola"
contador: entero = 10
activo: booleano = verdadero
pi: decimal = 3.14
```

---

## 🔧 Asignación y Variables

```lumina
nombre: texto = "Ana"
edad: entero = 25
```

Reasignación:
```lumina
edad = 26
```

---

## 🔁 Bucles

```lumina
repetir i desde 0 hasta 10 {
  mostrar(i)
}
```

O también:

```lumina
mientras edad < 30 {
  edad = edad + 1
}
```

---

## 🔀 Condicionales

```lumina
si edad >= 18 {
  mostrar("Mayor de edad")
} sino {
  mostrar("Menor de edad")
}
```

---

## ✨ Funciones

```lumina
funcion sumar(a: entero, b: entero): entero {
  resultado: entero = a + b
  retornar resultado
}
```

Llamada:

```lumina
total: entero = sumar(10, 5)
```

---

## 📢 Entrada / Salida

```lumina
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

## 🛠️ Ejemplo Completo

```lumina
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

## 📊 Ficha Técnica

| Aspecto               | Valor                        |
|-----------------------|------------------------------|
| Paradigma             | Imperativo, estructurado     |
| Tipado                | Estático, obligatorio        |
| Legibilidad           | Alta                         |
| Funciones             | Sí, con retorno              |
| Bucles                | Sí (mientras, repetir)       |
| Condicionales         | Sí (si, sino)                |
| Entrada / salida      | Sí                           |
| Objetos               | No                           |
| Sintaxis esotérica    | No extrema, sino moderada    |
| Identificadores       | Cualquier combinación válida |
| Inspiración           | Pseudocódigo, Python         |
