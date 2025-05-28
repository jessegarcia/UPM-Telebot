# API Backend - UPM-Telebot

## Descripción

Backend desarrollado con FastAPI para gestionar las solicitudes del chatbot y orquestar la funcionalidad RAG.

## Tecnologías

- **FastAPI**: Framework web asíncrono
- **Pydantic**: Validación de datos y serialización
- **SQLAlchemy**: ORM para base de datos
- **Redis**: Cache y gestión de sesiones
- **Uvicorn**: Servidor ASGI

## Estructura

```
api/
├── routes/              # Endpoints organizados por funcionalidad
├── middleware/          # Middleware personalizado (auth, logging, etc.)
├── models/              # Modelos de datos (SQLAlchemy)
├── schemas/             # Esquemas Pydantic para validación
├── dependencies/        # Dependencias inyectables
├── main.py             # Aplicación FastAPI principal
└── config.py           # Configuración de la API
```

## Endpoints principales

- `POST /chat/message` - Procesar mensaje del usuario
- `POST /chat/session` - Crear nueva sesión de chat
- `GET /chat/history/{session_id}` - Obtener historial
- `POST /documents/upload` - Subir documentos para indexación
- `GET /health` - Endpoint de salud
- `GET /metrics` - Métricas de rendimiento

## Middleware implementado

- **CORS**: Configuración para frontend
- **Authentication**: JWT para endpoints protegidos
- **Rate Limiting**: Prevención de abuso
- **Request Logging**: Trazabilidad de solicitudes
- **Error Handling**: Manejo centralizado de errores

## Buenas prácticas

- Usar dependency injection para servicios
- Implementar validación estricta con Pydantic
- Aplicar principios REST en el diseño de endpoints
- Documentación automática con OpenAPI/Swagger
- Manejo asíncrono para operaciones I/O intensivas
- Logging estructurado para observabilidad

## Configuración

Variables de entorno requeridas en `.env`:

```
API_HOST=0.0.0.0
API_PORT=8000
DATABASE_URL=postgresql://user:pass@localhost/upm_telebot
REDIS_URL=redis://localhost:6379
JWT_SECRET_KEY=your-secret-key
QDRANT_URL=http://localhost:6333
```

## Comandos útiles

```bash
# Ejecutar en desarrollo
uvicorn main:app --reload --host 0.0.0.0 --port 8000

# Ejecutar migraciones
alembic upgrade head

# Generar migración
alembic revision --autogenerate -m "descripción"
```

## Integración con RAG

La API actúa como orquestador entre el frontend y el sistema RAG:

1. Recibe consulta del usuario
2. Extrae contexto del vectorstore (Qdrant)
3. Envía prompt enriquecido al modelo Qwen 3
4. Procesa y valida la respuesta
5. Retorna resultado al frontend