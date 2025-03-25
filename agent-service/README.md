# Agent Service

Este repositorio contiene el código del microservicio de **Agente Virtual de IA** del CRM modular. Este módulo proporciona una interfaz inicial (MVP) para la interacción automatizada, procesando mensajes y generando respuestas automatizadas. Su diseño está preparado para futuras integraciones con modelos avanzados de procesamiento de lenguaje natural (NLP).

---

## Funcionalidades Clave

- **Chat Automatizado:**
  - Endpoint para recibir mensajes del usuario y devolver respuestas predeterminadas o dinámicas.
  - Base inicial para implementar capacidades de IA más avanzadas en el futuro.

- **Generación de Informes Preliminares (Opcional):**
  - Endpoint para proporcionar reportes básicos, basado en datos del sistema.
  - Ejemplo: Cantidad de leads activos, oportunidades en negociación, entre otros.

- **Futuras Integraciones:**
  - Preparación para incorporar librerías de IA como Hugging Face, TensorFlow o LangChain para generación de respuestas contextuales más avanzadas.

---

## Requisitos Previos

- **Python 3.9 o superior:** Asegúrate de tener Python instalado en tu sistema.
- **Docker:** Opcional, para ejecutar el servicio en un entorno contenedor.

---

## Estructura del Proyecto

El microservicio sigue la **arquitectura hexagonal**, separando la lógica central de las dependencias externas.

agent-service/ 
├── app/ 
│ ├── dominio/ # Entidades y modelos del núcleo del negocio 
│ ├── aplicacion/ # Casos de uso para la generación de respuestas y análisis 
│ ├── infraestructura/ # Adaptadores para servicios externos (NLP, APIs de análisis) 
│ └── interfaces/ # Endpoints y validaciones 
├── tests/ # Pruebas unitarias e integrales 
├── Dockerfile # Configuración de contenedor 
├── requirements.txt # Dependencias del proyecto 
└── README.md # Documentación del servicio