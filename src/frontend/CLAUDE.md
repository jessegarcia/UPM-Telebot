# Frontend - UPM-Telebot

## Descripción

Interfaz web interactiva desarrollada con Streamlit para el chatbot institucional de la UPM.

## Tecnologías

- **Streamlit**: Framework principal para la interfaz web
- **Python**: Lenguaje de programación
- **CSS personalizado**: Para estilos específicos de la UPM

## Estructura

```
frontend/
├── components/          # Componentes reutilizables
├── pages/              # Páginas de la aplicación
├── app.py              # Aplicación principal
├── config.py           # Configuración del frontend
└── utils.py            # Utilidades específicas del frontend
```

## Componentes principales

- **Chat Interface**: Interfaz principal de conversación
- **Document Upload**: Subida de documentos para indexación
- **Admin Panel**: Panel de administración para gestores
- **Analytics Dashboard**: Métricas de uso y rendimiento

## Buenas prácticas

- Usar session_state para mantener estado entre interacciones
- Implementar componentes modulares y reutilizables
- Aplicar el branding oficial de la UPM
- Asegurar responsive design para móviles
- Optimizar tiempos de carga y experiencia de usuario

## Configuración

Las variables de entorno específicas del frontend se definen en `.env`:

```
STREAMLIT_SERVER_PORT=8501
STREAMLIT_SERVER_ADDRESS=0.0.0.0
API_BASE_URL=http://localhost:8000
```

## Comandos útiles

```bash
# Ejecutar en desarrollo
streamlit run app.py

# Ejecutar con configuración específica
streamlit run app.py --server.port 8501 --server.address 0.0.0.0
```