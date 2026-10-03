# Ejercicio 01: APIs REST

## Tabla de resultados

| API / Endpoint | Método | Código | Tiempo (ms) | Bytes |
| --- | --- | --- | --- | --- |
| JSONPlaceholder (Listar posts) | GET | 200 | 720 ms | 27520 B |
| JSONPlaceholder (Crear post) | POST | 201 | 667 ms | 35 B |
| PokéAPI (Pikachu) | GET | 200 | 716 ms | 300521 B |
| OpenWeatherMap (Cd. Valles) | GET | 401 | 725 ms | 108 B |
| Recurso Inexistente | GET | 404 | 606 ms | 2 B |
| Sin Clave / Clave inválida | GET | 401 | 713 ms | 108 B |

---

## Errores provocados

* **404 (Not Found):** Consulté un recurso inexistente. La API regresó el código 404 y un JSON vacío `{}` de 2 bytes.
* **401 (Unauthorized):** Mandé la petición a OpenWeatherMap con una API Key inválida/inexistente. Me regresó el código 401 avisando que la petición requiere autenticación válida.

---

## Respuestas a las preguntas

* **¿Qué parte de la respuesta realmente usaste?**
De la PokéAPI solo tomé los nombres de las habilidades de Pikachu, que en el resultado fueron `['static', 'lightning-rod']`.
* **¿Qué porcentaje de los bytes recibidos fue innecesario?**
La respuesta completa de la PokéAPI pesó 300,521 bytes (~300.5 KB) debido a que incluye imágenes, movimientos, versiones y estadísticas detalladas. Como los nombres de las dos habilidades (`'static'` y `'lightning-rod'`) junto con la estructura JSON que los contiene equivalen a menos de 100 bytes útiles, **más del 99.96%** del payload recibido fue innecesario para el objetivo de la consulta.