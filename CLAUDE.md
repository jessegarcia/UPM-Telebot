# UPM-Telebot

## Objetivos del proyecto

	•	Desarrollar un chatbot institucional para consultas académicas y administrativas
	•	Proporcionar respuestas precisas y contextualizadas mediante RAG
	•	Garantizar privacidad y cumplimiento del RGPD
	•	Facilitar la integración con plataformas universitarias existentes

## Tecnologías utilizadas

	•	Modelo base: Qwen 3 (8B)
	•	Framework RAG: LangChain con LlamaIndex
	•	Base de datos vectorial: Qdrant
	•	Frontend: Streamlit para interfaz web interactiva
	•	Backend: FastAPI para gestión de solicitudes
	•	Contenedores: Docker y Docker Compose para orquestación
	•	Servidor web: Nginx como proxy inverso y gestor de SSL

## Buenas prácticas

	•	Indexar documentos institucionales en formato PDF y HTML
	•	Utilizar embeddings optimizados para recuperación eficiente
	•	Implementar control de versiones en la base de conocimientos
	•	Aplicar autenticación y autorización en endpoints sensibles
	•	Monitorizar logs y métricas para mejora continua
	•	Asegurar cifrado de datos en tránsito y en reposo

## Patrones aprendidos

	•	Las consultas al modelo se enriquecen con contexto recuperado dinámicamente
	•	Separación clara entre lógica de recuperación y generación de respuestas
	•	Uso de identificadores únicos para trazabilidad de conversaciones
	•	Manejo de sesiones para mantener coherencia en diálogos prolongados

## Decisiones arquitectónicas

	•	Adopción de arquitectura hexagonal para modularidad (28/05/2025)
	•	Implementación de RAG para respuestas basadas en documentos (28/05/2025)
	•	Integración con sistemas existentes mediante APIs RESTful (28/05/2025)

## Comandos importantes

	•	docker-compose up - Levanta todos los servicios en local
	•	python ingest.py - Indexa nuevos documentos en la base vectorial
	•	pytest tests/ - Ejecuta la suite de pruebas
	•	black . - Formatea el código según convenciones

## Pasos a completar en cada nueva feature

	1.	Crear rama feature/nombre-descriptivo desde main
	2.	Implementar cambios siguiendo las buenas prácticas documentadas
	3.	Verificar la funcionalidad en entorno de desarrollo
	4.	Realizar pruebas unitarias y de integración
	5.	Solicitar revisión de código antes de fusionar a main
	6.	Desplegar en entorno de staging para validación
	7.	Promover a producción tras aprobación y pruebas finales
