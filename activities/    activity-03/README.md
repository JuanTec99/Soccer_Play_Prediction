# Avance 3 — Modelo Baseline
## Soccer Play Prediction

**Equipo 52**

### Objetivo

Desarrollar y evaluar un modelo baseline para la predicción de posiciones futuras de jugadores de fútbol utilizando datos de seguimiento de diez partidos de la Serie A italiana.

### Metodología

Se implementaron y compararon tres modelos:

1. Persistencia.
2. Velocidad constante.
3. Random Forest Regressor.

Se utilizaron 13 características relacionadas con posición, velocidad, aceleración y contexto espacial.

Los datos se dividieron por partidos:

- Entrenamiento: 6 partidos.
- Validación: 2 partidos.
- Prueba: 2 partidos.

### Resultados

Error medio de posición en el conjunto de prueba:

| Horizonte | Persistencia | Velocidad constante | Random Forest |
|---|---:|---:|---:|
| 0.52 s | 1.1812 m | 0.2563 m | 0.2284 m |
| 1.00 s | 2.2489 m | 0.7239 m | 0.6350 m |
| 2.00 s | 4.3572 m | 2.2294 m | 1.9240 m |

Random Forest obtuvo el menor error en los tres horizontes evaluados.

### Ejecución

El notebook `Avance3.52Equipo.ipynb` fue desarrollado y ejecutado en Google Colab.

Para reproducir el entrenamiento se requiere acceso a los archivos originales de seguimiento, organizados por partido, cada uno con:

- `tracking.parquet`
- `meta.json`

Los archivos de seguimiento no se incluyen en este repositorio debido a las restricciones de acceso a los datos de investigación.

### Conclusión

El modelo Random Forest establece una referencia cuantitativa para evaluar futuras arquitecturas de predicción de movimiento y comportamiento colectivo, incluyendo modelos basados en grafos.
