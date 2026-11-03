# API de tienda — Entrega 3 Web

Proyecto académico de backend para una tienda. Implementa rutas de autenticación, productos, carrito, compras, usuarios y administración con Node.js y Express. La especificación de la API está en [`api.yaml`](api.yaml) y se sirve con Swagger UI en `/api/home`.

## Tecnologías

Node.js, Express, JavaScript, PostgreSQL (Neon), JWT y OpenAPI.

## Estructura

- `index.js`: servidor y registro de rutas.
- `routes/`: definición de endpoints.
- `controllers/`: lógica de cada módulo.
- `middleware.js`: middleware de la API.
- `api.yaml`: documentación OpenAPI.

## Ejecutar localmente

Instala las dependencias con `npm install` y ejecuta `node index.js`. El servidor escucha en el puerto `3001`. Para las funciones que usan base de datos se necesita configurar la conexión utilizada en `db.js`.

> Entrega académica de 2024. El repositorio documenta el trabajo realizado y no se presenta como servicio desplegado.
