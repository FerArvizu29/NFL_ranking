# NFL_ranking

## Resumen

Este proyecto presenta un **ranking de posiciones ofensivas de la NFL**, basado en **métricas propias derivadas del análisis de redes complejas**, con el objetivo de evaluar el rendimiento deportivo más allá de las estadísticas tradicionales.

Se diseñó e implementó un **multiplicador de presión contextual**, que ajusta el valor de cada jugada según condiciones de tiempo, oportunidad y posición en el campo, con el fin de capturar una noción más cercana a la percepción humana de *“jugar bien”* y permitir comparaciones más justas entre jugadores y equipos.

---

## Metodología

Como primer acercamiento, el modelo se desarrolló utilizando la **temporada 2024 de la NFL**.

Los datos base pueden descargarse en el siguiente enlace:  
https://drive.google.com/file/d/1_WQBcUbBWFrpdvwXjfUshBHJq1ZBQCNl/view?usp=sharing

El flujo de trabajo fue el siguiente:

- Se asignó una **valoración base a cada jugada**, incorporando un **multiplicador de presión contextual** definido a partir de variables de tiempo, oportunidades y posición en el campo.
- Se construyeron **redes (grafos) por partido y por equipo**, modelando las interacciones ofensivas.
- Se calcularon **métricas de redes** (grado de entrada ponderado, grado de salida ponderado y centralidades) para cuantificar el rendimiento de cada posición ofensiva.
- Las métricas fueron **agregadas por jugador y por equipo**, permitiendo la construcción de rankings comparativos.
- Los resultados del análisis se resumen en el reporte técnico:  
  _reporte_nfl.pdf_

Posteriormente, el modelo fue **escalado a las temporadas 2021–2024**, reutilizando el mismo código y ajustando únicamente los archivos de entrada.

Los datos resumidos de las cuatro temporadas analizadas pueden descargarse aquí:  
https://drive.google.com/file/d/1vGvkhl0msdMrSoaLPqcos-wI5faAePqc/view?usp=sharing

Finalmente, se desarrolló un **dashboard interactivo**, donde se visualizan los rankings segmentados por temporada y por escenario (multiplicador de presión activo / inactivo).  
Se incluyen imágenes de referencia:  
_Dashboard_ConPresion_2024.png_, _Dashboard_SinPresion_2024.png_.
