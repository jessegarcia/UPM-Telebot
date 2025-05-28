# Documentación - UPM-Telebot

## Descripción

Documentación técnica y de usuario para el proyecto UPM-Telebot.

## Estructura de documentación

```
docs/
├── architecture/        # Documentación de arquitectura
├── deployment/         # Guías de despliegue
├── development/        # Guías de desarrollo
├── user-guides/        # Manuales de usuario
├── api/               # Documentación de API
└── troubleshooting/   # Resolución de problemas
```

## Tipos de documentación

### Arquitectura
- Diagramas de componentes y flujo de datos
- Decisiones arquitectónicas (ADRs)
- Patrones y principios aplicados
- Integración con sistemas existentes

### Desarrollo
- Guía de configuración del entorno
- Convenciones de código y estilo
- Flujo de desarrollo y Git workflow
- Testing y QA guidelines

### Despliegue
- Configuración de entornos (dev, staging, prod)
- Scripts de automatización
- Monitoring y observabilidad
- Backup y recuperación

### Usuario
- Manual de uso del chatbot
- FAQ y casos de uso comunes
- Configuración de permisos
- Gestión de documentos

## Herramientas de documentación

- **Markdown**: Formato principal para documentación
- **Mermaid**: Diagramas de flujo y arquitectura
- **OpenAPI**: Documentación automática de API
- **MkDocs**: Generación de sitio de documentación

## Buenas prácticas

- Mantener documentación actualizada con el código
- Usar ejemplos claros y casos de uso reales
- Incluir capturas de pantalla para interfaces
- Versionado de documentación junto con releases
- Reviews de documentación en PRs

## Convenciones

- Usar Spanish para documentación de usuario
- Usar English para documentación técnica interna
- Seguir estructura consistente en todos los docs
- Incluir metadata (autor, fecha, versión)

## Plantillas disponibles

- `template-adr.md`: Architecture Decision Record
- `template-feature.md`: Documentación de features
- `template-api.md`: Documentación de endpoints
- `template-deployment.md`: Guías de despliegue

## Comandos útiles

```bash
# Generar documentación local
mkdocs serve

# Construir documentación estática
mkdocs build

# Desplegar documentación
mkdocs gh-deploy
```