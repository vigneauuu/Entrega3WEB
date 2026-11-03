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

Se necesita Node.js 20.6 o posterior para el comando con `--env-file` y una base PostgreSQL con el esquema esperado por los controladores. Este repositorio no incluye una migración que prepare ese esquema.

Copia `.env.example` a `.env` y configura `DATABASE_URL` con tu conexión propia y `JWT_SECRET` con una clave aleatoria exclusiva. Ambos valores son obligatorios; firma y verificación usan la misma variable. Mantén `.env` fuera de Git.

Luego ejecuta:

```bash
npm install
node --env-file=.env index.js
```

El servidor escucha en el puerto `3001`. La documentación de la API queda en `http://localhost:3001/api/home`.

> Entrega académica de 2024. El repositorio documenta el trabajo realizado y no se presenta como servicio desplegado.

## Estado y seguridad

La conexión y una clave JWT antiguas estuvieron publicadas. Si existió un despliegue, hay que cambiar la contraseña del rol PostgreSQL, actualizar la conexión y reemplazar `JWT_SECRET` en ese entorno; los tokens anteriores deben dejar de aceptarse. Quitar los valores del código no borra el historial ni revoca credenciales.

La ejecución con una base de datos real no se ha verificado en esta revisión. Antes de desplegar, revisa el esquema, permisos, validación de entradas, CORS y configuración de cookies para HTTPS.
