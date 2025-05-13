## Trabajo Práctico N°4

### Realizar el árbol de analisis sintáctico y el diagrama de sintactico para el lenguaje Deadfish

### Árbol de análisis sintáctico

El siguiente árbol de análisis sintáctico representa la secuencia de comandos del lenguaje Deadfish para la cadena `iisdo`:

```mermaid
flowchart TD
    A[PROGRAMA] --> B[SECUENCIA]
    B --> C1[COMANDO] --> T1["i"]
    B --> D1[SECUENCIA]
    D1 --> C2[COMANDO] --> T2["i"]
    D1 --> D2[SECUENCIA]
    D2 --> C3[COMANDO] --> T3["s"]
    D2 --> D3[SECUENCIA]
    D3 --> C4[COMANDO] --> T4["d"]
    D3 --> D4[SECUENCIA]
    D4 --> C5[COMANDO] --> T5["o"]
    D4 --> D5[SECUENCIA] --> E[ε]
```

### Diagrama de análisis sintáctico CONWAY


