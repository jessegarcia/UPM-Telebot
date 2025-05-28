# UPM-Telebot

Chatbot institucional para consultas académicas y administrativas de la Universidad Politécnica de Madrid, desarrollado con tecnologías de RAG (Retrieval-Augmented Generation).

## 🎯 Objetivos

- Desarrollar un chatbot institucional para consultas académicas y administrativas
- Proporcionar respuestas precisas y contextualizadas mediante RAG
- Garantizar privacidad y cumplimiento del RGPD
- Facilitar la integración con plataformas universitarias existentes

## 🚀 Tecnologías

- **Modelo base**: Qwen 3 (8B)
- **Framework RAG**: LangChain con LlamaIndex
- **Base de datos vectorial**: Qdrant
- **Frontend**: Streamlit para interfaz web interactiva
- **Backend**: FastAPI para gestión de solicitudes
- **Contenedores**: Docker y Docker Compose para orquestación
- **Servidor web**: Nginx como proxy inverso y gestor de SSL

## 📁 Estructura del proyecto

```
UPM-Telebot/
├── .github/workflows/           # CI/CD pipelines
├── src/
│   ├── api/                     # FastAPI backend
│   ├── core/                    # Lógica de negocio (RAG, LLM, embeddings)
│   ├── data/                    # Gestión de datos e ingesta
│   ├── frontend/                # Streamlit UI
│   └── utils/                   # Utilidades compartidas
├── tests/                       # Pruebas unitarias e integración
├── docs/                        # Documentación adicional
├── data/                        # Documentos institucionales
├── config/                      # Configuraciones
├── docker/                      # Dockerfiles y configs
└── scripts/                     # Scripts de automatización
```

## 🛠️ Comandos importantes

```bash
# Levantar todos los servicios en local
docker-compose up

# Indexar nuevos documentos en la base vectorial
python ingest.py

# Ejecutar la suite de pruebas
pytest tests/

# Formatear el código según convenciones
black .
```

## 🔄 Flujo de desarrollo

1. Crear rama `feature/nombre-descriptivo` desde `main`
2. Implementar cambios siguiendo las buenas prácticas documentadas
3. Verificar la funcionalidad en entorno de desarrollo
4. Realizar pruebas unitarias y de integración
5. Solicitar revisión de código antes de fusionar a `main`
6. Desplegar en entorno de staging para validación
7. Promover a producción tras aprobación y pruebas finales

## 📋 Requisitos

- Python 3.9+
- Docker y Docker Compose
- Node.js (para herramientas de desarrollo)

## 🚀 Inicio rápido

```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/UPM-Telebot.git
cd UPM-Telebot

# Configurar variables de entorno
cp .env.example .env

# Levantar servicios
docker-compose up -d

# Acceder a la aplicación
# Frontend: http://localhost:8501
# API: http://localhost:8000
```

## 📚 Documentación

- Ver [CLAUDE.md](./CLAUDE.md) para instrucciones técnicas detalladas
- Consultar [docs/](./docs/) para documentación adicional

## 📄 Licencia

Ver [LICENSE](./LICENSE) para más detalles.