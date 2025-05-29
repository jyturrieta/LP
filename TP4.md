## Trabajo Práctico N°4

### Realizar el árbol de analisis sintáctico y el diagrama de sintactico para el lenguaje Deadfish

### GIC

```gic
S -> C
C -> iC | dC | sC | oC | i | d | s | o 
```

### Árbol de análisis sintáctico

El siguiente árbol de análisis sintáctico representa la secuencia de comandos del lenguaje Deadfish para la cadena `iisdo`:

```mermaid
flowchart TD
    %% Configuración de estilos
    classDef program fill:#6e0dd0,stroke:#333,color:white
    classDef sequence fill:#2563eb,stroke:#333,color:white
    classDef command fill:#059669,stroke:#333,color:white
    classDef terminal fill:#f59e0b,stroke:#333
    classDef epsilon fill:#9ca3af,stroke:#333

    %% Árbol de parsing
    A[SECUENCIA]:::program --> B[COMANDO]:::sequence
    B --> C1[i]:::command 
    B --> S1[COMANDO]:::sequence
    S1 --> C2[i]:::command 
    S1 --> S2[COMANDO]:::sequence
    S2 --> C3[s]:::command 
    S2 --> S3[COMANDO]:::sequence
    S3 --> C4[d]:::command 
    S3 --> S4[COMANDO]:::sequence
    S4 --> C5[o]:::command 
   
```

### Diagrama de análisis sintáctico CONWAY

![image](https://raw.githubusercontent.com/jyturrieta/LP/refs/heads/main/diagrama.png)