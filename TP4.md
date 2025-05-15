## Trabajo Práctico N°4

### Realizar el árbol de analisis sintáctico y el diagrama de sintactico para el lenguaje Deadfish

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
    A[PROGRAMA]:::program --> B[SECUENCIA]:::sequence
    B --> C1[COMANDO]:::command --> T1["i"]:::terminal
    B --> S1[SECUENCIA]:::sequence
    S1 --> C2[COMANDO]:::command --> T2["i"]:::terminal
    S1 --> S2[SECUENCIA]:::sequence
    S2 --> C3[COMANDO]:::command --> T3["s"]:::terminal
    S2 --> S3[SECUENCIA]:::sequence
    S3 --> C4[COMANDO]:::command --> T4["d"]:::terminal
    S3 --> S4[SECUENCIA]:::sequence
    S4 --> C5[COMANDO]:::command --> T5["o"]:::terminal
    S4 --> S5[SECUENCIA]:::sequence --> E[ε]:::epsilon
```

### Diagrama de análisis sintáctico CONWAY

![image](/LP/diagrama.png)