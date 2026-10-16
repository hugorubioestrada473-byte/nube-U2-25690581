1. Separa la API del Ej. 3 en serviocios de ventas y servicio de IA
2. Entrena un modelo sencillo (p.ej.LinearrRegresion con datos sinteticos de ventas) y guardalo con joblib
3. Agrega un gateway y levanta todo con docker compose
4. Ejecuta carga.py con 1 y con 3 replicas: reporta rps, p50 y p95
5. Ejecuta el mismo compose en GitHub Codespaces con el puerto publico